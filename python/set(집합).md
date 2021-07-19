### set(집합)

> 집합명 = set([원소1,원소2,...])

- 중복 안됨, 순서 없음.
- 인덱스로 접근 불가
- | 기호를 사용해서 합집합 구할 수 있음.

- & 기호를 이용해 교집합 구할 수 있음

```python
prime={2,3,5,7}
odd={1,3,5,7}

print(prime | odd)      #{1,2,3,5,7}
print(prime&odd)        #{7}
```

- 1개의 원소 추가 => add
- 여러개의 원소 한번에 추가 => update

```python
prime={2,3,5,7}
prime.add(11)  

print(prime)                  #{2,3,5,7,11}

prime.update([11,13,17])

print(prime)                  #{2,3,5,7,11,13,17}
```

- 삭제는 remove

```python
prime={2,3,5,7}
prime.remove(2)

print(prime)                  #{3,5,7}
```

