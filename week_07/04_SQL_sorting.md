## 2. Sorting data

### ORDER BY syntax

- FROM clause 뒤에 위치

- ASC : 오름차순(기본값), DESC : 내림차순

### **< Examples >**

1. 테이블 employees 에서 firstName 필드의 모든 데이터를 오름차순 조회

```python
    SELECT
        firstName
    FROM
        employees
    ORDER BY
        firstName;
```

2. 테이블 employees에서 lastName 필드를 내림차순, firstName 필드를 오름차순 정렬

```python
    SELECT
        lastName, firstName
    FROM
        employees
    ORDER BY
        lastName DESC,
        firstName;
```

---

### SELECT statement 실행 순서

1. 테이블에서 (FROM)

2. 조회하여 (SELECT)

3. 정렬 (ORDER BY)