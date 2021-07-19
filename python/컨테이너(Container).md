# 컨테이너(Container)

- 여러 개의 값을 저장할 수 있는 것(객체)
- 시퀀스(sequence)형 : 순서가 있는(ordered) 데이터
  - 순서가 있다 ! = 정렬되어 있다
  - 리스트(list), 튜플(tuple), 레인지(range), 문자형(string), 바이너리(binary)
- 비 시퀀스(non-sequence)형 : 순서가 없는(unordered) 데이터
  - 세트(set), 딕셔너리(dictionary)



## 시퀀스(sequence)

### 리스트(list)

- 리스트는 순서가 있는 시퀀스로 인덱스를 통해 접근
  - 대괄호([ ]) 혹은 list( )를 통해 생성
  - 값에 대한 접근은 list[i]
- 인덱스는 0부터 시작
- 리스트 하나에 여러개의 타입의 데이터를 저장할 수 있음

```python
a = [1,2,3]
print(a[1])    #2
a[0] = '1'
print(a)       # ['1',2,3]
```



### 튜플(tuple)

- 튜플은 수정 불가능한(immutable) 시퀀스로 인덱스로 접근
  - 소괄호(()) 혹은 tuple()을 통해 생성
  - 값에 대한 접근은 my_tuple(i)

- 튜플은 일반적으로 파이썬 내부에서 활용됨
  - multiple assignment
  - 추후 함수에서 복수의 값을 반환하는 경우에도 활용
- 하나의 항목으로 구성된 튜플은 생성시 값 뒤에 쉼표를 붙여야 함

```python
# 실제로 tuple로 처리
x, y = (1,2)
print(x, y)         #1 2

print(divmod(5,2))                 # (2,1)
quotient, remainder = divmod(5,2)
print(quotient, remainder)         # 2 1
print(type(divmod(5,2)))           # <class 'tuple'>

b = (1, )
print(type(b))                     # <class 'tuple'>
```



### 레인지(range)

- range는 숫자의 시퀀스를 나타내기 위해 사용
  - 기본형 : range(n)
    - 0부터 n-1까지의 숫자의 시퀀스
  - 범위 지정 : range(n, m)
    - n부터 m-1까지의 숫자의 시퀀스
  - 범위 및 스텝 지정 : range(n, m, s)
    - n부터 m-1까지 s만큼 증가시키며 숫자의 시퀀스

```python
range(4)                 # range(0, 4)
list(range(4))           # [0,1,2,3]
print(type(range(4)))    # <class 'range'>
list(range(1,5,2))       # [1,3]
list(range(6,1,-1))      # [6,5,4,3,2]
```

> 담겨있는 숫자를 확인하기 위하여 리스트로 형변환
>
> (실제 활용시에는 형변환 필요 없음)



### containment test

- 시퀀스 포함 여부 확인
  - in
  - not in

```python
# 리스트
1 in [3,2]               # False
# 튜플
4 in (1,2,'hi')          # False
# range
-3 in range(3)           # False
# 문자열 
'a' in 'apple'           # True
# not in
'b' not in 'apple'       # True
```



### concatenation(+)

- 시퀀스 간의 concatenation(연결/연쇄)
  - range는 TypeError 발생

```python
# 리스트
[1,2] + ['a']            #[1,2,'a']
# 튜플
(1,2) + ('a',)           # (1,2,'a')
# range
range(2) + range(2,5)    # TypeError
# 문자열
'12' + 'b'               # '12b'
```



### 시퀀스 반복(*)

- 시퀀스를 반복
  - range는 TypeError

```python
# 리스트
[0] * 8                 # [0, 0, 0, 0, 0, 0, 0, 0]
# 튜플
(1, 2) * 3              # (1, 2, 1, 2, 1, 2)
# range
range(1) * 3            # TypeError
# 문자열
'hi' * 3                # 'hihihi'
```

