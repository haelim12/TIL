# SQL - Managing Table

DDL : 데이터의 기본구조 및 형식변경

    - CREATE, DROP, ALTER

## 1. Create a table

### **📍 CREATE TABLE** statement

```python
    CREATE TABLE table_name(
        column_1 data_type # 각 필드의 데이터 타입
        column_2 data_type
        ...,
        constraints # 테이블 및 필드에 대한 제약조건
    );
```
- examples
```python
    CREATE TABLE examples (
        examId INT AUTO_INCREMENT,
        lastName VARCHAR(50) NOT NULL,
        firstName VARCHAR(50) NOT NULL,
        PRIMARY KEY (examId)
    );

    # Table 구조 확인 :
    #     SHOW COLUMN FROM examples;

    # 데이터 타입 : INT, VARCHAR(50)
    # 제약 조건 : NOT NULL, PRIMARY KEY
    # 속성 : AUTO_INCREMENT
```

- MySQL Data Types

    - Numeric | 숫자형 | INT, FLOAT, ... |

    - String  | 문자형 | VARCHAR, TEXT, ... |

    - Date and Time | 날짜형 | DATE, DAY, ... |

- MySQL Constraints
    
    - Constraint : 데이터의 무결성을 지키기 위해 데이터를 입력 받을 때 실행하는 검사 규칙

    - PRIMARY KEY : 해당 필드를 기본 키로 지정

    - NOT NULL : 해당 필드에 NULL 값을 저장하지 못하도록 지정


- AUTO_INCREMENT attribute

    - 테이블의 기본 키에 대한 번호 자동 생성

    - 시작 값은 1이며 데이터 입력 시 값을 생략하면 자동으로 1씩 증가

    - 재사용 x

    - NOT NULL 제약 조건을 포함

## 2. Delete a table

### **📍 DROP TABLE** statement

```python
    DROP TABLE table_name;
```
- example
```python
    DROP TABLE examples;
```

## 3. Modifying table

### **📍 ALTER TABLE** statement

#### **📎 ALTER TABLE ADD**
```python
    ALTER TABLE
        table_name
    ADD
        new_column_name column_definition;

    # ADD 키워드 이후 추가하고자 하는 새 필드 이름과 데이터 타입 및 제약 조건 작성

```
< Examples >

1. example 테이블에 age, address 필드 추가
(단, age 필드는 정수 타입 저장되면 NULL 값을 허용하지 않음.
address 필드는 가변길이 문자열 최대 100자이며 NULL 값을 허용하지 않음)

```python
    ALTER TABLE
	    examples
    ADD
	    age int NOT NULL,
    ADD
	    address VARCHAR(100) NOT NULL;
```

#### **📎 ALTER TABLE MODIFY**

< Examples >

1. examples 테이블의 lastName, firstName 필드를 가변길이 문자열 최대 10자까지 그리고 NULL 값을 허용하지 않도록 변경

```python
    ALTER TABLE
        examples
    MODIFY
        lastName VARCHAR(10) NOT NULL,
    MODIFY
        firstName VARCHAR(10) NOT NULL;
```

#### **📎 ALTER TABLE CHANGE**

```python
ALTER TABLE
	table_name
CHANGE COLUMN
	original_name new_name column_definition;
```

< Examples >

1. examples 테이블의 country 필드 이름을 state로 변경 (단, 데이터 타입 및 제약 조건은 기존과 동일)

```python
    ALTER TABLE
        examples
    CHANGE COLUMN
        country state VARCHAR(100) NOT NULL;
```

#### **📎 ALTER TABLE DROP COLUMN**

```python
ALTER TABLE
	table_name
DROP COLUMN
	column_name;
```

< Example >

1. examples 테이블의 state, age 필드 삭제

```python
    ALTER TABLE
        examples
    DROP COLUMN
        state,
    DROP COLUMN
        age;
```