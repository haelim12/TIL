# The Relation

## 1. Relation Database

관계형 데이터베이스 : 데이터 간에 관계가 있는 데이터 항목들의 모음

- 테이블, 행, 열의 정보를 구조화

- 서로 관련된 데디터 포인트를 저장하고, 이에 대한 엑세스 제공

## 관계형 데이터베이스 용어

1. Table (= Relation)

2. Field (= Column, Attribute)

3. Record (= Row, Table)

4. Database (= Schema)

5. Primary Key

6. Foreign Key

## RDMS

- DBMS : 데이터베이스를 관리하는 소프트웨어 프로그램

- (R)DBMS :

    - 데이터 저장 및 관리를 용이하게 하는 시스템

    - 데이터베이스와 사용자 간의 인터페이스 역할

- MySQL

    - Table ⊂ Database ⊂ Database Server(MySQL)


---


## < 정리 >

- Table은 데이터를 기록하는 최종 위치

- 모든 Table에는 행에서 고유하게 식별 가능한 기본키라는 속성이 있으며, 외래키를 사용하여 각 행에서 서로 다른 테이블 간의 관계를 만들 수 있음

- 데이터는 기본 키 또는 외래 키를 통해 결합(join)될 수 있는 여러 테이블에 거쳐 구조화됨

- 각 Table은 Database로 그룹핑됨

- MySQL은 이러한 Database 들을 그룹핑하여 관련된 작업을 수행하는 Database Server