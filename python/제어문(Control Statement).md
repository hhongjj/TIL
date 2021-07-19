# 제어문(Control Statement)

- 파이썬은 기본적으로 위에서부터 아래로 순차적으로 명령을 수행
- 특정 상황에 따라 코드를 선택적으로 실행(분기/조건)하거나 계속하여 실행(반복)하는 제어가 필요함
- 제이문은 순서도(flow chart)로 표현이 가능



## 조건문(Conditional Statement)

- if문은 참/거짓을 판단할 수 있는 조건식이 함께 사용
  - expression에는 참/거짓에 대한 조건식
  - 조건이 참인 경우 이후 들여쓰기 되어있는 코드 블럭을 실행
  - 이외의 경우 else 이후 들여쓰기 되어있는 코드 블럭을 실행
    - else는 선택적으로 활용 가능함

```python
if <expression>:
    # Code block
else:
    # Code block
```

> 들여쓰기 주의할 것! - PEP8에서 권장하는 4space 사용(1 tab)

### 복수 조건문

- 복수의 조건식을 활용할 경우 elif를 활용하여 표현함

```python
if <expression>:
    # Code block
elif <expression>:
    # Code block
elif <expression>:
    # Code block
else:
    # Code block    
```

### 중첩 조건문(Nested Conditional Statement)

- 조건문은 다른 조건문에 중첩되어 사용될 수 있음
  - 들여쓰기를 유의하여 작성할 것

```python
if <expression>:
    # Code block
    if <expression>:
        # Code block
else:
    # Code block
```

### 조건 표현식(Conditional Expression)

- 조건 표현식을 일반적으로 조건에 따라 값을 정할 떄 활용
- 삼항 연산자(Ternary Operator)로 부르기도함

`<true인 경우 값> if <expression> else <false인 경우 값>`

``` python
num = 2
if num % 2:
    result = '홀수입니다'
else:
    result = '짝수입니다.'
print(result)

#조건 표현식
result = '홀수입니다.' if num % 2 else '짝수입니다.'

#절대값을 저장하기 위한 조건표현식 코드
value = num if num >= 0 else -num
```

> 할당은 한번만 한다!



## 반복문 (Loop Statement)

- while문 
  - 종료조건에 해당하는 코드를 통해 반복문을 종료 시켜야함
- for 문
  - 반복가능(iterable)한 객체를 모두 순회하면 종료 (별도의 종료조건이 필요 없음)
- 반복 제어
  - break, continue, for-else



### while문

- while문은 조건식이 참인 경우 반복적으로 코드를 실행 

  > 조건이 False가 될 때까지 반복

  - 조건이 참인 경우 들여쓰기 되어 있는 코드 블록이 실행됨
  - 코드 블록이 모두 실행되고, 다시 조건식을 검사하며 반복적으로 실행됨
  - while문은 무한 루프를 하지 않도록 종료조건이 반드시 필요

```python
while <expression>:
    # Code block
```

```python
# 값 초기화
n= 0
total = 0
user_input = int(input())          # 5

# 반복문
while n <= user_input():
    total += n
    n += 1
print(total)                      # 15
```



### for문

- for문은 시퀀스(string, tuple, list, range)를 포함한 순회가능한 객체(iterable) 요소를 모두 순회함
  - 처음부터 끝까지 모두 순회하므로 별도의 종료조건이 필요하지 않음

```python
for <변수명> in <iterable>:
    # Code block
```

```python
chars = input()                   # happy

for char in chars:
    print(char, end =' ')         # h a p p y
```



