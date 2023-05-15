# 기초 웹 스터디 7주차

### **클론 코딩**

**구획**

![클론 구현페이지](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week7/%ED%81%B4%EB%A1%A0%20%EA%B5%AC%ED%98%84%ED%8E%98%EC%9D%B4%EC%A7%80.png)

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