# Python

- 인터프리터 언어(Interpreter)
  - 소스 코드를 컴파일하지 않고, 한 줄씩 소스코드를 읽어서 바로 실행
  - 컴파일 언어에 비해 느릴 수 있지만 빌드 과정이 없이 바로 실행 가능함
- 객체 지향 프로그래밍(Object Oriented Programming)
  - 파이썬은 모두 객체로 이뤄져 있음

- 동적 타이핑(Dynamic Typing)
  - 변수에 별도의 타입 지정이 필요 없음



### 주석(Comment)

- 한 줄 주석은 #으로 표현한다.

- 여러 줄의 주석은 한 줄씩 #을 사용하거나, """ 또는 '''으로 표현한다.

  > 여러 줄 주석 : 드래그 후 `ctrl+/`

- 다만 """ 또는 '''으로 표현하는 방법은 docstring을 위해 사용한다.

  > 특수한 형태의 주석 - docstring
  >
  > 함수/클래스의 설명을 작성



### 변수

- 변수는 할당 연산자(=)를 통해 값을 할당(assignment)
- `type()`
  - 변수에 할당된 값의 타입
- `id()`
  - 변수에 할당된 값(객체)의 고유한 아이덴티티(identity) 값이며, 메모리 주소



### 할당 연산자(=)

- 같은 값을 동시에 할당할 수 있음

```python
x = y = 1004
print(x, y)
```

1004 1004

- 다른 값을 동시에 할당 할 수 있음(muliple assignment)

```python
x, y = 1, 2
print(x, y)
```

1 2



### 값 swap

- 임시 변수 활용

```python
x, y = 10, 20
tmp = x
x = y
y = tmp
print(x, y)
```

20 10

- Pythonic

```python
x, y = 10, 20
y, x = x, y
print(x, y)
```

20 10

