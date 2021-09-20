# Git_Guide


# 추가와 확정

변경된 파일을 아래의 명령어로 추가할 수 있다<br>
추가를 하면 working directory 즉 내가 코드를 작성하는 폴더작성하고 있는 내용이<br>
staging area로 저장이 된다.

> git add <파일 이름>

그리고 변경된 파일을 확정하려면 아래 명령어를 치면 된다.
commit을 하면 staging area에 있는 내용이 repository로 저장이 된다

> git commit -m "이번 commit에 대한 설명"

이렇게 하면 변경된 파일이 <strong>HEAD</strong>에 반영이 됨

<img src="https://i.stack.imgur.com/naws3.png">

# 커밋 취소

`git reset`이라는 명령어가 있는데 3가지 옵션이 있다

- --hard 옵션<br>
    working directory, staging area 그리고 repository 가 모두 바뀐다. 즉 커밋 이후로 한 작업이 전부 사라진다.

- --mixed 옵션
    repository 그리고 staging area가 바뀐다.

- --soft 옵션<br>
    repository만이 원하는 커밋을 가리킴, Working directory 와 staging area는 그대로이다.

> git reset `옵션` `특정 커밋 아이디 또는 HEAD^`

위와 같은 형식으로 적으면 됨

# 변경된 내용 올리기

처음 올리는 경우에는 아래와 같이 저장소를 등록해 주고

```
git remote add origin <git 주소>
```

그다음부터는 아래와 같이만 해 주면 된다

```
git push
```

가끔 push 하다가 rejected 어쩌고 하는 오류가 뜨는데<br>
github와 local의 커밋이 달라서 뜨는 오류이다

```
git fetch
```

위와 같이 사용해서 github에 있는 파일을 가져오거나

```
git push -u origin +master
```

위와 같이 사용해서 강제로 push 하면 된다


[더 자세한 내용](https://rogerdudler.github.io/git-guide/index.ko.html)<br>
[더 자세한 내용2](https://webdevtechblog.com/%EA%B9%83%ED%97%88%EB%B8%8C-%EC%82%AC%EC%9A%A9%EB%B0%A9%EB%B2%95-github-tutorials-4a63f31bb6a5)

---

주소를 적다 갑자기 아래와 같은 오류가 뜰 수 있는데

```
fatal: remote origin already exists.
```

이건 이미 remote가 되어 있어서 그런다.
remote를 취소하고 다시 주소를 add 해주면 된다

> git remote rm origin

## branch

```
git branch
```

위와 같이 하면 branch 목록을 볼 수 있다

```
git branch <branchname>
```

이렇게 하면 branch가 생성이 되고

```
git checkout <branchname>
```
위와 같이 하면 branch를 전환할 수 있다

```
git branch -d <branchname>
```

마지막으로 위와 같이 하면 branch를 삭제 할 수 있다