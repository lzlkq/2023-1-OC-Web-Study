# 기초 웹 스터디 1-2주차

**1주차**

- www.hongik.ac.kr를 치면 어떻게 될까? 사용자 입장에선 사이트로 이동

- 주소 :  resource가 저장된 주소

ex. 허니콤보(resource)가 있는 교촌치킨 신촌점(주소)

- URI(Uniform Resource Identifier) : resource를 식별하는 통일된 방식

ex. 허니콤보가 어디 있는지 알아내기 위한 방식

- URL(Uniform Resource Location) : ex. 교촌 치킨 신촌점
- URN(Uniform Resource Name) : ex. 도서 출판 번호

- Resource
    - HTML(자료, 뼈대)
    - CSS(UI, 살, 옷)
    - JS(제어)

→ 이 세가지 파일로 사이트를 그린다.

**2주차**

파일의 4가지 상태

- 추적X (Untracked)
- 추적O (Unmodified)
- 변경O (Modified)
- Staged

- working directory : 내 작업공간
- staging area : 가상의 공간, 변화를 쌓아두는 공간
- local repository : git에서 관리하는 저장

→ 3가지 영역을 통해서 코드 관리

**add, commit, push**

- add : working area에서 stgaing area로 옮기고 변화를 쌓아둘 수 있다.
- commit : staging area에서 commit을 하면 해당 내용들이 local repository에 올라간다.
- push : commit한 내용을 push하면 remote repository에 올려 서버에 저장할 수 있다.

**pull, fetch**

- pull : remote repository를 clone해서 local repository로 가져오면 서버에 저장되어 있는 변경사항을 pull하여 내 컴퓨터로 가져올 수 있다.
- fetch : fetch를 통해 remote repositroy에서의 변경사항을 확인 할 수 있다. 하지만 변경사항을 local repository로 가져오진 않는다.