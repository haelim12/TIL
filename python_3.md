
- for 문 : 반복 가능한 객체 모두 순회하면 종료 

    - 반복 가능 객체 : 요소

    - range : index

- while 문 : 종료 조건에 해당하는 코드를 통해 반복문을 종료시켜야 함

- 반복 제어 : break, continue, for-else

## while 문

- 조건식이 참인 경우 반복적으로 코드 실행

- while <expression>:
    code block

- 예시)
    ```python
    a = 0
    while a < 5:
        print(a)
        a += 1
    print('끝')
    ```

## 함수의 기초

- 함수 : 특정한 기능을 하는 코드의 조각

- 함수를 사용해야 되는 이유 : 재사용, 중복 방지

    - 내장함수 활용

    - pstdev 함수

- 자주 사용하는 함수

    - len(s), sum(iterable, start=0), max(), min()

- 수학 관련 함수

    - abs(x) : 절댓값

    - divmod(a, b), round 

- 논리 관련 함수

    - all(iterable) : 모두 참이면 True

    - any(iterable) : 어느 하나라도 참이면 True

- 기타 함수

    - bin(x), hex(x), oct(x), ord(), chr()


## map

- map(function, iterable) : 순회 가능한 데이터 구조(iterable)의 모든 요소에 함수(function)을 적용

- 알고리즘 문제 풀이 시 input 값들을 숫자로 바로 활용하고 싶을 때
