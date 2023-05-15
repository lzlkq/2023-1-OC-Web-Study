# 기초 웹 스터디 7주차

### **클론 코딩**

**구획**

![클론 구현페이지.png](%E1%84%80%E1%85%B5%E1%84%8E%E1%85%A9%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%B3%E1%84%90%E1%85%A5%E1%84%83%E1%85%B5%207%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20ea0d6b84c95f4fccaabeaacd2435303c/%25ED%2581%25B4%25EB%25A1%25A0_%25EA%25B5%25AC%25ED%2598%2584%25ED%258E%2598%25EC%259D%25B4%25EC%25A7%2580.png)

1. view : 전체
2. header : 헤더
3. container : header를 제외한 나머지 아래 부분
4. main-container : container 안에서 메인이 되는 부분 (video-container + video-infocontainer + comment-container)
5. aside-container : 사이드 부분
6. video-container : 영상 재생부
7. video-info-container : 영상 게시자 정보
8. comment-container : 영상 댓글

**배치**

1. view : header와 container가 flex-direction, colulmns 방향으로 배치
2. header : header 안에 각종 버튼들이 row 방향으로 배치
3. container : main-container와 asid-container가 row 방향으로 배치
4. main-container : 3개의 container가 columns 방향으로 배치
5. video-info-container : video 제목, 게시자 정보 등이 columns 방향으로 배치
6. comment-container : 댓글들이 columns 방향으로 배치