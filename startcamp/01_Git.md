# Git

- Git : 분산 버전 관리시스템
- github : 서비스 제공자



### Git Basic

#### 로컬 저장소 설정

` $ git init `

- 폴더에 git 저장소를 초기화하면,
  - `.git` 숨김 폴더가 생기고
  - bash에는 `(master) `  라고 표기된다.

> 주의사항!! git 저장소 내에 또 다른 git 저장소를 만들면 안됨! git init 명령어를 입력할 때, (master)가 있으면 절대 입력하지 말 것!



------

##### working directory                     staging area                                  commit                              github

​              수정     -------git add---->>   임시 공간  -------git commit ->>    ver   ------git push --->>

------

### add

> staging area / INDEX

```python
$ git add 파일명
$ git add .               # 현재 디렉토리 (하위 디렉토리)
$ git add a.txt           # 특정 파일
$ git add my_folder/      # 특정 폴더
```

-  `working directory ` 상태의 파일을 `staging area`상태로 변경
- 커밋을 위한 파일 및 폴더들을 추가하는 명령어
- 모든 정보는 `git status ` 에 있다.

### commit

```python
$ git commit -m "first commit"      # 커밋할 때 메세지 남기기 
$ git log                           # 커밋 목록 확인
$ git log --oneline                 # 커밋 목록 한 줄로 확인
```

### status

-  working directory, staging area 공간의 파일 상태를 확인할 수 있다. 

```
$ git status
```

### git show

- 현재 커밋의 변경 기록 확인하기

### git diff 커밋아이디1 커밋아이디2

- 커밋들 사이에 변경 사항을 확인할 수 있음

```python
# git diff 9b15 539d
```

### gitignore

> git으로 관리하고 싶지 않은 파일들의 리스트를 작성하여, 특정 파일들을 git이 버전 관리를 하지 않도록 하는 것

- 일반적으로 개인정보 및 특정 사람에게만 적용되는 환경들(개인 개발환경 관련)이 이 파일에 작성됨
- 개발환경 관련 파일들(.idea 등)은 버전관리가 될 필요도 없을 뿐더러, 개인정보 같은건 애초에 GitHub에 올라가서는 안됨.
- `.gitignore`파일을 만들어서 관리(위치는 `.git `파일과 동일한 곳)
- http://gitignore.io/
  - 본인 개발 환경에 대한 내용을 넣고 생성하면, 일반적으로 개발자들이 많이 쓰는 gitignore 문서를 제공

> 일반적으로 git init 후 첫 add 전 작성할 것!

