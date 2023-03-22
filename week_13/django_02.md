# Django template system

: 데이터 **표현**을 제어하면서, **표현**과 관련된 로직을 담당

## DTL Syntax

1. Variable (변수)

    **{{ variable }}**

    - view 함수에서 render 함수의 세 번째 인자

    - dictionary type 으로 받음

    - e딕셔너리 key에 해당하는 문자열이 template에서 사용 가능한 변수

    - dot(.)을 사용하여 변수 속성 접근

2. Filters

    **{{ variable | filter }}**

    - 변수를 수정할 대

    - {{ name | truncatewords : 30 }}

3. Tags

    **{% tag %}**

    - 출력 x

    - 반복, 논리를 수행하여 제어 흐름 만드는 등 변수보다 복잡한 일 수행

    - 일부는 시작, 종료 태그 필요 {% if %} {% endif %}

4. Comments (주석)

    - {# name #}

    - {#comment#} {% endcomment %}

## 새로운 페이지 코드 작성

1. url

2. view

3. template

- 검색할 때 : google에 django document + 주제 

- skeleton 역할 템플릿 (부트스트랩)

  - base.html

  - {%block ~~~}

  - 'extends' tag : {% extends 'path' %}

    *반드시 템플릿 최상단에 작성 되어야 함!*

  - 'block' tag : {% block name %}{% endblock name %}

---

1. Throw 뷰 함수

    - form 태그를 출력하는 템플릿을 응답

2. Catch 뷰 함수

    - throw 페이지에서 보낸 요청을 받고

    - 사용자 입력 데이터를 찾고

    - 찾은 데이터를 템플릿에 변수로 넣어서 응답 

=>

      1. /throw/ 주소로 요청을 보냄

      2. django는 /throw/ 주소에 맞는 throw 뷰 함수를 호출 (응답)

      3. 유저는 /throw/ 서버에 django의 응답결과 (throw 페이지)를 받음

      4. input 에 데이터를 입력하고 제출 (action 주소로 요청을 보냄)

      5. action 주소는 /catch/고, /catch/ 로 django 에 요청을 보냄

      6. django 는 /catch/ 주소에 맞는 catch 뷰함수를 호출 (응답)

      7. 유저는 django의 응답결과 (catch 페이지)를 받음