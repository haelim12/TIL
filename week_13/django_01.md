## 앱 생성

  1. $ python manage.py startapp articles

  2. setting.py -> INSTALLED APPS = [ ~ ] 에 'articles' 추가

- MVC 디자인 패턴

  - Model, View, Controller

  - 어플리케이션을 구조화 하는 대표적인 패턴

- MTV 디자인 패턴

  - Model, Template, View

  - Django 에서 어플리케이션을 구조화 하는 패턴

- 프로젝트 구조 (firstpjt/)

  - 사용하는 파일 : settings.py, urls.py

- 앱 구조 (articles/)

  - 사용하는 파일 : admin.py, models.py, **views.py** 

  - **views.py** : 모델, url 등 과의 control (요청 처리/응답)

- 메인 페이지 :

  - http://127.0.0.1:8000/articles/

  - firstpjt/ -> url.py

  - 앱 폴더 (articles) 안에 templates 폴더 만든 후 url, view 등에 저장 