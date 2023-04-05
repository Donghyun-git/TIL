# express

## 미들웨어?
- http 요청과 응답 사이에서 로직을 처리하는 함수.
- 매개변수 인자로 error, request, response, next 함수 를 받음.
- next()를 해줘야 다음 로직 처리 함수로 넘어감
- next 함수 안에 인자는 에러 메시지 전달. 다음 로직 처리 함수의 error 매개변수의 인자로 들어가게 된다.


