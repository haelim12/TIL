# SQL - Single Table Queries 1

##  1. Querying data

## **SELECT statement**

테이블에서 데이터 조회

### SELECT syntax
```python
    SELECT
        select_list
    FROM
        table_name;
```
    
- SELECT 키워드 다음에 데이터를 선택하려는 필드 하나 이상 지정

- FROM 키워드 다음에 데이터를 선택하려는 테이블의 이름을 지정

#### Examples

1. 테이블 employees 에서 lastName, FirstName 필드의 모든 데이터 조회

    
```python
    SELECT
        lastName, FirstName
    FROM
        employees;
```

2. 테이블 employees 에서 모든 필드의 데이터 조회

```python
    SELECT
        *
    FROM
        employees;
```

3. 테이블 employees 에서 firstName 필드의 모든 데이터 조회
(단, firstName 이 아닌 '이름'으로 출력될 수 있도록 변경)

```python
    SELECT
        firstName AS '이름'
    FROM
        employees;
```

4. 테이블 orderdetails에서 productCode, 주문총액 필드의 모든 데이터 조회
(주문총액 = quantityordered 와 priceEach 곱한 값)

```python
    SELECT
        productCode,
        quantityOrdered * priceEach AS '주문총액'
    FROM
        orderdetails;
```

- Arithmetic Operators

기본적인 사칙연산 사용 가능

---

## **SELECT 정리**

- SELECT 문을 사용하면 테이블의 데이터를 조회, 반환

- SELECT * 를 사용하여 테이블의 모든 필드 선택
