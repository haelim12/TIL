# SQL - Nested Queries

## 1. Subquery

    단일 쿼리문에 여러 테이블의 데이터를 결합하는 방법

### Examples

1. 가장 나이가 어린 사람 삭제

```sql
    DELETE FROM table1
    WHERE age = (
        SELECT MIN(age) FROM table1
    );
```
2. 가장 많은 돈을 소비한 고객 번호 조회

```sql
    SELECT customerNumber, amount
    FROM payments
    WHERE amount = (
        SELECT MAX(amount) 
        FROM payments
    );
```

3. 미국에 있는 사무실에서 근무하는 직원의 이름과 성 조회 (직원 정보는 employees, 사무실 정보는 offices 테이블)

```sql
    SELECT lastName, FirstName
    FROM employees
    WHERE officeCode IN (
        SELECT officeCode
        FROM offices
        WHERE country = 'USA'
    );
```
4. 
```sql
SELECT customerName
FROM customers
WHERE customerNumber NOT IN (
	SELECT DISTINCT customerNumber
    FROM orders
);
```

1-1.
지불 금액이 가장 높은 고객의 customerNumber, amount, contactFirstName을 조회
```sql
    SELECT customerNumber, amount, contactFirstName
    FROM (
        SELECT *
        FROM payments
        INNER JOIN customers USING (customerNumber)
    ) AS mySub -- mySQL 에서는 임의로 만들어준 table 이름 지정 필수
    WHERE amount = (
        SELECT MAX(amount)
        FROM payments
    );
```
```sql
SELECT L.customerNumber, L.amount, R.contactFirstName
FROM payments L
INNER JOIN customers R
	ON L.customerNumber = R.customerNumber
WHERE L.amount = (
	SELECT MAX(amount)
    FROM payments
);
```
### **📍EXISTS** syntax
```sql
SELECT
	select_list
FROM
	table
WHERE 
	[NOT] EXISTS (subquery);
```

#### Examples

1. 
```sql
    SELECT customerNumber, customerName
    FROM customers
    WHERE EXISTS (
        SELECT *
        FROM orders
        WHERE customers.customerNumber = orders.customerNumber
);
```
2. Paris에 있는 사무실에서 일하는 모든 직원의 번호, 이름, 성을 조회ALTER
(직원 테이블은 employees, 사무실 테이블은 offices 이며 두 테이블의 officeCode 필드를 기준으로 비교)
```sql
SELECT employeeNumber, firstName, lastName
FROM employees
WHERE EXISTS (
	SELECT *
    FROM offices
    WHERE 
		employees.officeCode = offices.officeCode
		AND city = 'PARIS'
);
```

## 2. Conditional Statements : 조건문

### **📍CASE** syntax

```sql
CASE case_value
	WHEN when_value1 THEN statements
    WHEN when_value2 THEN statements
    ...
    [ELSE else-statements]
END CASE;
-- case_value가 when_value와 동일한 것을 찾을 때까지 순차적으로 비교
-- when_value와 동일한 case_value를 찾으면 해단 THEN 절의 코드를 실행
-- 동일한 값을 찾지 못하면 ELSE 절의 코드를 실행
```