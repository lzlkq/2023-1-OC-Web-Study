# 기초 웹 스터디 6주차

### <**Box model과 FLEX box>**

**BOX MODEL**

![Untitled](%E1%84%80%E1%85%B5%E1%84%8E%E1%85%A9%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%B3%E1%84%90%E1%85%A5%E1%84%83%E1%85%B5%206%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20b17b9f74943c468a9a4cf1e01da0a272/Untitled.png)

- content : 태그 사이에 있는 글
- padding : 충전재, 쿠션 → content와 border 사이의 간격(border 안쪽의 내부 여백)
- border : 테두리 → 모든 요소들은 박스 안에 있음, 테두리의 두께(투명이 기본)
- margin : 여백 → 어떤 요소와 요소 사이의 여백, border와 다른 요소와의 간격

![Untitled](%E1%84%80%E1%85%B5%E1%84%8E%E1%85%A9%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%B3%E1%84%90%E1%85%A5%E1%84%83%E1%85%B5%206%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20b17b9f74943c468a9a4cf1e01da0a272/Untitled%201.png)

- top → right → bottom → left 순으로 설정이 적용된다.

**FLEX BOX LAYOUT**

- flexible box layout
- 아이템이 배열될 방향인 ‘주축’을 정할 수 있다.

![Untitled](%E1%84%80%E1%85%B5%E1%84%8E%E1%85%A9%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%B3%E1%84%90%E1%85%A5%E1%84%83%E1%85%B5%206%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20b17b9f74943c468a9a4cf1e01da0a272/Untitled%202.png)

- main axis : row, 주축
- cross axis : column, 주축과 수직한 축
- justify-content : main axis
    
    align-item : cross axis
    

**Flexbox Froggy**

1. justify-content: flex-end;
2. justify-content: center;
3. justify-content: space-around;
4. justify-content: space-between;
5. align-items: flex-end;
6. justify-content: center;
align-items: center;
7. justify-content: space-around;
align-items: flex-end;
8. flex-direction: row-reverse;
9. flex-direction: column;
10. flex-direction: row-reverse;
justify-content: start;
11. flex-direction: column;
justify-content: end;
12. flex-direction: column-reverse;
justify-content: space-between;
13. flex-direction: row-reverse;
justify-content: center;
align-items: end;

18. flex-wrap: wrap;

1. flex-direction: column;
flex-wrap: wrap;
2. flex-flow: column wrap;