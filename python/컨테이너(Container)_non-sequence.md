# 컨테이너(Container)

- 여러 개의 값을 저장할 수 있는 것(객체)
- 시퀀스(sequence)형 : 순서가 있는(ordered) 데이터
  - 순서가 있다 ! = 정렬되어 있다
  - 리스트(list), 튜플(tuple), 레인지(range), 문자형(string), 바이너리(binary)
- 비 시퀀스(non-sequence)형 : 순서가 없는(unordered) 데이터
  - 세트(set), 딕셔너리(dictionary)



## 비 시퀀스 컨테이너

### 세트(set)

- 순서가 없는 자료구조
  - 중괄호({ }) 혹은 set( )을 통해 생성
    - 빈 세트를 만들기 위해서는 set( )을 반드시 활용해야 함
  - 순서가 없어 별도의 값에 접근할 수 없음
- 수학에서의 집합과 동일한 구조를 가짐
  - 집합 연산이 가능
  - 중복된 값이 존재하지 않음

```python
{1,2,3,1,2}               # {1,2,3}
print(type({1,2,3}))      # <class 'set'>
blank = {}
print(type(blank))        # <class 'dict'>
blank_set = set()
print(type(set()))        # <class 'set'>
```

- 집합 연산자

```python
set_a = {1,2,3}
set_b = {3,6,9}
# 차집합
print(set_a - set_b)      # {1,2}
# 합집합
print(set_a | set_b)      # {1,2,3,6,9}
# 교집합
print(set_a & set)        # {3}
```

- 세트를 활용하면 다른 컨테이너에서 중복된 값을 쉽게 제거할 수 있음
  - 단, 이후 순서가 무시되므로 순서가 중요한 경우 사용할 수 없음



### 딕셔너리(dictionary)

- key와 value가 쌍으로 이뤄진 자료구조
  - 중괄호({}) 혹은 dict()을 통해 생성
  - key를 통해 value에 접근

```python
dict_a = {}
print(type(dict_a))       # <class 'dict'>
dict_b = dict()
print(type(dict_b))       # <class 'dict'>

dict_a = {'a':'apple', 'b':'banana', 'list': [1,2,3]}
dict_a                    # {'a':'apple', 'b':'banana', 'list': [1,2,3]}
dict_a['list']            #[1,2,3]

dict_b = dict(a='apple', b='banana', list=[1,2,3])
dict_b                    # {'a':'apple', 'b':'banana', 'list': [1,2,3]}
```

- key는 변경 불가능한 데이터(immutable)만 활용 가능
  - string, integer, float, boolean, tuple, range
- value는 모든 값으로 설정 가능(리스트, 딕셔너리 등)



## 컨테이너 특징

### 컨테이너 형변환

- 컨테이너 간의 형변화은 아래와 같이 가능

|            | string |   list    |   tuple   | range |    set    | dictionary |
| :--------: | :----: | :-------: | :-------: | :---: | :-------: | :--------: |
|   string   |        |     O     |     O     |   X   |     O     |     X      |
|    list    |   O    |           |     O     |   X   |     O     |     X      |
|   tuple    |   O    |     O     |           |   X   |     O     |     X      |
|   range    |   O    |     O     |     O     |       |     O     |     X      |
|    set     |   O    |     O     |     O     |   X   |           |     X      |
| dictionary |   O    | O (key만) | O (key만) |   X   | O (key만) |            |



### 컨테이너 분류

- 변경 불가능한 데이터(immutable) 

  >  dict의 key로 사용할  수 있음

  - 리터럴(literal) - 숫자(Number), 문자열(String), 참/거짓(Bool)
  - range, tuple
  - 변경 불가능한 데이터 (immutable)의 복사
    - b = a를 하면 같은 값이 공유되며,
    - b = 10을 통해 재할당이 발생

- 변경 가능한 데이터(mutable)
  - list, set, dictionary
  - 변경 가능한 데이터(mutable)의 복사
    - num2 = num1 을 하는 경우 동일한 리스트(객체)의 주소를 참조하고 있어,
    - num2[0] = 100 으로 변경하게 되면 해당 리스트의 첫번째 원소 값이 변경됨.

![](컨테이너(Container)_non-sequence.assets/mutable.jpg)



## Summary

![](컨테이너(Container)_non-sequence.assets/summary.jpg)

