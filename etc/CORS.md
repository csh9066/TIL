## CORS

- 보안상 브라우저는 다른 출처(origin)의 스크립트 요청은 제한하고 있음
- CORS는 다른 출처(origin)로 xhr과 같은 요청했을 때 접근 권한을 부여하도록 하는 브라우저 정책
- 기본적으로 서버에서는 응답 헤더 `Access-Control-Allow-Orgin`세팅 해줘야함

## 접근 제어 시나리오

### 단순 요청(Simple requests)

- `GET` `POST` `HEAD` 을 사용하는 기본적인 요청임
- Request Header에는 다음과 같은 요청만 허용함
  - `Accept`, `Accept-Language`, `Content-Language`, `Content-Type`
- Content-Type 헤더에는 다음과 같은 값들만 허용함
  - `application/x-www-form-urlencoded`, `multipart/form-data`, `text/plain`
- 커스텀 헤더를 사용할 수 없음

## 프리플라이트 요청(Preflighted request)

- Simple Request의 요청에 부합하지 않으면 브라우저는 자동으로 Preflight Request으로 요청을보냄
- 먼저 `OPTIONS` 메소드를 통해 서버에서 CORS설정에 부합 되면 원래 요청을 보냄
- 서버에서는 커스텀 헤더를 `Access-Control-Allow-Headers` 와 `Access-Control-Allow-Method` 를 설정해줘야 예비 요청(OPTION)을 통과할 수 있음

## 인증정보를 포함한 요청(credentialed request)

- cookie나 authorization header와 같은 인증 정보를 자격을 인증할 때 사용
- 브라우저에서는 `XMLHttpRequest.withCredential`의 속성을 true로 설정해야 서버에서는 자격 인증을 할 수있음
- 서버에서는 응답 헤더의 `Access-Control-Allow-Credentials` 를 `true` 로 설정해야하고 `Access-Control-Allow-Orgin` 을 `*` 로 설정하면 안됨

## Reference

[https://developer.mozilla.org/ko/docs/Web/HTTP/CORS](https://developer.mozilla.org/ko/docs/Web/HTTP/CORS)
