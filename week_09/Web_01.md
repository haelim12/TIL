# 01.Web - Fundamental of HTML and CSS

## 1-1 Intro

- World Wide Web : 인터넷으로 연결된 컴퓨터들이 정보를 공유하는 정보공간

- Web site

- Web page - "Web site" 를 구성하는 하나의 요소
     
    - HTML : **"Structure"** - 구조

    - CSS : **"Styling"** - 페이지 구성

    - JAVA : **"Behavior"** - 동작(자동), 클릭 후 반응

## 2. Structuring the Web

HTML (HyperText Markup Language)

: 웹페이지의 의미와 구조를 정의하는 언어

- HyperText : 

    - 웹페이지 -> 다른 웹페이즈 링크

    - 한 문서 -> 다른 문서 (선형적)

- Markup Language :

    - 태그 등을 이용하여 문서나 데이터의 구조 명시하는 언어

    - HTML, Markdown

    - 프로그래밍 언어는 x

    - 예시 :

        1. HTML

            1. Hyper Text

            2. Google Effect

- 개발자 도구 여는 방법 : 마우스 오른쪽 -> 검사

### 2.2 Structure of HTML

```html
<p>My cat is very grumpy</p>

<p class= "editor-note">My cat is very grumpy</p>
```
- , 로 구분하지 않고 공백으로 구분

- 속성값은 " "로 감싸야함

```html
<html></html> : 최상위 태그
<meta> : 닫는 태그 x, 내용 x, 설정 관련 태그(속성값)
```

- alt + b : 페이지 뜨게

- a + enter : 다른 페이지 이동할 수 있는 hypertext

## Structing the WEB

```HTML
<h1>메인 제목</h1> : 최상위 제목
<h2> </h2> 
...
점점 작아짐

<ol></ol> : order list
<ul></ul> : nonorder list

<br> : 줄바꿈
```

## 3. Styling the WEB

CSS (Cascading Style Sheet)

: 웹사이트의 디자인과 레이아웃을 구성하는 언어

```html
h1 {
    color: blue;
    font-size : 15px;
}
```

### 3-3 CSS Selectors

HTML 요소를 선택하여 스타일 적용

1. 기본 선택자

    - 전채(*) 선택자

    - 요소(tag) 선택자

    - 클래스(class) 선택자 : .클래스  이릅 {~~}

    - 아이디(id) 선택자 : #id이름 {~~}

    - 속성(attribute) 선택자

2. 결합자

    - 자손 결합자 (" " (Space))

    - 자식 결합자 (>)

```html
        <p> <em> </em> </p>
```
    <p> : 부모, <em> : 자식

- Cascade : 계단식, 마지막에 나오는 규칙 적용

- Specificity : 우선순위

    - 인라인 > id 선택자 > class 선택자 > 요소 선택자