# SQL - Single Table Queries 2

## 3. Filtering data

데이터를 필터링해서 중복 제거, 조건 설정 등 SQL Query를 제어하기


### **DISTINCT clause** : 중복된 레코드 제거

```python
        SELECT DISTINCT
            select_list
        FROM
            table_name;
```

### **WHERE clause** : 조회 시 특정 검색 조건을 지정

```python
        SELECT 
            select_list
        FROM
            table_name; 
        WHERE
            search_condition;
```

#### **< Examples >**

1. officeCode 필드 값이 1에서 4 사이 값인 데이터
(!과 4 포함)
```python
    WHERE
        officeCode BETWEEN 1 AND 4;
```
```python
    WHERE
        officeCode >= 1
        AND officeCode <= 4;
```

2. officeCode 필드값이 1 또는 3 또는 4가 아닌 데이터

```python
    WHERE
        officeCode NOT IN (1, 3, 4)
```
```python
    WHERE
        officeCode != 1
        OR officeCode != 3
        OR officeCode !=4;
```

3. lastName 필드값이 ~son 으로 끝나는 데이터
```python
    WHERE 
        lastName like '&son';
```

3. firstName 필드값이 4자리면서 y로 끝나는 데이터
```python
    WHERE
        firstName like '___y';
```

### **Limit Clause** : 조회하는 레코드 수를 제한

```python
    LIMIT [offset], row_count;
```

#### **< Examples >**

1. officeCode 기준 내림차순으로 7개만 조회
```python
    ORDER BY
        officeCode DESC
    LIMIT 7;
```

2. 내림차순 4번째부터 8번째 데이터까지 조회
```python
    ORDER BY
        officeCode DESC
    LIMIT 3, 5; (= LIMIT 5 OFFSET 3)
```
