# list(리스트)

> a =[ ]

- list 원소 추가

  - `.append(값)` : 값을 원소 마지막에 추가

  ```python
  >>> a = [1,2,3]
  >>> a.append(4)         
  >>>a
  [1,2,3,4]
  ```

  - `.insert(index,값)` : 리스트의 index에 값 추가 

  ```python
  >>> a = [1,2,3]
  >>> a.insert(1,4)
  >>> a
  [1,4,2,3]
  ```

  - `+`  연산자로 더하기 가능

  ```python
  >>> a = [1,3,5] 
  >>> b = [2,4,6]
  >>> c = a + b            
  >>> c
  [1,3,5,2,4,6]
  >>> c += [7,8]
  >>> c
  [1,3,5,2,4,6,7,8]
  ```

  - `.extend(추가할 리스트)` : 리스트 추가

  ```python
  >>> a = [1,2,3]
  >>> a.extend([4,5,6])
  >>> a
  [1,2,3,4,5,6]
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

  

