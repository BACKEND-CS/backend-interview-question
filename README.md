<h2> 📚참고자료 </h2>

<a href="https://github.com/BACKEND-CS/backend-interview-question/blob/main/TMI/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC%20%EC%A7%88%EB%AC%B8%20TMI.md">네트워크 내용 관련 TMI 정리본</a>
<br>
<a href="https://github.com/BACKEND-CS/backend-interview-question/blob/main/TMI/%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B2%A0%EC%9D%B4%EC%8A%A4%20%EC%A7%88%EB%AC%B8%20TMI.md">데이터베이스 내용 관련 TMI 정리본</a>


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
    
    RDBMS에서 데이터 조회 성능 향상을 위해 사용합니다.
    
    장점은 테이블의 레코드를 Full scan하지 않아 검색 속도가 향상됩니다.
    
    단점은 3가지가 있습니다.
    첫 번째로, 조회를 제외한(INSERT, UPDATE, DELETE) 성능에 악영향을 미칩니다.
    두 번째로, 인덱스를 위한 추가 저장 공간이 필요합니다.
    세 번째로, 인덱스를 생성하고 주기적으로 관리할 인력과 시간이 소요됩니다.
     
  </details>
  
  <details>
  <summary> 트랜잭션에 대해서 설명해주세요.</summary>
  
    데이터베이스의 상태를 변화시키는 하나의 논리적인 작업 단위입니다.
    
    하나의 트랜잭션은 여러 개의 연산이 수행될 수 있습니다.
     
  </details>
  
  <details>
  <summary> ACID에 대해서 설명해주세요.</summary>
     
     ACID는 트랜잭션이 안전하게 수행된다는 것을 보장하기 위한 성질로 4가지 특성이 있습니다.
     
     1. 원자성(Atomicity) 
        트랜잭션이 DB에 모두 반영되거나, 중간에 어떤 문제가 발생한다면 전혀 반영되지 않아야 합니다.
        
     2. 일관성(consistency)
        트랜잭션 작업이 완료된 후에도, 데이터베이스의 제약조건이 지켜져야 합니다.
        
     3. 고립성(Isolation)
        둘 이상의 트랜잭션이 실행되고 있을 때, 각각의 트랜잭션은 서로 간섭없이 독립적으로 수행되어야 합니다.
        
     4. 지속성(Durability)
        성공적으로 트랜잭션이 수행되었다면, 그 결과는 데이터베이스에 영구적으로 보존되어야 합니다.
        
  </details>
  
  <details>
  <summary> 트랜잭션 격리 수준(Transaction Isolation Levels)에 대해서 설명해주세요.</summary>
     
     트랜잭션들끼리 일관성 있는 데이터를 얼마나 허용할 것인지 정해놓은 수준을 말합니다.
     
     고립 수준이 높을수록 일관성은 보장되나 그만큼 동시성이 떨어져 성능은 하락합니다.
     
     수준은 총 4단계로, Read Uncommitted, Read Committed, Repeatable Read, Serializable이 있습니다.
     
     이상 현상은 Dirty Read, Non Repeatable Read, Phantom Read가 있습니다.
     
  </details>
  
  <details>
  <summary> 정규화에 대해서 설명해주세요.</summary>
     
     정규화는 관계형 데이터 모델에서 릴레이션의 구조, 스키마를 변경해 가는 과정을 말합니댜.
     
     정규화의 목적
     1. 데이터의 중복을 없애면서 불필요한 데이터를 최소화시킨다.
     2. 무결성을 지키고, 이상 현상을 방지한다.
     3. 테이블 구성을 논리적이고 직관적으로 할 수 있다.
     4. 데이터베이스 구조를 확장에 용이해진다.
     
     
  </details>
  
  <details>
  <summary> JOIN에 대해서 설명해주세요.</summary>
     
      조인은 한 테이블의 primary key로 사용되는 column을 기준으로 두 개의 테이블을 서로 묶어서 하나의 결과를 만들어 내는 것을 말합니다.

    - INNER JOIN(내부 조인)은 두 테이블에 모두 있는 행들만
    - OUTER JOIN(외부 조인)은 기준 테이블에 있는 모든 행들을 가져오고,
    - CROSS JOIN(상호 조인)은 모든 행을 가져옵니다.
    - SELF JOIN(자체 조인)은 자신이 자신과 조인한다는 의미로, 1개의 테이블을 사용합니다.
     
  </details>
  
  <details>
  <summary> RDBMS vs NOSQL에 대해서 설명해주세요.</summary>
     
     RDBMS는 관계형 데이터 베이스로 행과 열로 이루어진 테이블에 데이터를 저장하고, 테이블간의 관계를 만들 수 있습니다. 
     테이블에 정해진 스키마에 따라 데이터를 저장해야 하고, SQL을 사용해 데이터를 다룰 수 있습니다. 
     엄격한 transaction 처리를 필요로 하거나 명확한 데이터 구조를 보장받기를 원할 때 사용하기 좋지만,
     SCALE-UP만 가능해서 비용이 커질수 있습니다.

     NoSQL은 비관계형 데이터 베이스로 정형과 비정형 데이터 모두 (텍스트, 비디오, 오디오, 이미지)를 저장할 수 있습니다. 
     수평확장이 가능하기 때문에 방대한 양의 데이터를 저장해야 하거나
     정확한 데이터 구조를 알 수 없고 데이터가 변경/확장될 수 있는 시스템에 적합합니다.
     
  </details>
  
  <details>
  <summary> Redis에 대해서 간단히 설명해주세요.</summary>
     
     인 메모리 기반의 고성능 key-value 구조의 데이터 스토어입니다. 
     일반적인 데이터베이스는 하드 디스크나 SSD에 저장하는 반면, Redis는 메모리(RAM)에 저장해 디스크 스캐닝 과정이 필요없어 매우 빠릅니다.
     
     대표적인 특징으로는,
     
     1. 휘발성 메모리를 사용하므로(RAM) Snapshot, AOF방식으로 데이터 유실을 방지합니다.
     2. String, Sets, Sorted Sets, Hashes, Lists의 다양한 자료 구조를 지원합니다.
     3. 싱글 스레드로 동작하기 때문에 Thread Safe합니다.
    
  </details>
  
  <details>
  <summary> Redis와 Memcached의 차이에 대해서 설명해주세요.</summary>
     
     1. Memcached는 멀티스레드를 지원해서 멀티 프로세싱이 가능하나, Redis는 싱글 스레드 기반으로 동작합니다.
     2. 데이터 축출 시 Memcached의 경우, LRU(Least Recently Used) 알고리즘만을 채택하고 있지만, Redis는 다양하고 미세한 방법을 제공합니다.
     3. Memcached의 경우 문자열 데이터만 지원하나, Redis는 다양한 데이터 타입을 지원합니다.
     4. Memcached의 경우 데이터를 영속화할 수 있는 기능이 없지만, Redis의 경우 AOF 기반으로 데이터를 영속화할 수 있습니다.
     5. Redis에는 Memcached에는 없는 낙관적 락 기반의 트랜잭션, Replication(데이터 복제), Pub/Sub의 기능을 제공합니다.
     
     트래픽이 몰리는 상황이 자주 발생한다면 멀티 프로세싱 처리가 가능한 Memcached를, 다양한 자료구조가 필요하다면 Redis를 사용하는 것이 좋습니다.
     
  </details>
  
  <details>
  <summary> Elastic Search에 대해서 간단히 설명해주세요.</summary>
    
     
  </details>
  <details>
  <summary> Elastic Search의 인덱스구조와 RDBMS의 인덱스 구조의 차이에 대해 설명해주세요.</summary>
    
     
  </details>
  <details>
  <summary> Elastic Search의 키워드 검색과 RDBMS의 LIKE 검색의 차이에 대해 설명해주세요.</summary>
    
     
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


