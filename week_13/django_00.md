# DJANGO 프로젝트 생성 전 (VS code)

1. 가상 환경 설정

    $ python -m venv venv

2. 가상 환경 활성화

    $ source venv/Scripts/activate

3. django 설치

    $ pip install django==3.2.18

4. 의존성 파일 생성

    $ pip freeze > requirements.txt

5. gitignore 파일 생성 

    $ .gitignore

6. git 초기화

    $ git init

7. 프로젝트 생성

    $ django-admin startproject firstpjt


## 서버 실행
---

8. django 서버 실행

    $ python manage.py runserver

9. 서버 종료

    ctrl + c