# 기초 웹 스터디 3주차

**git branch**

- branch : 포인터, 처음 이름 → master
- HEAD : 지금 내가 보고 있는 공간 가르키는 포인터
- TESTING : 가장 마지막 commit을 가르키는 포인터

```c
$git branch testing \ testing이라는 이름의 branch 만든다.
$git checkout testing \ testing branch로 옮겨간다.
$git branch \ 모두 볼 수 있다.
```

**merge와 conflict**

```c
$git merge master / master->hotfix, fast-forward 전략
```

- 3ways merge 전략 : 새로운 commit이 생김
- conflict : 3개를 비교하는데 충돌이 있음

**깃플로우와 메시지 컨벤션**

- 깃플로우 : branch들을 하나 하나 관리(feature branches, release branches…)
- 메시지 컨벤션
    - 제목 → “태그: 제목”, 첫 글자는 대문자, 50자 이내, 개조식 구문
        - 기능
            - Feat : 새로운 기능 추가
            - Fix : 버그 고친 경우
            - Design : CSS등 사용자 UI 디자인 변경
        - 개선
            - Style : 코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우
            - Refactor : 프로덕션 코드 리팩토링
        - 그 외
            - Docs : 문서를 수정한 경우
            - Test : 테스트 추가, 테스트 리팩토링
            - Chore : 빌드 테스트 업데이트, 패키지 매니저를 설정하는 경우
    - 본문 → 한 줄 당 72자 내, 최대한 상세히, 무엇을 왜 변경했는지 설명
    - 꼬리말 → “유형: #이슈번호”, optional, 이슈 트래커 id 작성
        - Fixes : 이슈 수정 중(아직 해결X)
        - Resolves : 이슈를 해결했을 때
        - Ref : 참고할 이슈가 있을 때
        - Related to : 해당 커밋에 관련된 이슈번호(아직 해결X)