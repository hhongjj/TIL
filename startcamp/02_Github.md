# Github



### 원격 저장소 (remote repository)

1. 로컬 git 저장소 준비
2. Github repository 생성



### 원격 저장소 주소 추가

```python
$ git remote add origin 저장소url
```

> git 원격 저장소(remote)를 추가해줘(add) origin(원격 저장소 이름) 이라는 이름으로 저장소 URL을!



### 원격 저장소 목록 보기

```python
$ git remote -v
```

> 잘못 add 한 경우 삭제하기 $ git remote rm origin



### 원격 저장소에 업로드 (push)

```python
$ git push - u origin master
```

> git! push해줘 origin 이라는 이름의 원격저장소에 master브랜치로!

> 원격 저장소에는 commit이 올라간다. 즉, commit 이력이 없다면 push 할 수 없다
>
> 두번째 push 부터는 `u` 생략 가능



### pull

- 원격 저장소의 변경사항을 받아옴(업데이트)

```python
 $ git pull origin master
```



### clone

- 원격 저장소 전체를 복제

```python
$ git clone 저장소URL
```

> 주의!! clone 받은 프로젝트는 이미 git init 되어있음 (remote도 추가되어 있음)



## 순서!!

- `git add + git commit + git push`

```python
$ git add .
$ git commit -m "추가"
$ git remote add origin {url}
$ git push origin main
```

