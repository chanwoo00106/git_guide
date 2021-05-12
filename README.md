# Git_Guide


# 추가와 확정
변경된 파일을 아래의 명령어로 추가할 수 있다

> git add <파일이름>

그리고 변경된 파일을 확정하려면 아래 명령어를 입력

> git commit -m "이번 확정본에 대한 설명"

이렇게 하면 변경된 파일이 <strong>HEAD</strong>에 반영이 됨

# 커밋 취소

아래와 같이 적어주면 가장 최근 커밋을 취소해 준다

> git log HEAD^

가끔 가다 '^' 문자를 필터링 하는경우가 있어서 아래와 같이 적어준다

> git reset --soft HEAD~1

또는

> git log "HEAD^"

# 변경된 내용 올리기

현재 변경된 내용은 아직 로컬 저장소에 있어서
이 내용을 github에 올려준다

> git push origin master

생성한 github와 연동하기 위해서는 먼저 해당 원격 저장소를 프로젝트에 등록시켜야한다

*origin: 원격 저장소의 주소

*master: 현재 브랜치

→ git push origin master의 뜻은 대략

"내가 등록한 원격 저장소(origin)안에서 master 브랜치로 push하겠다" 로 해석할 수 있다

(브랜치는 git에서 협업, 버전 관리를 위해 '가지'를 따서 작업할 때 사용되는 개념이다)

> git remote add <등록 이름(대부분 origin으로 함)> <원격 저장소 주소>

이렇게 명령어를 사용하면 내PC의 로컬 git 프로젝트와 원격 저장소가 연동된다

[더 자세한 내용](https://rogerdudler.github.io/git-guide/index.ko.html)
[더 자세한 내용2](https://webdevtechblog.com/%EA%B9%83%ED%97%88%EB%B8%8C-%EC%82%AC%EC%9A%A9%EB%B0%A9%EB%B2%95-github-tutorials-4a63f31bb6a5)

# 기존 저장소에 올리는 법

> git remote add origin <주소>

> git branch -M master

> git push

---
주소를 적다 갑자기 아래와 같은 오류가 뜰 수 있는데

```
fatal: remote origin already exists.
```

이건 이미 remote가 되어 있어서 그런다.
remote를 취소하고 다시 주소를 add해주면 된다

> git remote rm origin

---
가끔가다 기존 파일이 손상돼서 막는 경우가 있는데
그건 아래와 같이 강제 커밋을 하면 된다

> git push origin +master
