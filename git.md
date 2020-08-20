# Git 기초

> Git은 분산형 버전관리 시스템(DVCS)이다.
>
> (한줄 정의할 때는 > 를 이용한다.)

Git을 윈도우에서 활용하기 위해서는 [git bash](https://gitforwindows.org/)를 설치해야 한다.

## 1. 저장소 초기화

```bash
$ git init
($ 를 제외한 문장을 입력하면 된다.)
Initialized empty Git repository in C:/Users/i/Desktop/TIL/.git/

(master) $
```

* 로컬 저장소를 만들고 나면, `.git/`  폴더가 생성되고, bash에 `(master)`라고 표기된다.
* 반드시 저장소를 만들기 전에 원하는 디렉토리인지 확인하는 습관을 가지고, 저장소 내부에 저장소를 만들면 안된다!!
  * ex) Desktop -> git 저장소, TIL -> 다른 git 저장소 (X)

## 2. add

작업할 내용을 커밋 대상 목록에 추가한다.

```bash
$ git add .			# 현재 디렉토리 (하위 디렉토리 포함)
$ git add a.html	# 특정 파일
$ git add b.html c.html	# 특정 다수 파일
$ git add blog/			# 특정 폴더
```

```bash
# 작업 후 상태
$ git status
On branch master

No commits yet
# untracked files => Git으로 관리된 적 없는 파일 목록
Untracked files:
# commit될 것들에 포함시키기 위해서는 add 명령어를 써라
  (use "git add <file>..." to include in what will be committed)
        git.md
        markdown-images/
        markdown.md
# 총평
# commit 될 곳에 없다. (nothing)
# 하지만, 새로 생성한 파일(untracked filies)은 존재 한다.
nothing added to commit but untracked files present (use "git add" to track)

```

```bash
$ git add .
```

```bash
# add 명령어 후 상태
$ git status
On branch master

No commits yet
# commit이 될 변경사항들
# working directory X
# Staging area O
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   git.md
        new file:   markdown-images/bash.JPG
        new file:   markdown.md

```

* staging area : add는 되었고 commit을 기다리고 있는 파일들이 있는 영역

## 3. commit

```bash
$ git commit -m 'Add markdown.md'
[master (root-commit) a6cca56] Add markdown.md
 3 files changed, 94 insertions(+)
 create mode 100644 git.md
 create mode 100644 markdown-images/bash.JPG
 create mode 100644 markdown.md
```

* commit은 version(이력)을 기록하는 명령
* commit message는 해당하는 이력을 잘 나타낼 수 있도록 작성해야 한다.
* commit 이력을 확인하기 위해서는 아래의 명령어를 사용한다.

```bash
$ git log
commit a6cca562fd893608fea524d254a3c633893e6d8c (HEAD -> master)
Author: efacd <efacd@naver.com>
Date:   Thu Aug 20 14:58:10 2020 +0900

    Add markdown.md
    
$ git log -1
$ git log --oneline
a6cca56 (HEAD -> master) Add markdown.md
$ git log --oneline -1
```

```bash
$ git status
On branch master
# Working Directory X
# Staging area X
nothing to commit, working tree clean
```





















