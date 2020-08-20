## Git 원격 저장소 활용

Git 원격 저장소 기능을 제공해주는 서비스는 `gitlab`, `bitbucket`, `github` 등이 있다.

## 0. 원격 저장소 설정

```bash
$ git remote add origin {url}
$ git remote add origin https://github.com/efacd/TIL.git
```

* git, 원격저장소를 추가(`add`)하고, `origin`이라는 이름으로 `url`으로 설정

  git아 원격저장소를 추가해줘 origin이라는 이름으로 url을

* 설정된 저장소를 확인하기 위해서는 아래의 명령어를 사용한다.

  ```bash
  $ git remote -v
  ```

## 원격 저장소에 `push`

```bash
$ git push origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 682 bytes | 682.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/efacd/TIL.git
   64cdbf7..e12ec76  master -> master
```

