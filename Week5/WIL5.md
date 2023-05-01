# 기초 웹 스터디 5주차

- css(cascading style sheet) : HTML의 각 요소의 style을 정의해 화면 등에 어떻게 렌더링 하면 되느지 브라우저에게 설명하기 위한 언어
- cascading : 위에서 아래로 내려가는 like 폭포
1. 상속 : 수많은 html 태그는 부모의 스타일을 자식에게 상속 할 수 있다.

ex.

div style = “ color : red”

<div>

<div>

똑같은 style 적용(상속) → red

</div>

</div>

1. 우선순위
- 스타일 시트
    - 브라우저 기본 스타일
    - 사용자 스타일
        - 인라인 스타일
        - 내부 스타일 시트
        - 외부 스타일 시트

1) 사용자 스타일(컴퓨터 사용자) : 내 컴퓨터 기본 브라우저 스타일 적용

ex. 윈도우 : 설정 - 고대비

2) 제작자 스타일(개발자) : css 문서에 코딩 해놓은 것

3) 브라우저 기본 스타일 : css 까먹고 무언가를 처리 안했을 경우 방지 

- 만약 두가지 서열이 충돌한다면?(서열이 같다면)

→ 세부적인 설정으로 결정, selector를 통해 지정

- improtant → property value
- 인라인 스타일 : 줄 안에 쓴 style, 전체 스타일 적용되어 있어도 인라인 스타일을 쓰면 인라인 스타일이 적용됨
- id 스타일
- 클래스 스타일
- 타입 스타일 : 태그 스타일

- selector : head안에 style 태그를 넣으면 body에 알아서 적용됨
    - h1 {color: red; font-size: 12px;}
        - h1 : selector(선택자)
        - color, font-size : property(속성)
        - red, 12px : value(값)
        - colo: red; , font-size: 12px; : 선언
        - {color: red; font-size: 12px;} : 선언블록

1. id 선택자 : #아이디(속성: 값, …) 특정 아이디를 가진 요소에 적용
2. 클래스 선택자 : .클래스(속성: 값,…) 특정 클래스를 가진 모든 요소에 적용, 두 가지 클래스를 한 가지 태그에 중복 적용 가능
3. 타입 선택자 : 태그(속성: 값,…) 특정 태그를 사용한 모든 요소에 적용 ex. div
4. 전체 선택자 : *(속성: 값,…) 문서의 모든 요소에 적용
5. 어트리뷰트 선택자 : 선택자[속성: 값]

외부 스타일 시트 : <link rel =” “ href = “ “> → 이 문서와 다른 문서와의 관계를 설명할 떄 스임

→ 상속, 우선순위가 있기 때문에 cascading이라는 단어가 붙음 

[https://poiemaweb.com/](https://poiemaweb.com/)