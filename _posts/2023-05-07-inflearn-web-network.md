---
layout: post
title: 인터넷 네트워크
subtitle: "인터넷 네트워크 개념 정리"
categories: network
tags: [network, web]
---

인터넷 네트워크 정리

## IP(Internet Protocol)

클라이언트(100.100.100.1) => 인터넷(노드) => 서버(200.200.200.2)

IP 패킷 정보를 만들어서 전송
출발(src) : 100.100.100.1
목적(desc) : 200.200.200.2
...

비연결성 - 목적지의 서버가 올라와 있는지 알 수 없음.
비신뢰성 - 중간에 패킷이 손실되거나 인터넷 망, 데이터 용량 등에 따라 전달 순서가 보장되지 않음

## TCP(Transmission Control Protocol)
출발지, 목적지 port, 전송제어, 순서, 검증정보 등을 담고 있다. 

- 연결지향 - TCP 3 way handshake
 1. Client => Server 로 SYN
 2. Client <= Server 로 SYN, ACK
 3. Clinet => Server 로 ACK 
 4. 데이터 전송
 SYN:접속 요청
 ACK:요청 수락

- 데이터 전달 보증
- 순서 보장

따라서 IP의 단점을 보완할 수 있음.

## UDP(User Datagram Protocol)
 
IP와 거의 같다. 다만, port + 체크섬 정도 추가가 되어있음.

## PORT

같은 IP 내에서 프로세스 구분

ex> 아파트를 PC라고 가정했을때 PORT는 전달되어야 하는 호수(프로세스) 정보

0 ~ 65535 할당 가능
0 ~ 1023: 잘 알려진 포트, 사용하지 않는 것이 좋음
- FTP - 20,21
- TELNET - 23
- HTTP - 80
- HTTPS - 443

## DNS(Domain Name Service)

IP는 기억하기 어렵고 변경될 가능성이 있기 때문에 Domain으로 IP를 받아 전송하기 위함






