<h2> 📚참고자료 </h2>

<a href="https://github.com/BACKEND-CS/backend-interview-question/blob/main/TMI/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC%20%EC%A7%88%EB%AC%B8%20TMI.md">네트워크 내용 관련 TMI 정리본</a>
<a href="https://github.com/BACKEND-CS/backend-interview-question/edit/main/TMI/%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B2%A0%EC%9D%B4%EC%8A%A4%20%EC%A7%88%EB%AC%B8%20TMI.md">데이터베이스 내용 관련 TMI 정리본</a>


<details>
  <summary><h2> 📡네트워크 </h2> </summary>
  
  <details>
  <summary> 웹 통신의 큰 흐름: https://www.google.com/ 을 접속할 때 일어나는 일</summary>
  
    1. 입력한 도메인 주소에 해당하는 서버의 IP주소를 알기 위해 첫번째로 캐싱된 데이터가 있는지 확인한다.
    2. 캐싱된 데이터가 없다면 DNS 서버에서 해당 도메인에 매핑되는 IP 주소가 검색될 때까지 반복적 질의 요청을 진행합니다.
    3. 신뢰할수 있는 연결을 위해 TCP 프로토콜을 이용해 3-way handshake 과정을 진행합니다.
    4. 브라우저가 서버에 HTTP/GET 요청을 보내고, 서버는 해당하는 리소스를 응답하면 브라우저는 리소스를 렌더링해서 클라이언트에게 보여줍니다.
    
  </details>
  
  <details>
  <summary> TCP와 UDP의 차이점에 대해서 설명해보세요.</summary>
  
    - TCP
      1. 가상 회선 방식의 연결 지향형 프로토콜(3/4-way handshake)
      2. 전송 순서 보장
      3. 흐름 제어, 혼잡 제어를 통한 데이터 처리 속도, 패킷 수 조절
      4. 높은 신뢰성 보장
      5. 속도 느림
     
    - UDP
      1. 데이터그램 방식의 비연결형 서비스
      2. 전송 순서 미보장
      3. 데이터 수신 여부 미확인
      4. 신뢰성이 낮음
      5. TCP보다 속도 빠름

  </details>
  
  <details>
  <summary> TCP 3, 4 way handshake에 대해서 설명해보세요.</summary>
  
    TCP 3way handshake는 SYN, ACK 패킷을 주고받으며 가상회선을 수립하는 단계입니다. 
    클라이언트는 서버에 요청을 전송할 수 있는지, 서버는 클라이언트에게 응답을 전송할 수 있는지 확인하는 과정입니다. 
    
    TCP 4way handshake는 ACK, FIN 패킷을 주고받으며, TCP연결을 해제하는 단계입니다.
    단, 서버에서 소켓이 닫혔다고 통지해도 클라이언트 측에서는 일정시간 대기하는데, 혹시나 패킷이 나중에 도착할 수 있기 때문입니다.
    
  </details>
  
  <details>
  <summary> HTTP와 HTTPS의 차이점에 대해서 설명해보세요.</summary>
 
    HTTP와 HTTPS 모두 인터넷 상에서 클라이언트와 서버가 자원을 주고 받을 때 쓰는 통신 규약입니다.
    HTTP 암호화되지 않은 텍스트 교환이고, HTTPS는 TLS/SSL 프로토콜을 사용해 데이터를 암호화하여 통신합니다.

  </details>
  
  <details>
  <summary> SSL Handshake에 대해서 설명해보세요.</summary>
  
    1. 클라이언트는 TCP 3-way handshake를 수행한 이후 데이터 전송합니다.
    2. 서버는 SSL 인증서 보냅니다.
    3. 클라이언트는 받은 SSL 인증서를 인증기관에 검증합니다.
    4. 클라이언트는 서버의 공개키를 얻을 수 있습니다.
    5. 클라이언트가 서버의 공개키로 대칭키를 암호화해서 서버에 보냅니다.
    6. 서버는 이를 개인키로 복호화하고 이후 통신은 공유된 대칭키로 암호화되어 통신합니다.

  </details>
  
  <details>
  <summary> HTTP 메서드와 이것이 하는 역할에 대해서 설명해보세요.</summary>
  
    HTTP 메서드는 클라이언트가 서버에 리소스를 요청할 때 사용하는 방법입니다.
    각 메서드는 서버에서 수행하는 특정 동작을 나타냅니다.
    대표적으로, GET/POST/PUT/DELETE가 있습니다.

    HTTP 메서드는 서버에서 어떤 동작을 수행할지를 결정하여 클라이언트와 서버 간에 명확하고 예측 가능한 상호 작용을 가능하게 합니다.

  </details>
  
  <details>
  <summary> RESTful, REST에 관한 설명</summary>
  
    REST는 각 자원에 대하여 자원의 상태에 대한 정보를 주고받는 개발방식을 말합니다.
    서버의 자원을 어떠한 방식으로 접근하도록 해야 하는지를 구체적으롬 명시한 아키텍쳐 스타일입니다.
    
    이 아키텍쳐 원칙을 잘 준수해서 설계했을 때 RESTful하다고 할 수 있습니다.

  </details>

  <details>
  <summary> OSI 7계층과 존재 이유</summary>
    
    OSI 7계층은 네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말합니다.
    
    통신이 일어나는 과정을 단계별로 파악하기 용이합니다.
    문제가 발생했을 때 다른 단계의 장비/소프트웨어를 건드리지 않고 문제가 발생한 단계에서 해결할 수 있습니다.
    
  </details>
  <details>
  <summary> TCP/IP 4계층</summary>
  
    TCP/IP 4계층은 TCP/IP 프로토콜 통신 과정에 초점을 맞춘 모델입니다.
    OSI 7계층에 비해 간소화된 계층 구조로 네트워크 통신의 효율성을 높이고자 하는데 그 목적이 있습니다.

  </details>
  <details>
  <summary> 웹 서버 소프트웨어(Apache, Nginx)는 OSI 7계층 중 어디서 작동하는지 설명해보세요.</summary>
  
    Web Server는 HTTP 프로토콜을 이용하여 HTML 데이터를 클라이언트에게 제공해주는 서버입니다.

    HTTP 프로토콜이란 OSI 7 계층인 응용 계층에 위치한 프로토콜로서 브라우저(클라이언트)와 서버 사이에 정보를 주고 받기 위한 프로토콜로 사용된다. 

    그렇기 때문에 웹 서버 소프트웨어인 Apache, Nginx는 OSI 7계층 중 응용 계층(Application Layer)에서 작동합니다.

  </details>

