# Django Model

  1. 새로 만든 app/ => models.py

      ```python
      class 모델이름(models.Model)
        
        title = models.CharField(max_length=10)
        completed = models.BooleanField(default=False)
        priority = models.IntegerField(default=3)
        created_at = models.DateTimeField(auto_now_add=True)
        deadline = models.DateTimeField(null=True)
        category = models.CharField(max_length=20)
      ```
  
  2. $ python manage.py makemigrations

      => 0001.initial~~~ 생김

  3. $ python manage.py migrate

      => DB 내에 테이블 생성

  4. $ python manage.py createsuperuser

      => 관리자 계정 만들기

  5. 새로 만든 app/ => admin.py 에 추가

      ```python
      from .models import 모델이름

      admin.site.register(모델이름)
      ```
