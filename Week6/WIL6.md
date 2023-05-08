# 기초 웹 스터디 6주차

### <**Box model과 FLEX box>**

**BOX MODEL**

![Untitled](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week6/Untitled.png)

- content : 태그 사이에 있는 글
- padding : 충전재, 쿠션 → content와 border 사이의 간격(border 안쪽의 내부 여백)
- border : 테두리 → 모든 요소들은 박스 안에 있음, 테두리의 두께(투명이 기본)
- margin : 여백 → 어떤 요소와 요소 사이의 여백, border와 다른 요소와의 간격

![Untitled 1](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week6/Untitled%201.png)

- top → right → bottom → left 순으로 설정이 적용된다.

**FLEX BOX LAYOUT**

- flexible box layout
- 아이템이 배열될 방향인 ‘주축’을 정할 수 있다.

![Untitled 2](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week6/Untitled%202.png)

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
19. flex-direction: column;
    flex-wrap: wrap;
20. flex-flow: column wrap;