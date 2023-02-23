# backend-interview-question



<details>
  <summary><h1> 네트워크 </h1></summary>
  
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
  
    
     내용   

  </details>
 
</details>

