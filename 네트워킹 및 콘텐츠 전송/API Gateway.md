![image](https://user-images.githubusercontent.com/103885741/232383576-6f091b48-7d25-43ab-b78b-26c64647e848.png)
API Gateway


- 개념 및 특징

API 형식으로 AWS 서비스에 접근할 수 있도록 해주는 서비스이다.

규모에 상관없이 API 생성, 유지 관리, 모니터링과 보호를 할 수 있게 해주는 서비스이다.

Client에서 server로 통신할 때 사용하는 많은 api들의 문(게이트웨이)과 같은 역할을 한다고 보면 된다.


- 특성

API Gateway를 이용하면 통합적으로 엔드포인트와 REST API를 관리할 수 있다.

API 게이트웨이를 등록해주면, 모든 클라이언트는 각 서비스의 엔드포인트 대신 API Gateway로 요청을 전달하여 관리가 용이해진다. 

사용자가 설정한 라우팅 설정에 따라 각 엔드포인트로 클라이언트를 대리하여 요청하고 응답을 받으면 다시 클라이언트에게 전달하는 프록시(proxy) 역할을 하기 때문이다.


- REST API

Lambda를 HTTP 프로토콜 기반의 REST API로 호출

- WebSocket

WebSocket 프로토콜로 Lambda를 호출

WebSocket으로 붙을때 ConnectionID를 부여

ConnectionID로 구분 된 클라이언트에 메시지 전송 가능
