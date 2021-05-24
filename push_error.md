```
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'Your github page path'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
> 원인 : fetch를 해주지 않고 push할 경우에 생김

> 해결 : git push origin +master로 해결 가능 (기존 데이터를 보장할 수 없음)
