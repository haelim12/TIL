
## 🎈 String Formatting

- f-string
    
    print(f'{name}는 {age}살입니다.')

    print(name + '는' + str(age) + '살입니다.')

    print('{}는 {}살입니다.'.format(name, age))

## 🎈 형 변환

### 자료형 변환 (Type Casting)

- 암시적 형 변환
    
    - 파이썬에서 내부적으로 자료형 변환

    - True + 3  # 4

    - 3 + 5.0  # 8

    - 3 + 4j + 5  # 8 + 4j

- 명시적 형 변환

    - str, float => int
        
        int('3') + 4  # 7
    
    - str, int => float

        float('3.5') + 5  # 8.5
    
    - int, float, list, tuple, dict => str

---

객체 (Object) 활용하기 위해 **Type** 과 연산자

학습 목표 :  
    
    **조건문, 반복문** 을 활용해 코드를 작성하고 문제 풀이에 적용

    ⭐중첩된 조건문과 반복문의 결과를 판단

---

## 🎈 제어문

- 파이썬은 위 -> 아래 로 순차적으로 명령 수행

- 코드를 선택적으로 실행하거나 반복하는 제어가 필요

- 순서도 (flow chart) 로 표현이 가능

## 🎈 조건문

- 참(거짓) 을 판단할 수 있는 조건식과 함께 사용
    
    - 비교 연산자 활용

- ``` python
    if ~ :
        ~
    else :
         ~
    # 들여쓰기 4칸 space

- 예시) 
```python
    num = int(input("숫자를 입력하세요 > "))
    if num % 2 ==0 :
       print("짝수")
    else :
        print("홀수")
```
```python
    num = int(input())
    if num % 2 ==1 :
        print("홀수")
    else :
        print("짝수")
```

### 복수 조건문

- elif 활용

### 중첩 조건문

## 🎈 레인지(range)

- 범위 나타낼 때

- 숫자의 시퀀스
    
    - range(n): 0 ~ n-1 

    - range(n, m) : n ~ m-1

    - range(n, m, s) : n ~ m-1 까지 s 만큼 증가

        예시) 0 부터 -6 : range(0, -6, -1)

## 🎈 반복문

- while문, for문, 반복문 제어

### for 문

- 시퀀스(string, tuple, list, range) 를 포함한 순회가능한 객체 (iterable)

- 변수에 이름을 각각 붙여줌

### 반복문 제어

- break : 반복문 종료

- continue : 다음 반복 수행

- for-else : 끝까지 반복문 실행한 이후 else 문 실행
