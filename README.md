# Git_Guide


# 추가와 확정
변경된 파일을 아래의 명령어로 추가할 수 있다

> git add <파일 이름>

그리고 변경된 파일을 확정하려면 아래 명령어를 입력

> git commit -m "이번 commit에 대한 설명"

이렇게 하면 변경된 파일이 <strong>HEAD</strong>에 반영이 됨

# 커밋 취소

아래와 같이 적어주면 가장 최근 커밋을 취소해 준다

> git log HEAD^

가끔가다 '^' 문자를 필터링하는 경우가 있어서 아래와 같이 적어준다

> git reset --soft HEAD~1

또는

> git log "HEAD^"

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

## branch 생성

```
git branch <branchname>
```

이렇게 하면 branch가 생성이 되고

```
git checkout <branchname>
```
위와 같이 하면 branch를 전환할 수 있다