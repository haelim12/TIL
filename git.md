# git 정리

- 저장소 생성
    $ git init : git 저장소 만들고 관리

- 버전 관리
    1. 작업을 하고
    2. 변경된 파일을 모아 (add)
    3. 버전으로 남긴다 (commit)

## git 기초 명령어

### $ git add <file>
- working directory 상의 변경내용을 staging area에 추가하기 위해 사용

### git commit -m'<커밋메세지>'
- staged 상태의 파일을 커밋을 통해 버전으로 기록

### git status
-  현재 파일 상태

### git log
- 현재 저장소에 기록된 커밋 조회
    - $ git log -1 : 최근 1개
    - $ git log --oneline : 한줄로

## git 상황들
- (1통) Untracted Files : 1.txt를 만들었지만, add를 하지 않음
- (2통) Changed to be commited : 보고서.txt를 만들고 add함
- nothing to commit, working tree clean : 모두 add, commit,한 이후 => 1통, 2통 비어있음
- Changes not staged for commit : 커밋된 적 있는 보고서.txt 파일을 수정한 상태


> 정리

git init

git add