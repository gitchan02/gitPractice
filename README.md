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

# 내가 예전에 아는 개발자분한테 배운거 추가

```markdown

## Branch & Fork
### Branch
> 현재 사용중인 환경을 복제하는 것

``` shell
# branch 생성
git branch [branch name]
# branch로 작업 공간 변경
git checkout [branch name]
# 
git push --set-upstream origin [branch name]
# branch 삭제
git branch -d [branch name]
```

snapshot을 기준으로 diff의 결과만 저장하여 branch를 많이 해도 큰 용량을 사용하지 않음 (diff하니까 피신 생각나네 ㅇㅁㅇ)

## Fork
내 계정에 레포지토리 복사해왔음 (레포지토리 상단의 Fork를 통해 생성)

원본 레포지토리와 Pull request를 통해 원본 레포지토리에 반영 가능

clone - 작성 - commit - push까지 진행 후 웹 페이지에서 Pull requests 요청
주인이 메세지, 소스코드 확인 후 저장

Pull request에 의해서만 원본이 수정되기때문에 git pull은 사용이 안됨

``` shell
git remote add upstream [원본 레포지토리 url]
git fetch upstream
git branch -r
git merge upstream/main
git push origin main
```

### Merge 충돌이 나오는 경우
(같은 영역을 여러 사용자가 수정한 경우)
수동으로 확인 후 원하는대로 작성

### 그래서?
소규모는 편한대로 해도 상관 없음
그런데 개발 인원이 몇십명인데 각자 브랜치를 따는게 좋을까? 아니면 필요한 주제로만 브랜치를 만들고 각자 자기가 작업해야하는 브랜치를 포크하는게 좋을까?를 생각해보면 후자가 좋겠죠?

## revert, rebase
> revert : 
> rebase : 
>> (이부분도 또 놓침)

상의 없이 임의로 실행하면 어마어마한 커밋 충돌이 발생

## github전략
### git flow
> 메인 개발 / 피처 토픽 / 릴리스 / 핫픽스
> 네가지 브랜치로 개발
>> main -> develop
>> develop -> feature, topic, hotfix
>> feature -> develop
>> release, hotfix -> main
>> geatyre, release, hotfix -> merge & delete

### github flow
> git flow가 복잡하다고 생각해서 나옴
> CI/CD 자동화가 되어있고 수시로 배포할 때 적합



```
