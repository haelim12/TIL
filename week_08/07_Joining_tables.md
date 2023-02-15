# 07. SQL - Multi Table Queries

## 1. Join

관계형 데이터베이스 : 데이터 간의 관계가 있는 데이터 항목들의 모음

## 2. Joining tables

### **📍INNER JOIN** clause

- 두 테이블에서 값이 일치하는 레코드에 대해서만 결과를 반환

```python
SELECT
	*
FROM
	articles
INNER JOIN users
	ON articles.userId = users.id;
```
#### Example

1. 각 주문번호 별 주문상태와 총 판매액을 요약
(주문번호는 orderNumber 필드, 총 판매액은 quantityOrdered와 priceEach 필드의 곱셈 결과)

```python
    SELECT
        orders.orderNumber, status, sum(quantityOrdered*priceEach) AS totalSales
    FROM
        orders
    INNER JOIN orderdetails
        ON orders.orderNumber = orderdetails.orderNumber
    GROUP BY orderNumber; # 각 주문번호 별 총 판매액 요약

```

### **📍LEFT JOIN** clause

- 특징 :

    - 왼쪽은 무조건 표시하고, 매치되는 레코드 없으면 NULL 표시

    - 왼쪽 테이블 한 개의 레코드에 여러 개의 오른쪽 테이블 레코드가 일치할 경우, 해당 왼쪽 레코드를 여러 번 표시

```python
SELECT
	*
FROM
	articles # 항상 왼쪽
LEFT JOIN users
	ON articles.userId = users.id;
```

#### Example

1. 주문 내역이 없는 고객의 이름과 주문번호 및 배송 상태 조회 (고객의 이름은 contactFirstName 필드, 주문번호는 orderNumber, 배송상태는 status 필드)

```python
    SELECT 
        contactFirstName, orderNumber, status
    FROM 
        customers
    LEFT JOIN orders
        ON customers.customerNumber = orders.customerNumber
    WHERE orders.orderNumber IS NULL;
```

### **📍RIGHT JOIN** clause

- 특징 :

    - 오른쪽 테이블은 무조건 표시하고 매치되는 레코드가 없으면 NULL을 표시

    - 오른쪽 테이블 한 개의 레코드에 여러 개의 왼쪽 테이블 레코드가 일치할 경우, 해당 오른쪽 레코드를 여러 번 표시

#### Example

1. 고객에게 판매한 내역이 없는 직원 목록 조회
(직원 번호와 이름은 employeeNumber, firstName 필드이며 고객 번호와 이름은 customerNumber, contactFirstName 필드)

```python
    SELECT
        employees.employeeNumber, firstName, customerNumber, contactFirstName
    FROM
        customers
    RIGHT JOIN employees
        ON customers.salesRepEmployeeNumber = employees.employeeNumber
    WHERE customerNumber IS NULL;
```

### JOIN 정리 (추가)

```python
SELECT * FROM tableA
LEFT JOIN tableB ON tableA.fk = tableB.id
UNION
SELECT * FROM tableB
RIGHT tableB ON tableA.fk = tableB.id;
```