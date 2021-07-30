# grpc-example

**1. gRPC란 ?**

구글에서 공개한 오픈소스로 Remote Procedure Call System.
HTTP/2의 stream을 지원하고, 프로토콜 버퍼를 이용하여 proto 파일을 작성한다. 
이때, proto 파일은 Java, C++, Python 등 언어에 종속적이지 않게 자유로운 코드 변환을 제공한다.

**2. gRPC의 서비스 메소드 종류**

- Unary / 서버 (1) : 클라이언트(1)
- Server Streaming / 서버(N) : 클라이언트(1)
- Client Streaming / 서버(1) : 클라이언트(N)
- Bidirectional Streaming / 서버 (N) : 클라이언트 (N)

rpc unaryEvent(HelloRequest) returns (HelloResponse) {}

rpc serverStreamingEvent(HelloRequest) returns (stream HelloResponse) {}

rpc clientStreamingEvent(stream HelloRequest) returns (HelloResponse) {}

rpc biStreamingEvent(stream HelloRequest) returns (stream HelloResponse) {}

[참고]

https://grpc.io/

https://coding-start.tistory.com/353?category=842331

https://jeong-pro.tistory.com/192
