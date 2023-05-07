---
layout: post
title: URI
subtitle: "웹 브라우저의 요청 흐름"
categories: network
tags: [network, web]
---

URI와 웹 브라우저 요청 흐름

## URI(Uniform Resource Identifier)

- Uniform: 리소스 식별하는 통일된 방식
- Resource: 자원, URI로 식별할 수 있는 모든 것 
- Identifier: 다른 항목과 구분하는데 필요한 정보

## 웹 브라우저의 요청 흐름
 
https://www.google.com/search?q=hello&hl=ko

1. 아래와 같이 HTTP 요청 메시지가 만들어짐
GET /search?q=hello&hl=ko HTTP/1.1
Host: www.google.com

2. TCP/IP 패킷을 생성하여 HTTP 요청 메시지를 담아 전송
3. Server(google)에서 메시지를 해석
4. HTTP 응답 메시지를 생성 후 1번과 같은 방식으로 전송 
HTTP/1.1 200 OK
Content-Type: text/html;charset=UTF-8
Content-Length: 3423 ....

