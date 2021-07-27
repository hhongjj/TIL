# list(리스트)

> a =[ ]

- 순서가 있는 시퀀스, 인덱스로 접근
- 리스트의 특징
  - 변경 가능하고(mutable)
  - 순서가 있고(ordered)
  - 순회 가능한(iterable)
  - 

### 값 추가 및 삭제

#### .append(x)

- 리스트에 값을 추가함

```python
>>> a = [1,2,3]
>>> a.append(4)         
>>>a
[1,2,3,4]
```

#### .insert(i, x)

- 정해진 위치 i 에 값을 추가함

```python
cafe = ['starbucks','tomntoms','hollys']
cafe.insert(0, 'start')
print(cafe)
# ['start','starbucks','tomntoms','hollys']
```

#### .extend(*iterable*)

- 리스트에 iterable의 항목을 추가함 ( `+`연산자와 동일)

```python
a = ['starbucks','tomntoms','hollys']
a.extend(['coffee'])
print(a)
# ['starbucks','tomntoms','hollys','coffee']
a.extend('cafe')
print(a)
# ['starbucks','tomntoms','hollys','coffee','c','a','f','e']
```

- list 원소 삭제

  - `del` : 삭제

  ```python
  >>> a = [1,2,3,4]
  >>> del a[1]
  >>> a
  [1,3,4]
  ```

  - `.remove(값)` : list에서 값을 찾아 삭제, 찾을 값이 없으면 ValueError 발생

  ```python
  >>> a = [1,2,3,4]
  >>> a.remove(3)
  >>> a
  [1,2,4]
  >>> a.remove(5)
  ValueError: list.remove(x): x not in list
  ```

  

