# 사용자 정의 함수

## 함수의 결과값 (Output)

- return

    - 함수는 반두시 값을 하나만 return

    - return 과 동시에 실행이 종료

    - return vs print

        - return : 함수 안에서 값을 반환하기 위해 사용되는 키워드

        - print : 출력을 위해 사용되는 함수

## 함수의 입력 (Input)

- parameter

    - 함수를 실행할 때, 함수 내부에서 사용되는 식별자

    - 
    ```python
    def function(ham) #parameter : ham
        return ham
    ```

- argument

    - 함수를 호출할 때 넣어주는 값

    - 
    ```python
    function('spam')  # argument : 'spam'
    ```

    - 함수 호출 시 함수의 parameter를 통해 전달되는 값

    - positional arguments. keyword arguments

    - print(*~) : 정해지지 않은 개수의 argument

## 함수의 범위 (Scope)

- LEGB

    def ~~~~()

# 정리

> input
    
    기본 -> 위치 : 키워드로 호출

    def foo(x, y) : foo(1, 2)
    def foo(x, y = 0, z=1) : foo(1) foo(1, z=3)
    def foo(*x) : tuple foo(1, 2, 3, ...)
    def foo(**kwarg) : dictionary foo(1=1, 2=2, ...)

> output
    
    하나의 객체를 return
    여러 개 ? => tuple