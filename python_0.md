
# 파이썬

- 컴퓨터 프로그래밍 언어란?

    컴퓨터에게 명령하기 위한 약속

    - 컴퓨터 (Computer) : Calculation(조작), Remember(저장)

    - 프로그래밍 (programming) : 명령어의 모음(집합)

    - 언어 : 자신의 생각을 나타내고 전달하기 위한 체계


## 파이썬의 특징

- 인터프리터 언어 - 즉시 실행해서 결과

- 객체 지향 프로그래밍
    
    객체 (object) : 사물 (담는 모든 것)

## 변수

- 할당 연산자(=) 를 통해 값을 할당 (assignment)

- type() : 변수에 할당된 값의 타입

- id() : 변수에 할당된 값(객체)의 고유한 아이덴티티

- x = 'hi'
    type(x) #str
    id(x) #

- **변수 할당**

    - 같은 값을 동시에 할당
        
        x = y = 1004
    
    - 다른 값을 동시에 할당 

        x, y = 1, 2

- 실습 문제 
    
    x = 10, y = 20 일 때, 각각 값을 바꿔서 저장하는 코드

    1. tmp = x
       x = y
       y = tmp
       print (x, y)
    
    2. y, x = x, y
       print (x, y)

## 식별자 (identifiers)

- 규칙 : 
    
    영문 알파벳, 언더스코어(_), 숫자로 구성
    
    첫 글자에 숫자 x
    
    길이 제한 x, 대소문자 구별

- 일반적 : **snake_case**

## 자료형 (Data Type)

## 수치형 (Numeric Type)

- 정수 (int)

    - 모든 정수 타입은 int

    - 매우 큰 수를 나타낼 때 오버 플로우가 발생하지 않음

- 실수 (Float)

    - 정수가 아닌 모든 실수는 float 타입

    - 부동소수점

        실수를 컴퓨터가 표현하는 방법 : 2진수(비트)

        Floating point rounding error : 부동소수점에서 실수 연산 과정에서 발생 가능

- 복소수 (Complex)

    - 실수부, 허수부


## 불린형

- 불린 (Boolean)

    - True / False 값을 가진 타입은 Bool
         
        True 는 1, False 는 0
    
    - 비교/논리 연산을 수행함에 있어 활용

    - 0, 0.0, (), {}. [], None : 모두 False로 변환

## 연산자 (Operator)

- 산술 연산자

    - 기본적인 사칙연산 

    : +, -, *, % (나머지), / (나눗셈), // (몫), ** (거듭제곱)

- 복합 연산자

    - a = a+b  ->  a+=b

    - a = a-b  ->  a-=b

- 비교 연산자

    - 값을 비교

    : <= 이하, >= 이상, == 같음, != 같지 않음

- 논리 연산자 (Logical Operator)

    - and : 모든 참 => 참

    - or : 둘 중 하나만이라도 참 => 참

    - not : 참 거짓의 반대의 결과

## 컨테이너

- 컨테이너 분류 

    - 시퀀스 : 문자열, 리스트, 튜플, 레인지

    - 컬렉션/비시퀀스

## 시퀀스형 컨테이너

- 시퀀스형 주요 공통 연산자

    s[i] : s의 i번 째 항목, 0 에서 시작

    s[i:j] : s의 i부터 j까지의 항목

## 문자열 (String Type)

- 모든 문자는 str 타입

- 작은 따옴표(') 나 큰 따옴표 (") 를 활용하여 표기

    하나의 소스코드 내에세는 하나의 문장부호를 선택

- 중첩 따옴표, 삼중 따옴표

- **인덱싱** 
    
    예) s = 'a,b,c,d,e,f,g'
        
    s[1] = b : **0부터 시작**

    s[2:5] = c,d,e : **5 포함 x**

### 문자열 활용

- 결합

    'hello,' + 'python!'
    => hello, python!

- 반복

- 포함

### 문자열 특징

- Immutable : 변경 불가능

- Iterable : 반복 가능

## 리스트 (List)

- 배열, 나열, array

- 정의 : 변경 가능한 값들이 나열된 자료형 [ ~~~ ]

- 생성과 접근 

    - [ ] 혹은 list() 통해 생성

    - 순서가 있는 시퀀스로 접근

- 리스트 값 추가 / 삭제

    - 값 추가 : .append() 활용

        even_numbers = [2, 4, 6, 8]

        even_numbers. append(10)

    - 값 삭제 : .pop() 활용

        even_numbers = [2, 4, 6, 8]

        even_numbers.pop(0)

        even_numbers = [4, 6, 8]

- 예시 )

    boxes = ['apple', 'banana']

    len(boxes) = 2

    boxes[1] = 'banana'
    
    boxes[1][0] = 'b'

