# tech-interview-handbook

## Table of Contents

[CS](##cs)

- [Network](###network)
- OS
- Database

Front-End

- Web
- JavaScript

## CS

### [Network](https://github.com/heech1013/tech-interview-handbook/network/README.md)

- OSI 7계층
  - OSI 7계층이란?
  - OSI 7계층이 필요한 이유는?
  - OSI 7계층이 네트워크 개발과 유지보수에 어떤 이점이 있을까?
  - OSI 7계층과 TCP/IP 4계층을 비교해본다면?
  - OSI와 TCP/IP 계층이 각각 어느 계층과 연관되어 있을까?
- OSI 1계층(물리 계층, Physical Layer)
  - OSI 1계층(물리 계층, Physical Layer)이란?
  - OSI 1계층의 인코더와 디코더란?
  - 아날로그 신호와 디지털 신호의 차이점?
  - 아날로그 신호를 디지털 신호로 바꾸는 과정은?
  - 1계층이 구현되어 있는 구체적인 위치는?
- OSI 2계층(Data-link Layer)
  - OSI 2계층(Data-link Layer)이란?
  - 데이터 링크 계층의 주요 역할은?
  - 2계층에서는 데이터가 hop-by-hop으로 전달된다는 것의 의미는
  - Framing이란?
  - Frame의 구조(필드)는?
  - 물리 주소(MAC 주소)이란?
  - MAC 주소와 IP 주소의 차이점은?
  - MAC 주소의 종류에는 어떤 것들이 있을까?
  - OSI 2계층에 사용되는 장비에는 어떤 것들이 있을까?
  - 스위치란?
  - 스위치의 포워딩 방식에는 어떤 것들이 있을까?
  - 스위치 포워딩 방식 cut-through에 대해 설명?
  - cut-through의 장단점은?
  - 스위치 포워딩 방식 중 store-and-forward에 대해 설명?
  - store-and-forward에서 패킷의 오류를 어떻게 체크하나?
  - MAC 주소 테이블의 용도는?
  - MAC 주소 테이블의 구성은?
  - MAC 주소 테이블이 동작하는 과정은?
  - MAC 주소 테이블에 entry가 생성되는 과정은?
  - LAN과 WAN의 차이점?
  - 접근 제어란?
  - CSMA/CD란?
  - 흐름 제어(Flow control)란?
  - OSI 2계층의 흐름 제어에 대해 설명해본다면?
  - 순서제어란?
  - OSI 2계층의 순서 제어란? `보충`
  - 오류 제어란? `보충`
  - OSI 2계층의 프로토콜에는 어떤 것들이 있을까?
  - 이더넷이란?
  - 이더넷의 특징?
  - 이더넷의 장단점?
  - 회선 구성 방식에는 어떤 것들이 있을까?
  - 점대점 방식이란?
  - 점대점 방식의 장단점은?
  - 다중점 방식이란?
  - 다중점 방식의 장단점은?
  - 전이중, 반이중, 단방향 방식에 대해 설명해본다면?
- (OSI) 3계층 & (TCP/IP) Network Layer
  - osi 3계층(network layer)란?
  - network layer의 역할은?
  - network layer의 장비에는 어떤 것들이 있을까?
  - 라우터란?
  - 라우팅이란?
  - 라우팅의 종류?
  - 정적 라우팅의 장단점?
  - 동적 라우팅의 장단점?
  - 스위치와 라우터의 차이점은?
  - 스위치와 라우터의 공통점은?
  - 포워딩이란?
  - 포워딩 테이블이란?
  - 라우터의 자치(자율) 시스템(AS, Autonomous System)이란?
  - AS가 필요한 이유는?
  - gateway router란?
  - network layer의 프로토콜에는 어떤 것들이 있을까?
  - IP(Internet Protocol)란?
  - IP의 특징?
  - 연결형 서비스와 비연결형 서비스의 차이점?
  - 패킷 교환 방식에는 어떤 것들이 있을까?
  - 데이터그램 방식이란?
  - 가상 회선 방식이란?
  - 가상 회선 방식에서 논리적 연결이 설정되는 과정은?
  - 데이터그램 방식과 가상회선 방식이 속도 측면에서 어떤
  - 데이터그램 방식과 가상회선 방식은 각각 어떠한 특성의
  - 네트워크 내 한 노드가 다운되었을 때 데이터그램 방식과
  - 가상회선 방식과 데이터그램 방식의 공통점은?
  - Packet Switching `보충`
  - 패킷 교환 방식 말고 다른 방식에는 어떤 것들이 있을까?
  - 네트워크에서 '신뢰성'이란 무엇을 의미하나?
  - IP의 비신뢰성을 보완하기 위한 방법에 대해 알고 있는 것이
  - ICMP에서 사용하는 에러 메시지의 종류에는 어떤 것들이
  - IP의 데이터그램 단편화(fragmentation)란?
  - IP 데이터그램 단편화/재조립에 사용되는 IP 헤더의 종류에는
  - IPv6가 등장한 배경은?
  - IPv6의 특징은?
  - QoS(Quality of Service)란?
  - ARP란?
  - 데이터 통신에 ARP가 필요한 이유는?
  - ARP 테이블이란?
  - 누가 ARP 테이블을 가지고 있을까?
  - ARP 테이블에서 TTL의 역할은?
  - ARP의 plug-and-play에 대해 설명?
  - 같은 LAN 상에서의 전송에서 ARP가 진행되는 과정은?
  - 다른 LAN으로의 전송에서 ARP가 진행되는 과정은?
  - DHCP(Dynamic Host Configuration Protocol, 동적 호스트 구성
  - DHCP의 장단점?
  - DHCP에서 IP 주소를 할당 받으면 영원히 사용할 수 있을까?
  - DHCP가 ip주소를 임대해주는 절차? `보충`
  - network layer(3계층)와 Transport Layer(4계층)와의 차이점은?
- OSI 4계층 / TCP/IP Transport Layer
  - Transport Layer란?
  - Transport Layer의 특징?
  - Transport Layer의 역할?
  - Transport Layer에서 논리적 연결이 성립되는 과정은?
  - Data-link Layer와 Transport Layer 모두 오류 제어와 흐름
  - Transport Layer가 흐름 제어를 제공하는 방법?
  - stop and wait이란?
  - 슬라이딩 윈도우란?
  - 송신측이 수신측의 윈도우 사이즈를 어떻게 알 수 있을까?
  - 혼잡 제어(Congestion control란?
  - Transport Layer가 혼잡 제어를 제공하는 방법?
  - 혼잡 제어 알고리즘 AIMD(합 증가/곱 감소)란?
  - 혼잡 제어 알고리즘 Slow start(느린 시작)란?
  - 혼잡 제어 알고리즘 Fast retransmit(빠른 재전송)이란?
  - Transport Layer가 오류 제어를 제공하는 방법?
  - TCP(Transmission Control Protocol)란?
  - TCP의 특징은?
  - TCP가 UDP에 비해 속도가 느린 이유는?
  - TCP가 전이중 방식인 이유는?
  - TCP가 전송할 수 있는 데이터의 크기 제한은?
  - TCP에서 서버와 클라이언트가 몇 대 몇으로 연결될까?
  - TCP가 논리적 연결을 성립/해제하는 방법은?
  - 3-way handshake의 과정에 대해 설명해본다면?
  - 4-way handshake의 과정에 대해 설명해본다면?
  - 메시지(세그먼트)가 SYN인지, ACK, FIN 등인지 나타내는
  - UDP(User Datagram Protocol)란?
  - UDP의 특징은?
  - 체크섬 필드로 오류를 어떻게 검출할 수 있을까?
  - UDP가 전송할 수 있는 데이터의 크기 제한은?
  - UDP에서 서버와 클라이언트가 몇 대 몇으로 연결되나?
  - TCP와 UDP는 각각 어떤 특성의 서비스에 적합할까?
- OSI 5계층(Session Layer) / OSI 6계층(Presentation Layer) /
- TCP/IP 4계층(Application Layer, 응용 계층)
  - 응용 계층이란? `보충`
  - 응용 계층의 역할은?
  - 응용 계층의 프로토콜에는 어떤 것들이 있을까?
- DNS
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
  - DNS에 UDP를 사용하는 이유? `보충`
  - DNS Round robin? `보충`

### OS

### Database

## front-end

### Web

### JavaScript
