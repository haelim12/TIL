## 4. Grouping data

### **GROUP BY clause** : 레코드를 그룹화하여 요약본 생성 with 집계함수

#### **< Examples >**

1. customerㄴ 테이블에서 country 필드를 그룹화하여 각 그룹에 대한 creditLimit 의 평균값을 내림차순 조회

```python
    SELECT
        country, AVG(creditLimit)
    FROM
        customerㄴ
    GROUP BY
        country
    ORDER BY
        AVG(creditLimit) DESC;
```

2. customers 테이블에서 country 필드를 그룹화하여 각 그룹에 대한 creditLimit 의 평균값이 80000을 초과하는 데이터

```python
    SELECT
        country, AVG(creditLimit)
    FROM
        customers
    GROUP BY
        country
    HAVING
        AVG(creditLimit) > 80000;
```

- **HAVING** clause : 집계 항목에 대한 세부조건 지정

    주로 GROUP BY와 함께 사용되며 GROUP BY 가 없다면 WHERE 처럼 동작