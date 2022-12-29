
#### 12월 29일
---

### GitHub Profile README 만들기

 1. 프로필 폴더 만들고 README.md 파일에 자기소개 작성

 2. Git 버전 만들기

 3. GitHub 원격저장소 만들기 

    ※ 저장소 이름은 본인 GitHub username 이어야 함

## Branch 

: 독립적인 작업 흐름을 만들고 관리

### 주요 명령어

1. 브랜치 생성

    (master) $ git branch *{branch name}*

2. 브랜치 이동 

    (master) $ git checkout *{branch name}*

3. 브랜치 생성 및 이동

    (master) $ git checkout -b *{branch name}*

4. 브랜치 삭제

    (master) $ git checkout -d *{branch name}*

5. 브랜치 목록

    (master) $ git branch -d *{branch name}*


## Git Flow

- Git을 활용하여 협업하는

- 각자 독립된 버전의 흐름을 만들 수 있다.

## 기본 원칙

1. master branch 는 반드시 배포 가능한 상태

2. feature branch 는 각 기능의 의도를 알 수 있게 작성

3. Commit message 는 매우 중요☆ 명확하게 작성

4. Pull Request 를 통해 협업 진행

5. MERGE !

---

> Q.  a.txt 파일만 커밋 하려고 했는데 git add . 해버렸어요

    A. $ git restore --staged b.txt

> Q. 실수로 x 눌렀는데 어떻게 하나요 ?

    A. $ git restore 파일명 : 이전 내용
        restore stage : add 한 내용 돌리기

> Q. commit 메세지 실수했어요.

    A. $ git commit --amend
        BUT 아예 다른 버전이 되어버림.