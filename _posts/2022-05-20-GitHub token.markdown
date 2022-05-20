---
layout: post
title: GitHub Push Token
date: 2022-05-20
category: GitHub
---
# GitHub Push Token
어제 Mac으로 작업 후 GitHub에 푸쉬를 했더니 UserName과 Password를 입력하라고 나왔다.     
기존 GitHub의 UserName과 Password를 입력하면 푸쉬가 진해되지 않는다.     
찾아보니 Password에 Token이라는걸 넣어야된다고 한다.
Token 생성은 간단했다.        
1. 우측 상단 프로필 클릭 > Settings > Developer Settings
2. Personal access tokens에서 Generate new token
3. repo, admin:repo_hook, gist, user, delete_repo 등 관리에 필요한 권한을 체크한다.
4. github.com 키체인 삭제
5. user 정보 입력
```
$ git config --global user.name "username"
$ git config --global user.email "email@email.com"
```
6. push하면 UserName="username", Password="token" 입력. push 끝.


