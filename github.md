
분산버전관리 시스템(DVCS)

- 원격 저장소(remote repository)를 활용하여 협업
    -GitHub 활용

# 원격 저장소 활용

> Push
    
    - 로컬 저장소의 버전을 원격 저장소로 보낸다
    - $ git push

> Pull

    - 원격 저장소의 버전을 로컬 저장소로 가져온다 
    - $ git pull <원격 저장소 이름> <브랜치 이름>

**git remote add origin http://github.com/ GitHub Username / 저장소 이름**

    이름의 글로벌 룰 : 원격 저장소 기본 이름으로 많이 쓰는 것 => origin

**Q**
GitHub에 올리고 로컬에서 파일을 지우면 사라지나요 ?
**A**
실제 상태를 add, commit 하기 때문에 로컬에서 삭제 후 commit -> push 하면 사라짐

> Clone

    - 저장소 자체를 가져오는 행위
    - 다운로드(zip) : (가장 최신 버전 상태의) 파일만 받는 것
    - clone : git 저장소를 받아오는 것, 모든 버전을 받은 것

    - Pull 과의 차이점 :
        clone 은 원격 저장소를 복제한 것이고, pull은 원격 저장소의 커밋을 가져오는 것



## 명령어 정리

    git clone <url> : 원격저장소 복제

    git remote -v : 원격저장소 정보확인

    git remote add <원격저장소> <url> : 원격저장소 추가 (일반적으로 origin)

    git remote rm <원격저장소> : 원격저장소 삭제

    git push <원격저장소> <브랜치> : 원격저장소에 push

    git pull <원격저장소> <브랜치> : 원격저장소에 pull


> git ignore
   
    - 버전 관리랑 상관 없는 파일은 관리하지 x

    - 관리 안 하고 싶을 때 ? => .gitignore 안에 넣어버리기
        - *.pptx : pptx 로 끝나는 모든 파일 
    
    - 이미 commit 한 경우 ? => 무시 x , 미리 .gitignore 를 설정하기 !

