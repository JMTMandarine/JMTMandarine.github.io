---
layout: post
title: HTTP
subtitle: "HTTP 기본 개념"
categories: network
tags: [network, web]
---

HTTP 기본 개념

## HTTP(HyperText Transfer Protocol)
서버간 모든 데이터 전송 가능
- HTML, TEXT
- IMAGE, 음성, 영상, 파일
- JSON, XML

## 클라이언트 서버 구조

Request, Response 구조

클라이언트는 서버에 요청을 보내고 응답을 대기하는 구조

클라이언트와 서버가 각각 분리되어 있어 각각 역할에 맞게 고도화가 가능
 
## Stateful, Stateless

1. Stateful (상태유지)
 - 상태가 계속 유지되어 있어야 하므로 중간에 서버가 바뀔 경우 문제 발생 

2. Stateless (무상태)
 - 중간에 서버가 바뀌어도 문제가 발생하지 않음, 따라서 요청이 증가함에 따라 추가적인 서버 증설이 가능.

[정리]
1. 모든 것을 무상태로 설계할 수 없음. 하지만 상태유지는 필요한 경우 최소한만 사용
2. 상태유지 - 로그인, 무상태 - 로그인이 필요하지 않은 단순 서비스 화면 등
3. 브라우저의 쿠기와 서버의 세션 등을 사용하여 상태유지

## 비연결성
[장점]
HTTP는 기본적으로 연결을 유지하지 않는 모델
서버 자원을 매우 효율적으로 사용할 수 있음

[한계&극복]
TCP/IP 연결을 새로 맺어야 해서 3 way handshake 시간이 매번 추가됨
지금은 HTTP 지속 연결(Persistent Connections)로 문제 해결
HTTP/2, HTTP/3에서는 더 많은 최적화가 이루어짐

## 대용량 트레픽에 따른 구조 
1. 최초 접속 페이지를 무상태의 정적 페이지를 노출
2. 무상태 정적 페이지에서 이벤트와 같은 서버 요청을 유도
3. 서버 구조를 최대한 Stateless 로 구현


