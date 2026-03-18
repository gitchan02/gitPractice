# Git 사용해보기

## github에 내 프로젝트 연동하기
### at Github
1. git repository 생성

### at Directory
0. git 설치
    - Window
    - Mac
    - Linux
    - Android - termux
1. change directory
   - cd를 통한 접근
   - IDE를 통한 접근
2. git init
3. git remote
   - try git remote -h

### 개인적인 빠른 방법
1. github에서 repository 생성
2. terminal에서 git clone을 통해 원하는 위치에 폴더 생성
3. 해당 위치에 프로젝트 생성
```shell
git add .
git commit -m "init git project"
git push
```

## git branch 사용 예시
```shell
git branch [branch_name]
git checkout [branch_name]
# 작업
git add [작업물]
git commit -m "[작업내용]"
git push origin [branch_name]
```

이후 깃허브에서 계속