# Git_Guide


# 추가와 확정
변경된 파일을 아래의 명령어로 추가할 수 있다

> git add <파일이름>

그리고 변경된 파일을 확정하려면 아래 명령어를 입력

> git commit -m "이번 확정본에 대한 설명"

이렇게 하면 변경된 파일이 <strong>HEAD</strong>에 반영이 됨

# 변경된 내용 올리기
현재 변경된 내용은 아직 로컬 저장소에 있어서
이 내용을 github에 올려준다

> git push origin master

생성한 github와 연동하기 위해서는 먼저 해당 원격 저장소를 프로젝트에 등록시켜야한다

> git remote add <등록 이름(대부분 origin으로 함)> <원격 저장소 주소>

이렇게 명령어를 사용하면 내PC의 로컬 git 프로젝트와 원격 저장소가 연동된다

[더 자세한 내용](https://rogerdudler.github.io/git-guide/index.ko.html)
