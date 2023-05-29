# 기초 웹 스터디 9주차

### js이벤트와 DOM

**함수**

- 함수란?
    - 일정한 동작을 수행하는 코드의 집합 ex. 밥 먹는 법
    - 부분 수정이 가능하다
    - 편하다
- js에서의 함수
    - function foo(x) {
        
        return x + 10;
        
        }
        
        - function foo : foo 함수 선언
        - (x) : 매개변수 (함수 안에서 사용할 변수)
        - return : 반환
    - 매개변수(parameter) : 여러 개 선언 가능
    - 인자(argument) : 함수 호출 시 전달되는 실제 값
        
        ex. foo(10, 20, 30)
        
        → 함수를 호출할 때 인자를 넣어주면 함수 내부에서는 매개변수로 사용 가능하다.
        
    - call-by-value : 값에 의한 호출, 매개변수에 값을 복사하여 함수로 전달
    - call-by-reference : 참조에 의한 호출, 매개변수에 값이 복사되지 않고 객체의 참조값이 매개변수에 저장되어 함수로 전달
    - 이러한 코드는 어디에 사용할까?
    <script> <\script>를 body 태그의 최하단에 위치
    html parsing → script fetch, script execution(html parsing paused)
    → DOM이 다 그려진 다음에 script가 실행되는 게 좋다. 그려지기 전에 실행되면 오류가 남

**이벤트**

- 사용자가 브라우저에 일으킨 ‘사건’
    
    브라우저에 a라는 사건 발생 → b라는 일을 수행 
    
    ex. 마우스 사용 이벤트, 키보드 이벤트
    
    ![1.png](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week9/1.png)
    

이벤트 핸들러 

- on + 이벤트 이름
    
    ex. <div onclick=”handleclick()”>
    
    누르지 마세요
    
    <\div>
    

**DOM**

문서 객체 모델

html 문서의 각 항목을 계층으로 표현하여 생성, 변형, 삭제 할 수 있도록 돕는 인터페이스이다.

- dom tree

document 요소들을 tree형태로 표현한 것

ex. 

- html → root node
    - head
        - title
    - body
        - h1
        - a

하나 하나를 node 맨 위를 root node, 맨 아래를 leaf node

- node 어떻게 접근? document 객체(문서 그자체)를 통해 접근 + 선택자(id, class, 태그 등…)
- html 요소의 선택
- dom을 이용한 이벤트 처리