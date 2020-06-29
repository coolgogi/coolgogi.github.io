---
title: "Github_study1"
date: 2020-06-30 02:24 +0900
categories: study
---
오늘은 git에 대해서 공부했습니다.

git을 사용하는 이유는 크게 3가지가 있습니다.
1. version
2. backup
3. collaboration

1. version
문서를 혼자서 관리한다면 git을 사용할 필요가 없겠으나, 여러 명에서 같이 관리한다면
복잡하기 때문에 git을 사용하는 것이 좀 더 좋을 것입니다.

2. backup
문서를 한 컴퓨터에만 저장해놓는 것은 위험하기 때문에 backup을 해둡니다.
개인이 server를 만들어 backup을 해도 되지만 개인이 server를 만들기는 힘들기 때문에 다른 곳에서 제공해주는 서비스를 사용합니다.
git hosting service는 github에서도, gitlab 등등 다양한 곳에서 제공해주는데, 가장 유명한 것이 지금 보고계시는 github입니다.

3. collaboration
다른 사람과의 협업을 편하게 해주는 것이 git 입니다. 저도 이번 여름방학에 프로젝트를 해보려고 git을 배운 것입니다.

git을 사용하는 방법은 TortoiseGit, SourceTree 등의 프로그램을 사용해도 되지만, CLI를 이용해서 git을 다뤄보려고 합니다.


Version
version이 저장되는 곳을 Repository라고 하고 version으로 만들어 지기 전 단계를 Working Tree라고 합니다. 그리고 version으로 만들어진 것들을 Staging Area 라고 합니다.
단순히 개인이 작업을 하면 Working Tree에 있고, git add를 통해 staging area로 올려서 git commit을 하게되면 Repository에 저장됩니다.

Create - git init
Read - git pull, 
Update - git add, git commit, git push, git merge, 
Delete - git reset, git revert
명령어
git init : (git으로 관리하겠다는 명령어 .git이 생깁니다. ls -al로 확인가능)
git add : working tree에 있는 것들을 staging area로 저장합니다.
git commit : staging area에서 repository로 저장합니다.
git diff : ??
git status : 현재 상태를 알려줍니다. commit 할 것이 있는지 working tree의 상태, HEAD 위치 등등
git log : 지금까지 한 commit을 보여줍니다. 
git checkout ID : git log로 확인한 id로 넘어갑니다. 또 ID 자리에 다른 branch 이름을 넣으면 그 branch로 넘어갑니다.

git reset ID : ID 이후의 commit을 삭제하고, ID로 되돌아 갑니다.
git revert ID : ID commit 당시의 변경점을 되돌립니다. (만약 5에서 2로 가고싶다면 revert 5, 4, 3 순차적으로 해야함)

git branch : branch 목록을 보여줍니다.
git branch "name" : branch를 추가합니다.
+ git checkout

git merge 

3 way merge

mergetool : p4merge

git remote add origin URL

작업할 때 순서
git pull
작업
git add
git commit
git push

git push -u origin master


충돌을 피하려면 -> 자주 pull하고, push하고, update 확인


patch?

pull request -> open source에서 push 권한이 없는 사람이 요청하는 것
