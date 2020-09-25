# JAVASCRIPT
자바 스크립트 스킬에 관련된 페이지 입니다.

## promise & ajax

CMS 페이지에서 create / insert / delete 시 로그를 남기고 싶음.<br>
각 칼럼은 육하원칙에 따라 사용자 idx , 메뉴 idx , 실행시간 , 무엇을 실행했는지 , 실행에 대한 정리를 cms_log에 남기려고 함.<br>

보통 view에서 create / insert / delete 시 ajax를 활용하여 비동기식 처리를 함. <br>
그에 맡게 무엇을 실행했는지 Contorller -> service -> DB 로 보내려고함.<br>

문제는 serivce 단에서 데이터를 가공하여 DB에 넣을지 view에서 가공해서 넣을지 고민.<br>
service단에서 넣기에는 문제 (log에 들어갈 데이터를 추합할 때 )가 있어서 뷰에서 데이터를 보내기로 함.<br>
따라서 한 작업 수행 당 한개의 로그가 쌓여야 함.<br>
ajax 안에 ajax를 사용해야하는데 기능적으로는 모르겠지만 딱 봐도 코드가 너저분함.<br>
인터넷에서 방법을 찾던 중 promise 메소드 발견.<br>

https://lee-mandu.tistory.com/437<br>

설명 아주 말끔히 되어있기 때문에 참고할만함.<br>
