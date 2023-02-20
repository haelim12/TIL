# 09. SQL - Advanced 1

## 1. Transaction

: 여러 쿼리문을 묶어서  하나의 작업처럼 처리하는 방법

자동 commit 비활성화
```sql
SET autocommit = 0;
```
트랜잭션 사용해서 ROLLBACK or COMMIT

```SQL
START TRANSACTION
..
..
ROLLBACK ;
COMMIT ;

## 2. Trigger