</details>

<details>
 <summary><h2> 📳데이터베이스 </h2> </summary>

  <details>
  <summary> 데이터베이스에서 인덱스를 사용하는 이유 및 장단점에 대해 설명해주세요.</summary>
     
  </details>
  
  <details>
  <summary> 트랜잭션에 대해서 설명해주세요.</summary>
     
  </details>
  
  <details>
  <summary> ACID에 대해서 설명해주세요.</summary>
     
  </details>
  
  <details>
  <summary> 트랜잭션 격리 수준(Transaction Isolation Levels)에 대해서 설명해주세요.</summary>
     
  </details>
  
  <details>
  <summary> 정규화에 대해서 설명해주세요.</summary>
     
  </details>
  
</details>


 <details>
 <summary><h2> 📳운영체제 </h2> </summary>

  <details>
  <summary> Blocking/Non-blocking & Synchronous/Asynchronous</summary>
      
    - Blocking : 호출된 함수가 자신의 작업을 다 마칠 때까지 제어권을 가지고 있고, 호출한 함수는 호출된 함수가 작업을 마무리할 때까지 기다립니다.
    - Non-blocking : 호출된 함수가 작업을 마치지 않아도 제어권을 호출한 함수에게 바로 넘겨주어 호출한 함수도 자신의 작업을 진행할 수 있습니다.
      
      -> 호출된 함수가 호출한 함수에게 제어권을 넘겨주는 유무의 차이
      
    - Synchronous : 요청 순서에 맞게 하나씩 처리하는 것을 말합니다.
    - Asynchronous : 하나의 요청이 끝나기도 전에, 다른 요청을 동시에 처리할 수 있는 것을 말합니다.
     
     -> 즉, 호출된 함수를 호출한 함수가 신경쓰는지, 호출된 함수 스스로 신경쓰는지를 동기/비동기라고 생각하면 된다.
     
  </details>
 </details>


