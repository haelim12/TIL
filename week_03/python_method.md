# 튜플

- 변경 불가능하며(immutable), 반복가능함(iterable) vs 변경 가능한 list

- (0, 1, 3) list랑 비슷

- 순서를 가지며, 서로 다른 타입의 요소를 가질 수 있음

## 생성과 접근

- 소괄호 (()) 혹은 tuple()을 통해 생성

- 값 접근 : a = (1, 2, 3, 1) -> a[1]

- 값 변경 : 불가능


# 세트

- 유일한 값들의 모임(collection)

- **순서가 없고** 중복된 값이 없음

- 변경 가능(mutable), 반복 가능(iterable)

 ## 세트 생성

- 중괄호 ({}) 혹은 set()

- 예시 
```python
    {1, 2, 3, 1, 2}  # {1, 2, 3}
    type({1, 2, 3})  # <class 'set'>
    {hi, 1, 2}  # {1, 2, hi}
```

## 추가 / 삭제

- 추가 .add()

- 삭제 .remove()

## 활용

- 다른 컨테이너에서 중복된 값 쉽게 제거 가능

- my_list = {'서울', '서울', '대전', '광주', '서울', '부산', '대전', '부산'}

    => set(my list)

# 데이터 타입과 메서드 (method)

- len(happy!)
    ```python
    word = 'happy!'
    cnt = 0
    for char in word:
        cnt += 1
    ```

- 함수 (function)

    - input().split()

    - 문자열.split()

    - 리스트.append()

    - **타입.메서드()**

# 메서드 (method)

- 시퀀스 : 문자열(string), 리스트(list)

    컬렉션 : 세트(set), 딕셔너리(dictionary)

## 문자열

- str 타입

- ' 나 " 로 표기

- 문자열 탐색

    - s.find(x) : x의 첫 번쨰 위치 반환, 없으면 -1 반환

    - s.index(X) : x의 첫 번째 위치 반환, 없으면 error

    - s.isalpa() : 알파벳 문자

    - s.isupper() : 대문자 여부

    - s.islower() : 소문자 여부

    - s.istitle() : 타이틀 형식

- 문자열 변경

    - s.replace(old, new[,count]) : 바꿀 대상글자를 count 만큼 새로운 글자로 반환

    - s.strip() : 특정한 문자 지정 - 공백 제거

    - s.split() : 특정한 단위로 나눠 리스트 반환

    - seperator.join([iterable]) : 반복 가능한 컨테이너 요소를 합쳐

## 리스트 

- 변경 가능한 값들의 나열

- 문법

    - .append(x) : 마지막에 추가

    - .insert(i, x) : index i에 x 삽입

    - .remove(x) : 가장 첫 번째 x 제외

    - .pop(i) : i에 있는 항목 반환 후 제거

    - .clear() : 모든 항목 삭제

    - .index(x) : x 값을 찾아 해당 index 값 반환

        - 예시) 
        ```python
        numbers = [1, 2, 3, 4]
        print(numbers.index(3))  # 2
        ```

    - .reverse() : 거꾸로 ([::-1])

    - .sort() 정렬

        list.sort() : 원본 자체를 변경

        sorted(list) : 원본 바꿔서 반환, 원본 변경 x
    
    - .count(x) : x 몇 개 존재

## 세트

- 세트 메서드

    - .copy()

    - .add()

    - .pop() : 랜덤하게 항목을 반환

    - .remove(x) : x가 세트에 있을 경우 삭제

    - s.update(t) : 세트 t에 있는 모든 항목 중 s에 없는 항목 추가

## 딕셔너리

- 키-값 (key-value) 쌍으로 이뤄진 모음

- 키와 값은 ':' 로 구분, 개별 요소는 ','로 구분

- 문법

    - d.keys() : 모든 키 반환

    - d.values() : 모든 값 반환

    - d.get(k) : 키 k의 값을 반환. 키 k가 딕셔너리 d에 없을 경우 None 반환

    - d.pop(key[default]) : key가 딕셔너리에 있으면 제거하고 해당 값 반환

    - d.update([other]) 

        ```python
        my_dict['apple'] = '사라'
        ```

# 정리

- 시퀀스

    - 문자열 (string) : 문자의 나열 (변경 불가)

    - 리스트 (list) : 변경 가능한 값의 나열

    - 튜플 (tuple) : 변경 불가능한 값의 나열

    - 레인지 (range) : 숫자의 나열 (변경 불가)

- 컬렉션 

    - 세트 (set) : 중복 없는 값의 모음

    - 딕셔너리 (dictionary) : 키-값의 모음