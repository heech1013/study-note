<h1 align="center">Study Note</h1>

<div align="center">
  <img src="https://github.com/heech1013/tech-interview-handbook/blob/main/self-taught.jpg" alt="self-taught" width="400">

<br>
<br>

CS / Front-End를 공부하고 기록합니다.  
 ( 2021.01 ~ 2021.11 )

> · 꼬리에 꼬리를 물고 `왜?`에 대해 탐구한다.  
> · 내용에 `핵심`만 담는다.  
> · 답안을 `병렬적`으로 작성한다.

<br>

</div>

<br>

## Table of Contents

- [CS](#cs)
    - [Network](#network)
    - [OS](#os)
    - [Database](#database)
    - [Data Structure & Algorithm](#data-structure--algorithm)
    - [Etc](#etc)

- [Front-End](#front-end)
    - [Web](#web)
    - [JavaScript](#javascript)

- [Reference](#reference)

<br>

## CS

### Network

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/network/README.md)

일반

- 주소창에 www.naver.com을 입력 후 접속했을 때의 무슨 일이 일어날까?

OSI 7계층

- OSI 7계층이란?
- OSI 7계층이 필요한 이유는?
- OSI 7계층과 TCP/IP 4계층을 비교해본다면?

OSI Physical Layer(물리 계층, 1계층)

- OSI Physical Layer란?

OSI Data-link Layer(2계층)

- OSI Data-link Layer란?
- TCP/IP Network (Interface) layer(1계층)란?
- 데이터 링크 계층의 주요 역할은?
- 2계층에서 데이터가 hop-by-hop으로 전달된다는 것의 의미는 무엇일까?
- 프레이밍이란?
- 프레임의 구조(필드)는?
- MAC 주소란?
- MAC 주소와 IP 주소의 차이점은?
- MAC 주소의 종류에는 어떤 것들이 있을까?
- 스위치란?
- 스위치의 포워딩 방식에 대해 설명해본다면?
- MAC 주소 테이블이란?
- MAC 주소 테이블이 동작하는 과정은?
- LAN과 WAN의 차이점?
- 접근 제어란?
- 흐름 제어(Flow control)란?
- 오류 제어란?
- 이더넷이란?
- 이더넷의 특징?
- 이더넷의 장단점?

OSI Network Layer(3계층) & TCP/IP Internet Layer(2계층)

- OSI Network layer(TCP/IP Internet layer)란?
- 라우터란?
- 라우팅이란?
- 정적 라우팅과 동적 라우팅이란?
- 포워딩이란?
- 포워딩 테이블이란?
- 스위치와 라우터의 차이점은?
- 스위치와 라우터의 공통점은?
- AS(Autonomous System, 자치 시스템)란?
- IP(Internet Protocol)란?
- 네트워크에서 '신뢰성'이 의미하는 것은?
- ICMP(Internet Control Message Protocol)란?
- IP의 데이터그램 단편화(fragmentation)란?
- IP 데이터그램 단편화/재조립에 사용되는 IP 헤더의 종류에는 어떤 것들이 있을까?
- IPv6란?
- ARP(Address Resolution Protocol)란?
- ARP 테이블이란?
- 같은 LAN 상에서의 전송에서 ARP가 진행되는 과정은?
- DHCP(Dynamic Host Configuration Protocol, 동적 호스트 구성 프로토콜)란?
- DHCP의 장단점?
- DHCP에서 IP 주소를 할당 받으면 영원히 사용할 수 있을까?
- DHCP가 ip주소를 임대해주는 절차? `보충`

OSI Transport Layer(4계층) & TCP/IP Transport Layer(3계층)

- Transport Layer란?
- network layer(3계층)와 Transport Layer(4계층)와의 차이점은?
- Transport Layer가 흐름 제어를 제공하는 방법?
- 혼잡 제어(Congestion control란?
- Transport Layer가 혼잡 제어를 제공하는 방법?
- AIMD(합 증가/곱 감소)란?
- Slow start(느린 시작)란?
- Fast retransmit(빠른 재전송)이란?
- Transport Layer가 오류 제어를 제공하는 방법은?

TCP & UDP

- TCP(Transmission Control Protocol)란?
- UDP(User Datagram Protocol)란?
- 연결형 서비스와 비연결형 서비스의 차이점은?
- 데이터그램 방식과 가상 회선 방식이란?
- 가상 회선 방식에서 논리적 연결이 설정되는 과정은?
- 회선 구성 방식에는 어떤 것들이 있을까?
- 전이중, 반이중, 단방향 방식에 대해 설명해본다면?
- TCP와 UDP는 각각 어떤 특성의 서비스에 적합할까?
- 3-way handshake의 과정에 대해 설명해본다면?
- 4-way handshake의 과정에 대해 설명해본다면?
- 왜 2-way handshake는 성립될 수 없을까?

OSI Application Layer(응용 계층, 7계층) & TCP/IP Application Layer(4계층)

- Application Layer란?

DNS

- DNS(Domain Name Server)란?
- 도메인 네임(domain name)이란?
- 도메인 네임의 구조?
- DNS에서 도메인을 얻어오는 과정은?
- PC는 local DNS의 ip 주소를 어떻게 알고 있을까?
- DNS의 구성 요소는?
- 도메인 네임 스페이스란?
- 네임 서버란?
- 네임 서버의 종류는?
- resolver란?
- DNS가 사용하는 전송 계층(Transport Layer)의 프로토콜은?
- DNS에 UDP를 사용하는 이유?

로드 밸런싱(Load Balancing)

- 트래픽이 증가해 기존의 컴퓨팅 자원으로 서비스할 수 없을 때, 대처할 수 있는 2가지 방법은?
- 로드 밸런싱이란?
- 로드 밸런싱 알고리즘에 대해 설명해본다면?
- 각 계층의 로드 밸런서에 대해 설명해본다면?

[(목차로 돌아가기)](#table-of-contents)

<br>

---

### OS

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/os/README.md)

운영체제

- 운영체제란?
- 운영체제의 역할은?

프로세스와 스레드

- 프로세스란?
- 메모리는 어떻게 구성되어 있을까?
- 스레드란?
- 스레드가 필요한 이유는? (스레드의 장점은?)
- 프로세스와 스레드의 차이점은?
- 스레드를 지원하는 주체에 따라 나눈다면 어떻게 나뉠까?
- 사용자 레벨 스레드의 장단점?
- 커널 레벨 스레드의 장단점?
- 멀티 프로세스와 멀티 스레드의 차이점은?

스케줄링

- Context Switching(문맥 교환)이란?
- Context Switching이 필요한 이유는?
- Context Switching이 진행되는 과정은?
- Context에는 어떤 정보들이 있을까?
- Context Switching는 어떤 상황에서 진행될까?
- PCB(Process Control Block)란?
- PCB가 가지고 있는 정보에는 어떤 것들이 있을까?
- 프로세스의 상태가 전이되는 과정은? (프로세스 상태 전이도의 흐름은?)
- 인터럽트(Interrupt)란?
- 인터럽트의 종류에는 어떤 것들이 있을까?
- 인터럽트가 동작하는 순서는 어떻게 될까?
- 시스템 콜(System Call)이란?
- 시스템 콜이 필요한 이유는?
- 커널 모드(Kernel mode)와 사용자 모드(User mode)란?
- 시스템의 성능을 어떤 기준으로 측정할까?
- (참고) 용어
- 스케줄링의 주기에 따라 3가지로 나눈다면 어떻게 나뉠까?
- 선점형 스케줄링과 비선점형 스케줄링의 차이?
- 자원 관리에 있어서 time sharing과 space sharing의 차이는?
- FCFS(First Come First Service)란?
- Round Robin이란?
- SPN(Shortest Process Next)이란?
- SRTN(Shortest Remaining Time Next)란?
- HRRN(High Response Ratio Next)이란?
- MLQ(Multi Level Queue)란?
- MFQ(Multi level Feedback Queue)란?

동기화

- 동기화란?
- 동기화가 필요한 이유는?
- Critical section(임계 구역)이란?
- Race condition(경쟁 상태)이란?
- Mutual exclusion(상호 배제)이란?
- Mutual exclusion에 사용되는 기본 연산(primitive)의 조건은?
- Mutual exclusion을 SW로 구현한 알고리즘에는 어떤 것들이 있나?
- Dekker's algorithm을 설명해본다면?
- Dekker's algorithm을 더 자세히 설명해본다면? (간단하게 코드로 표현해본다면?)
- SW로 구현한 상호 배제 알고리즘의 단점은?
- HW로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?
- TAS(TestAndSet)란?
- TAS를 이용해 ME가 보장되는 과정을 조금 더 자세히 설명? (코드로 설명?)
- OS로 구현한 상호 배제 알고리즘에는 어떤 것들이 있나?
- 스핀락이란?
- 스핀락은 어떤 특성의 프로세스에서 사용하기 적절할까?
- 뮤텍스란?
- 뮤텍스는 어떤 상황에서 사용하기 적절할까?
- 스핀락과 뮤텍스의 차이점은?
- 세마포어란?
- 세마포어에 사용되는 연산의 종류와 그 로직은?
- 스핀락/뮤텍스와 세마포어의 차이는?

데드락

- 데드락(dead lock, 교착 상태)이란?
- 데드락이 발생하기 위한 조건은?
- 데드락을 처리하는 방법은?
- 데드락 회피 알고리즘 중 하나를 설명해본다면?
- 데드락 탐지 알고리즘 중 하나에 대해 설명해본다면?

가상 메모리

- 가상 메모리란? (메모리 가상화란?)
- 메모리의 가상화가 필요한 이유는?

주소 변환(address translation)

- 주소 변환이란?
- 주소 변환이 필요한 이유는?
- 주소 변환을 구현한 기술에는 어떤 것이 있는지?
- base and bound란?
- 베이스 레지스터란?
- 바운드 레지스터(bound register)란?
- 바운드 레지스터가 타 프로세스 메모리 침범을 막는 방법은?
- base and bound에서 운영체제의 역할은?
- base and bound에서 프로세스의 주소 공간을 옮기려면 어떻게 해야 하나?
- base and bound의 장단점은?
- base and bound의 내부 단편화 문제란?

세그멘테이션(segmentation)

- 세그멘테이션이란?
- 세그먼트란?
- 세그멘테이션에서 가상 주소로부터 물리 주소를 얻는 과정은?
- 세그먼트의 바운드 레지스터의 역할은?
- 하드웨어가 가상 주소에서 세그먼트의 종류와 오프셋을 파악하는 방법은?
- 가상 주소 변환에 있어서 스택과 나머지 종류의 세그먼트 간 차이는?
- 하드웨어는 세그먼트가 어느 방향으로 확장해야 하는지 어떻게 알 수 있을까?
- 세그멘테이션이 메모리 공유를 지원하는 방법은?
- 세그멘테이션을 위한 운영체제의 역할은?
- 세그먼트 테이블이란? `보충`
- 세그멘테이션의 장단점은?
- 외부 단편화란?
- 외부 단편화에 대한 대응 방안은?
- 압축이란? 진행되는 과정은?
- 압축의 단점은?
- 빈 공간 리스트를 관리하는 알고리즘에는 어떤 것들이 있으며, 각각의 장단점은?

페이징(Paging)

- 페이징이란?
- 페이징이 등장하게 된 배경은?
- 페이징의 장단점은?
- 페이징에서 물리 메모리의 구성은 어떻게 다른가?
- 페이지 테이블(page table)이란?
- 페이지 테이블 엔트리(PTE, Page Table Entry)란?
- PTE의 구성 요소에는 어떤 것들이 있는지?
- 페이징의 가상 주소에서 물리 주소를 얻어내는 과정은?
- 현재 실행 중인 프로세스의 페이지 테이블 위치를 어떻게 알 수 있을까?

TLB

- TLB(Translation-Lookaside Buffer, 변환-색인 버퍼)란?
- TLB가 필요한 이유는?
- TLB가 도입된 상태에서 가상 메모리 참조 시 일어나는 과정은?
- (TLB의) 지역성 2종류와 적용된 예시에 대해 설명?
- TLB 미스를 처리하는 방법에는 어떤 것들이 있을까?
- TLB 미스 트랩 핸들러가 실행될 때 TLB 미스가 나지 않도록 대응 방안?
- TLB Cache가 설계된 방식은? (cache의 associativity와 관련하여)
- TLB 각 항목의 구성은?
- 페이지 테이블의 valid bit와 TLB의 valid bit 간 차이점은?
- TLB에는 여러 VPN이 공존할 수 있다. 하지만 그럴 경우 여러 프로세스 간 VPN을 구분할 수 없다. 이에 대한 방안은?
- 캐시 교체 정책에는 어떤 것들이 있나?
- LRU란?
- Random 정책이란? 장단점은?
- TLB coverage를 벗어난다는 것의 의미는?

스와핑(Swapping)

- 스와핑이란?
- swap in과 swap out에 대해 설명?
- page fault란?
- 스와핑이 지원되는 상황에서 메모리가 참조되는 과정을 설명?
- 운영체제가 Page fault를 처리하는 과정은?
- 운영체제가 페이지 교체(스왑) 알고리즘을 작동시키는 시기는?
- 페이지 교체(스왑) 알고리즘이 작동될 때(즉, 여유 공간이 최솟값보다 적어질 때) 일어나는 일은?

Blocking/Non-Blocking & Synchronous/Asynchronous

- Blocking과 Non-Blocking의 차이점?
- Synchronous와 Asynchronous의 차이점?
- Blocking + Sync 조합에 대해 설명해본다면?
- Non-Blocking + Sync 조합에 대해 설명해본다면?
- Blocking + Async 조합에 대해 설명해본다면?
- Non-Blocking + Async 조합에 대해 설명해본다면?

[(목차로 돌아가기)](#table-of-contents)

<br>

---

### Database

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/database/README.md)

인덱스

- 인덱스(index)란?
- 인덱스를 사용하면 검색 속도가 빨라지는 이유는?
- 인덱스가 작동하는 과정(순서)은?
- 인덱스를 Hash Table로 구현하지 않는 이유는?
- B-Tree란?
- B+Tree란?
- B-Tree보다 B+ Tree가 갖는 이점은?
- 범위 검색이 Hash table보다 B+ Tree에서 이점을 갖는 이유는?
- 인덱스의 장단점은?
- 인덱스를 생성하기에 적절한 컬럼의 특성은?
- 인덱스를 생성하기에 적절하지 않은 컬럼의 특성은?
- DML(INSERT, DELETE, UPDATE)을 수행할 때 인덱스를 사용하는 컬럼에 대해 추가로 해줘야 하는 작업은?
- 인덱스를 생성/조회하기 위한 SQL문 작성 방법은?

트랜잭션

- 트랜잭션이란?
- 트랜잭션의 성질에는 어떤 것들이 있을까?
- 트랜잭션의 연산에는 어떤 것들이 있을까?
- 트랜잭션의 상태를 설명해본다면?
- 트랜잭션의 고립 수준에 따라 발생 가능한 읽기 이상 현상(Read Phenomena)에 대해 설명해본다면?
- 트랜잭션의 고립 수준 유형에 대해 설명해본다면?
- 트랜잭션의 고립 수준과 동시성과의 상관 관계는?

정규화

- 정규화란?
- 제1 정규화에 대해 설명?
- 제2 정규화에 대해 설명?
- 제3 정규화에 대해 설명?
- BCNF에 대해 설명?
- 데이터베이스의 이상 현상(Anomaly)에는 어떤 것들이 있을까?
- 정규화의 단점은?
- 반정규화(De-normalization)란?

키

- 키란?
- 슈퍼키란?
- 후보키란?
- 기본키란?
- 대체키란?
- 외래키란?

SQL Query

- SQL이란?
- JOIN이란?
- INNER JOIN이란?
- OUTER JOIN이란?
- LEFT (OUTER) JOIN / RIGHT (OUTER) JOIN이란?
- CROSS JOIN(카티전 조인)이란?
- JOIN에서 ON과 WHERE의 차이점은?
- (OUTER) JOIN에서 (ON과 WHERE를 이용해서) 차집합을 구하는 방법은?

DBMS

- DBMS란?
- DBMS를 사용했을 때의 장점은?
- RDBMS란?

[(목차로 돌아가기)](#table-of-contents)

<br>

---

### Data Structure & Algorithm

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/data-structure-and-algorithm/README.md)

Data Structure

- 스택과 큐에 대해 설명해본다면?
- 연결 리스트(Linked List)란?
- 그래프와 트리란?
- 이진 탐색 트리(Binary Search Tree, BST)란?
- 이진 탐색 트리의 연산에 대해 설명해본다면?
- 불균형한 이진 탐색 트리의 검색 연산을 보완하기 위한 방법은?
- 힙이란?
- 힙의 삽입과 삭제 연산에 대해 설명해본다면?
- 우선순위큐를 구현하는 방법에는 어떤 것들이 있을까?
- 해시 테이블(Hash Table)이란?
- 해시 값의 충돌을 해결하는 방법에는 어떤 것들이 있을까?

Algorithm

- 코딩 인터뷰 팁
- 정렬의 종류에는 어떤 것들이 있을까?
- 퀵 소트의 피벗 지정 방식을 어떻게 개선할 수 있을까?
- n번째 피보나치 수를 구하는 방법은?
- DFS와 BFS의 시간 복잡도는?

[(목차로 돌아가기)](#table-of-contents)

<br>

---

### Etc

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/etc/README.md)

객체 지향 프로그래밍(OOP)

- 객체 지향 프로그래밍이란?
- 객체 지향 프로그래밍의 장단점은?
- 절차 지향 프로그래밍이란?
- 클래스와 인스턴스(객체)란?
- 오버로딩(Overloading)과 오버라이딩(Overriding)의 차이점은?
- 객체 지향 5대 원칙에 대해 설명해본다면?

[(목차로 돌아가기)](#table-of-contents)

<br>

---

## Front-end

### Web

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/web/README.md)

브라우저

- 브라우저의 렌더링 과정에 대해 설명?
- 레이아웃과 리페인트의 차이점은?
- 레이아웃과 리페인트의 성능상 차이점은?
- DOM이란?
- DOM의 개체 구조에 대해 설명?
- DOM은 HTML과 1:1로 매핑되는가?
- HTML 문서에서 script 파일을 어디에 위치시키는 것이 좋을까?
- 스크립트 로딩이 HTML 파싱을 방해하는 이유는?
- script를 body 태그 최하위에 놓는 것의 한계는? 그 대안은?
- script 태그의 defer 속성에 대해 설명?
- 여러 defer script 간 script가 실행되는 순서는?
- defer script를 사용할 때 주의해야 할 점은?
- script 태그의 async 속성에 대해 설명?
- 여러 async script 간 script가 실행되는 순서는?
- defer script와 async script가 각각 어느 경우에 유용한가?

성능

- 웹에서 서비스의 성능을 측정하는 방법은?
- 브라우저에서 DOMContentLoaded와 load 이벤트가 발생하는 시점은?
- 브라우저에서 이벤트가 발생하는 시점을 측정하는 방법은?
- 브라우저 기준으로 성능을 측정하는 것의 한계(단점)은?
- 사용자 기준에서 성능을 측정할 수 있는 지표들에 대해 아는 것이 있는지?
- 사용자 기준에서 성능을 측정하는 방법은?
- 웹 페이지 로딩을 최적화할 수 있는 방법에는 어떤 것들이 있을까?
- 블록 리소스 최적화에 대해 설명?
- 리소스 요청 수 줄이기에 대해 설명?
- 리소스 용량 줄이기에 대해 설명?
- 웹 페이지 렌더링을 최적화할 수 있는 방법에는 어떤 것들이 있을까?
- 레이아웃 최적화에 대해 설명?
- 애니메이션 최적화에 대해 설명?

HTTP

- HTTP란?
- HTTP의 특징?
- HTTP가 비연결성으로 설계된 이유가 뭘까?
- HTTP의 비연결성으로 인한 단점이 뭐가 있을까?
- HTTP의 비연결성을 해결하기 위한 방법?
- Keep-Alive를 사용하는 방법?
- Keep-Alive의 장점?
- Keep-Alive의 단점?
- 무상태성을 해결하기 위한 방법?
- HTTP 요청/응답 메시지의 구성(형식)은?
- HTTP Method에는 어떤 것들이 있나?
- GET과 POST의 차이?
- 멱등성이란?
- GET과 HEAD의 차이?
- POST와 PUT의 차이?
- PUT와 PATCH의 차이?
- OPTIONS 란?
- OPTIONS가 언제 사용될까?
- CORS의 preflight request의 목적은?
- (참고) 주요 HTTP 응답 코드
- 인증과 인가의 차이점은?
- HTTP 헤더에는 어떤 것들이 있을까? `보충`
- HTTP의 보안 취약점은?

HTTPS

- HTTPS란?
- HTTPS를 통해 얻을 수 있는 이점은?
- HTTPS가 암호화 채널을 수립할 때 사용하는 암호화 프로토콜은?
- SSL 인증서란?
- SSL 인증서의 역할은?
- SSL 인증서에 포함된 정보는?
- SSL 인증서가 서비스를 보증하는 과정은?
- SSL 통신 과정을 설명해본다면?

HTTP/2

- HTTP/2 이전 버전들의 성능 제한 이슈는? (HTTP/2가 등장한 이유는?)
- HTTP/2의 목적은?
- HTTP/2가 제공하는 주요 기능에는 어떤 것들이 있나?
- HTTP/2는 HTTP의 의미 체계를 대체(변경)하는지?
- HTTP/2의 바이너리 프레이밍 계층이란?
- HTTP/2의 스트림, 메시지, 프레임에 대해 설명?
- HTTP/2가 요청, 응답 다중화를 지원하는 원리는?
- HTTP/2의 요청, 응답 다중화를 통해 얻을 수 있는 이점은?
- HTTP/2의 (출처당) 단일 연결을 통해 얻을 수 있는 이점은?
- HTTP/2에서 스트림 우선순위를 지정하는 과정은?
- HTTP/2의 서버 푸시에 대해 설명?
- HTTP/2의 헤더 압축에 대해 설명?

쿠키 & 세션

- 쿠키란?
- 쿠키는 어떻게 구성되어 있나?
- 쿠키를 생성하는 방법은?
- 쿠키를 요청 메시지에 어떻게 설정하나?
- 요청 메시지에 쿠키가 어디에 들어가있나?
- 쿠키의 단점은?
- 쿠키의 성능 상 단점을 보완하기 위한 대안은?
- 쿠키의 보안적 취약점?
- 쿠키의 보안적 취약점에 대한 대안은?
- 쿠키가 만료되는 시점은?
- 세션이란?
- 세션을 생성하는 절차는?
- 세션의 데이터가 유지되는 기간은? (만료되는 시점은?)
- 쿠키와 세션의 차이점?
- 세션의 장점에도 불구하고 쿠키를 사용하는 이유?

localStorage & sessionStorage

- localStorage(또는 sessionStorage)란?
- 쿠키 대신 사용하는 이유는?
- localStorage과 sessionStorage의 차이점은?

CORS

- CORS란?
- origin(출처)이란?
- 같은 출처, 다른 출처를 판단하는 기준은?
- SOP(동일 출처 정책)란?
- SOP가 존재하는 이유는?
- SOP가 교차 출처로 삽입하는 리소스를 허용하는 경우는?
- 브라우저와 서버 중 CORS를 판단하는 주체는?
- CORS가 동작하는 방식은? (브라우저가 CORS를 판단하는 방법은?)
- CORS가 동작하는 세 가지 시나리오에 대해 알고 있는지?
- Simple Request란? (+ 과정을 설명해본다면?)
- Simple Request를 사용할 수 있는 조건은?
- Preflight Request란? (+ 과정을 설명해본다면?)
- Credentialed Request란?
- Credentialed Request를 사용하는 방법은?
- credentials에 옵션이 same-origin(그리고 같은 출처 간 통신일 때)이거나 include일 때 브라우저가 추가로 확인하는 조건은?
- CORS를 해결할 수 있는 방법은?
- 프록시 서버를 활용해 CORS 에러를 해결하는 과정은?
- CORS(혹은 Access-Control-Allow-Origin)의 단점?
- JSONP란?
- JSONP를 활용하는(동작하는) 과정에 대해 설명?
- JSONP가 더 이상 사용되지 않는 이유는?

REST

- REST란?
- REST의 특징은?
- Uniform Interface란? (더 자세히 설명?)
- Uniform Interface가 필요한 이유는 뭘까?
- REST의 구성은?
- REST에서 정의하는 CRUD Operation과 그에 해당하는 HTTP Method는?
- REST의 장단점?
- REST API란?
- REST API의 규칙은?

보안 공격(XSS/CSRF/SQL Injection)

- XSS란?
- XSS를 방지하기 위한 방법은?
- CSRF란?
- CSRF를 방지하기 위한 방법은?
- SQL Injection이란?
- SQL Injection 중 아는 종류가 있는지?
- SQL injection의 대응 방안은?

Web Server & WAS

- Static Page와 Dynamic Page의 차이점은?
- 웹 서버란?
- 웹 서버의 기능은?
- WAS(Web Application Server)란?
- WAS의 기능은?
- 웹 서버가 필요한 이유는?
- WAS가 필요한 이유는?
- WAS로 웹 서버와 애플리케이션 서버 기능을 모두 수행하지 않는 이유는?

CSR / SSR / SPA

- CSR이란?
- SSR이란?
- SSR의 장점?
- SSR의 단점? `보충`
- SPA란?
- 전통적인 웹 방식은 어땠나?
- SPA의 장점?
- SPA의 단점?
- SPA를 하면 SEO에 문제가 생기는 이유? `보충`
- SPA의 단점 - 초기 구동 속도를 극복하기 위한 방법?
- SPA의 단점 - SEO 최적화 문제를 극복하기 위한 방법? `보충`
- Routing이란?
- SPA에서 routing이 어려울 수 있는 이유?

프론트엔드 개발의 흐름과 철학

- 단방향 바인딩과 양방향 바인딩의 차이는?
- 양방향 데이터 바인딩의 장단점은?
- 단방향 데이터 바인딩의 장단점은?
- (참고) 데이터 상태 관리의 흐름에 대하여

이벤트 버블링 & 캡처 & 위임

- 이벤트 버블링이란?
- 이벤트 캡쳐란?
- 이벤트 캡쳐를 구현하는 방법은?
- 이벤트 전파를 막는 방법은?
- 이벤트 위임이란?
- 이벤트 위임을 사용함으로써 얻을 수 있는 이점은?

Ajax

- Ajax란?
- Ajax의 이점? 사용 이유?
- Ajax를 사용하는 방법은? Ajax가 동작하는 원리는?

JSON

- JSON이란?
- 다른 데이터 포맷과 비교하여 JSON의 이점?
- JavaScript 객체를 JSON으로 변환하는 방법은? 그 반대는?

웹팩 & 바벨

- 웹팩이란?
- 모듈 번들러란?
- 모듈이란?
- 모듈 번들러(혹은 웹팩)이 필요한 이유는?
- 파일 단위로 모듈을 관리하지 않을 때의 문제점?
- 웹팩이 파일 단위로 모듈을 관리하기 위해 사용하는 방법은?
- 웹을 개발할 때 반복되는 작업에는 어떤 것들이 있을까?
- 모듈 번들러(혹은 웹팩)이 웹 로딩 속도를 어떻게 개선할 수 있을까?
- 엔트리(entry)란?
- 아웃풋(output)이란?
- 로더란?
- 로더의 예시에는 어떤 것들이 있을까?
- 플러그인(plugin)이란?
- 바벨이란?
- 트랜스파일이란?

모듈 시스템

- 모듈을 사용함으로써 얻을 수 있는 장점은?
- 자바스크립트 모듈을 구현하는 대표적인 '명세'에는 어떤 것이 있을까?
- AMD와 CommonJS가 어떻게 다를까?
- ES2015(ES6)의 ES Module없이 모듈의 문제점을 어떻게 해결할 수 있을까?
- IIFE 방식으로 모듈을 사용하는 방법은?

컴포넌트

- 프론트엔드에서 컴포넌트란?
- 좋은 컴포넌트를 설계하기 위해 따를 수 있는 원칙에는 어떤 것들이 있을까?

기타

- URI와 URL의 차이는?
- 웹 접근성(Web Accessibility)
- HTML5

[(목차로 돌아가기)](#table-of-contents)

<br>

---

### JavaScript

### [(답변 보러가기 →)](https://github.com/heech1013/tech-interview-handbook/blob/main/javascript/README.md)

언어의 특징

- JS의 언어적인 특징?
- 인터프리터 언어와 컴파일 언어의 차이점?
- 인터프리터 언어와 컴파일 언어의 장단점?
- 프로토타입 기반 언어란?

엔진 & 런타임

- JavaScript 엔진의 구성은?
- JavaScript 런타임이란?

객체(Object)

- Object(객체)란?
- 객체를 생성하는 방법은?

프로토타입(Prototype)

- 클래스 기반의 객체지향 프로그래밍 언어와, 프로토타입 기반의 객체지향 프로그래밍 언어(JavaScript)의 차이점은?
- prototype이란?
- 프로토타입을 사용하는 이유는? (활용되는 예시는?)
- (참고) `[[Prototype]]` & `__proto__` & `prototype`
- 프로토타입이 결정되는 시기는?
- prototype chain이란?
- 프로토타입 객체를 확장하는 방법은?
- 값을 할당할 때와, 참조할 때 프로토타입 체인이 동작하는 여부?
- 프로토타입 객체를 동적으로 변경하는 방법은?
- 프로토타입 객체를 동적으로 변경하기 이전에 생성된 객체와, 이후 생성된 객체의 차이점은?

Class `보충`

- (참고) Class의 constructor

Closure

- Closure란?
- Closure의 동작 원리를 (실행 컨텍스트와 관련하여) 설명?
- Closure의 활용법?
- Closure의 상태 유지가 전역 변수에 비해 갖는 이점?
- 렉시컬 스코핑(lexical scoping)이란?
- Closure의 단점?
- Closure가 참고하고 있는 메모리를 해제해주려면 어떻게 할까?
- 클로저로 인해 자주 발생하는 실수에는 어떤 것들이 있을까? `보충`

this

- this란?
- this의 값이 결정되는 방식을 설명?
- 함수가 '일반 함수로서' 호출될 때 this가 바인딩되는 객체는?
- 전역객체란?
- Browser-side와 server-side에서의 전역객체가 어떻게 다른가?
- 그러면 함수가 '일반 함수로서', 함수의 내부 함수나 메소드의 내부 함수, 콜백 함수 등으로서 호출될 때는?
- 함수가 '일반 함수로서' 호출되었을 때 this가 전역 객체를 참조하는 것을 회피하는 방법이 있을까?
- 함수가 '메소드로서' 호출될 때 this가 바인딩되는 객체는?
- 그러면 함수가 '프로토타입 객체의 메소드로서' 호출될 때는?
- 함수가 '생성자 함수로서' 호출될 때 this가 바인딩되는 객체는?
- 객체 리터럴 방식과 생성자 함수 방식의 차이는?
- 명시적으로 this를 바인딩하는 방법?
- this를 사용할 때 자주 발생하는 실수에는 어떤 것들이 있을까?
- apply, call, bind 메소드의 사용법에 대해 설명?
- 유사 배열(arguments)이 배열의 메소드를 사용할 수 있도록(조작할 때) apply와 call을 사용하는 방법에 대해 아는지?
- 암시적 바인딩과 명시적 바인딩의 우선 순위는?
- arrow function에서의 this는 어떻게 동작하나?
- arrow function을 사용하면 안되는 경우는?

비동기 처리

- JavaScript에서의 비동기 프로그래밍이란?
- JavaScript가 코드를 비동기적으로 실행하는 이유는 뭘까?
- JavaScript에서 (시간이 오래 걸리는) 동기적인 코드가 blocking을 일으키는 이유는 뭘까?
- 프론트엔드에서 비동기 처리가 중요한 이유는?

콜백 패턴 & Promise

- Promise란?
- 동기식 작업과 비동기식 작업이란? 차이점은?
- Promise는 어떤 문제점을 해결하고자 등장했나?
- 비동기 처리에 콜백 패턴을 사용해야 하는 이유는?
- 콜백 방식의 비동기 처리가 에러 처리에 곤란한 이유는?
- Promise를 생성하는 방법은?
- Promise의 상태(state)는 어떤 것들이 있나?
- Promise의 후속 처리 메소드에 대해 설명?
- Promise의 에러 처리는 then과 catch 중 어떤 것으로 하는 것이 더 좋을까?
- Promise의 정적 메소드에 대해 설명?
- Promise.resolve와 Promise.reject에 대해 설명?
- Promise.all과 Promise.race에 대해 설명?

이벤트 루프

- 이벤트 루프란?
- 이벤트 루프가 필요한 이유는?
- Run-to-Completion이란?
- 자바스크립트가 Run-to-Completion으로 동작하는 이유(원리)는?
- 태스크 큐가 동작하는 과정은?
- 태스크 큐와 마이크로 태스크 큐가 동작하는 과정은?
- 이벤트 루프(혹은 태스크 큐의 우선 순위)로 인해 사용자 경험에 해가 되는 경우가 있을까?
- 고비용 연산으로 인한 블로킹에 대응하는 방법은?
- (참고) 활용 예시: progress bar

실행 컨텍스트

- 실행 컨텍스트란?
- 실행 가능한 코드란?
- 실행에 필요한 환경이란?
- 코드가 실행되고, 함수가 실행되고 끝나는 과정을 실행 컨텍스트 스택으로 설명해본다면?
- 실행 컨텍스트의 (물리적인) 구조는?
- Variable Object란?
- 전역 컨텍스트와 함수 컨텍스트에서 VO가 가리키는 객체(내용)의 차이는?
- 스코프 체인이란?
- 특정 EC의 스코프 체인에는 어떤 스코프가 담겨있나?
- 변수를 검색하는 과정을 스코프 체인과 연관하여 설명해본다면?
- 실행 컨텍스트에 값이 채워지는 순서는? (실행 컨텍스트가 생성되는 순서는?)
- 변수 객체화가 진행되는 과정은?
- 클로저를 실행 컨택스트에 기반해 설명해본다면?
- 함수 호이스팅이란?
- 변수 호이스팅이란?

호이스팅

- 호이스팅이란?
- 호이스팅의 대상은?
- 함수 선언문과 함수 표현식의 차이는?
- 함수 선언문에 비해 함수 표현식이 가지는 장점은?
- 호이스팅에서의 우선순위에 대해 설명해본다면?
- 호이스팅은 지향해야 할까, 지양해야 할까?
- 호이스팅을 방지하기 위한 방법은?
- 호이스팅을 지양해야 함에도 불구하고, var와 호이스팅을 이해해야 하는 이유는?

EcmaScript

- EcmaScript란?
- ECMAScript와 JavaScript의 관계는? 차이점은?
- ES6에서 추가된 문법에 대해 아는 것이 있는지?

기타

- 자바스크립트 배열도 객체일까? (배열의 내부 구조는?)
- use strict란?

[(목차로 돌아가기)](#table-of-contents)

<br>

## Reference

- [CS144 Introduction to Computer Networking Fall 2016 Stanford University](https://www.youtube.com/playlist?list=PLvFG2xYBrYAQCyz4Wx3NPoYJOFjvU7g2Z)
- [최희준 교수의 컴퓨터 일반](https://www.youtube.com/channel/UC7Gm_n3bUqqbOiDR3E1U2qg)
- [Operating System, CPA310, KOREATECH](https://www.youtube.com/playlist?list=PLBrGAFAIyf5rby7QylRc6JxU5lzQ9c4tN)
- [운영체제: 아주 쉬운 세가지 이야기](https://github.com/remzi-arpacidusseau/ostep-translations/tree/master/korean)
- [별걸다하는 IT - 운영체제](https://jhnyang.tistory.com/category/%EB%B3%84%EA%B1%B8%EB%8B%A4%ED%95%98%EB%8A%94%20IT/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C%20OS)
- [NHN TOAST FE Guide](https://ui.toast.com/fe-guide/ko)
- [PoiemaWeb](https://poiemaweb.com/)
- [Interview Question for Beginner](https://github.com/JaeYeopHan/Interview_Question_for_Beginner)
- [Tech Interview for Developer](https://gyoogle.dev/blog/)
- [Gidhub - Technology](https://goodgid.github.io/category/#Technology)

---

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fheech1013%2Fstudy-note&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
