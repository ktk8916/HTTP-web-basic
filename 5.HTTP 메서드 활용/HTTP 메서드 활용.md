# HTTP 메서드 활용

## 클라이언트에서 서버로 데이터 전송

1. 정적 데이터 조회
   - 이미지, 정적 텍스트 조회
   - 쿼리 파라미터 없이 리소스 경로로 조회가능
2. 동적 데이터 조회
   - GET과 쿼리 파라미터 등을 사용하여 검색어 처럼 활용
3. HTML FORM
   - GET, POST만 사용가능
   - POST 메서드는 파라미터를 메시지 바디에 넣어주지만, GET 메서드는 쿼리파라미터로 작성
   - enctype="multipart/form-data"으로 설정하여 파일 등을 업로드 가능
4. HTTP API
   - POST, PUT, PATCH: 메시지 바디를 통해 데이터 전송
   - GET: 조회, 쿼리 파라미터로 데이터 전달
   - Content-Type: application/json을 주로 사용

---

## HTTP API 설계 예시

1. 컬렉션
   - POST 기반
   - 등록될 리소스의 URI를 클라이언트가 모름
   - 서버가 새로 등록된 리소스 URI를 생성
   - /board로 POST하면 게시글이 등록되는 모양
2. 스토어
   - PUT 기반
   - 등록될 리소스의 URI를 클라이언트가 알고 있음
   - /files/{filename}으로 PUT하면 저장되는 모양
3. HTML FORM
   - GET, POST로만 동작

> 리소스와 메서드로만 URI를 설계하기엔 한계가 있기에, URI에 행위가 들어가는 컨트롤 URI의 사용도 충분히 고려
