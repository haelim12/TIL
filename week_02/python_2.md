
## π String Formatting

- f-string
    
    print(f'{name}λ {age}μ΄μλλ€.')

    print(name + 'λ' + str(age) + 'μ΄μλλ€.')

    print('{}λ {}μ΄μλλ€.'.format(name, age))

## π ν λ³ν

### μλ£ν λ³ν (Type Casting)

- μμμ  ν λ³ν
    
    - νμ΄μ¬μμ λ΄λΆμ μΌλ‘ μλ£ν λ³ν

    - True + 3  # 4

    - 3 + 5.0  # 8

    - 3 + 4j + 5  # 8 + 4j

- λͺμμ  ν λ³ν

    - str, float => int
        
        int('3') + 4  # 7
    
    - str, int => float

        float('3.5') + 5  # 8.5
    
    - int, float, list, tuple, dict => str

---

κ°μ²΄ (Object) νμ©νκΈ° μν΄ **Type** κ³Ό μ°μ°μ

νμ΅ λͺ©ν :  
    
    **μ‘°κ±΄λ¬Έ, λ°λ³΅λ¬Έ** μ νμ©ν΄ μ½λλ₯Ό μμ±νκ³  λ¬Έμ  νμ΄μ μ μ©

    β­μ€μ²©λ μ‘°κ±΄λ¬Έκ³Ό λ°λ³΅λ¬Έμ κ²°κ³Όλ₯Ό νλ¨

---

## π μ μ΄λ¬Έ

- νμ΄μ¬μ μ -> μλ λ‘ μμ°¨μ μΌλ‘ λͺλ Ή μν

- μ½λλ₯Ό μ νμ μΌλ‘ μ€ννκ±°λ λ°λ³΅νλ μ μ΄κ° νμ

- μμλ (flow chart) λ‘ ννμ΄ κ°λ₯

## π μ‘°κ±΄λ¬Έ

- μ°Έ(κ±°μ§) μ νλ¨ν  μ μλ μ‘°κ±΄μκ³Ό ν¨κ» μ¬μ©
    
    - λΉκ΅ μ°μ°μ νμ©

- ``` python
    if ~ :
        ~
    else :
         ~
    # λ€μ¬μ°κΈ° 4μΉΈ space

- μμ) 
```python
    num = int(input("μ«μλ₯Ό μλ ₯νμΈμ > "))
    if num % 2 ==0 :
       print("μ§μ")
    else :
        print("νμ")
```
```python
    num = int(input())
    if num % 2 ==1 :
        print("νμ")
    else :
        print("μ§μ")
```

### λ³΅μ μ‘°κ±΄λ¬Έ

- elif νμ©

### μ€μ²© μ‘°κ±΄λ¬Έ

## π λ μΈμ§(range)

- λ²μ λνλΌ λ

- μ«μμ μνμ€
    
    - range(n): 0 ~ n-1 

    - range(n, m) : n ~ m-1

    - range(n, m, s) : n ~ m-1 κΉμ§ s λ§νΌ μ¦κ°

        μμ) 0 λΆν° -6 : range(0, -6, -1)

## π λ°λ³΅λ¬Έ

- whileλ¬Έ, forλ¬Έ, λ°λ³΅λ¬Έ μ μ΄

### for λ¬Έ

- μνμ€(string, tuple, list, range) λ₯Ό ν¬ν¨ν μνκ°λ₯ν κ°μ²΄ (iterable)

- λ³μμ μ΄λ¦μ κ°κ° λΆμ¬μ€

### λ°λ³΅λ¬Έ μ μ΄

- break : λ°λ³΅λ¬Έ μ’λ£

- continue : λ€μ λ°λ³΅ μν

- for-else : λκΉμ§ λ°λ³΅λ¬Έ μ€νν μ΄ν else λ¬Έ μ€ν
