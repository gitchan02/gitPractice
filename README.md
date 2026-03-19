# Git 사용해보기

## github에 내 프로젝트 연동하기
### at Github.com
1. git repository 생성
2. 해당 레포지토리의 주소 파악 및 저장
 - https, ssh 중 필요한 것을 고르면 된다
 - 만약 cli환경에서 한다면 ssh주소를 통한 접근이 가능하다
 - https의 경우 주소의 구성은 아래와 같다
```
https://github.com/[UserID]/[git repository name].git
```
 - ssh의 경우 주소의 구성은 아래와 같다
```
git@github.com:[UserID]/[git repository name].git
```

### at Working Directory
0. git 설치
    - Window (git을 사이트 가서 잘 찾아서 해야만함)
    - Mac (homebrew를 사용하자)
    - Linux (사실 리눅스 설치할때 어지간하면 포함 가능)
    - Android - termux (이걸 쓰면 조언이 필요 없지)
1. change directory
   - cd를 통한 접근
   - IDE를 통한 접근
      - 새 프로젝트 생성도 기존 프로젝트에서도 가능
2. git init
   - .git 이라는 숨겨진 디렉토리의 생성을 확인 가능하다
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
- 물론 진짜 프로젝트면 .gitignore 먼저 잘 설정하고 와야한다
gitignore.io [https://www.toptal.com/developers/gitignore]

## git branch 사용 예시
### 개인 디바이스에서
```shell
git branch [branch_name]
git checkout [branch_name]
# 작업
git add [작업물]
git commit -m "[작업내용]"
git push origin [branch_name]
```

### 깃허브에서
1. 해당 브랜치를 머지하려는 사람이 풀 리퀘스트 요청
2. 리뷰 남기기
   - 코드에 대한 리뷰
   - 전체적인 리뷰
3. 머지

```shell
git branch dev
git branch [new branch] [from branch]
git push origin [new branch]
```

## 추가될 내용
- 추가적인 name, email 설정 방법
