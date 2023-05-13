---
layout: post
title: HTTP 메서드
subtitle: "HTTP 메서드 활용"
categories: network
tags: [network, web, http, method]
---

## HTTP 클라이언트에서 서버로 데이터 전송

1. 쿼리 파라미터를 통한 데이터 전송
 - GET
 - 주로 정렬 필터(검색어)

2. 메시지 바디를 통한 데이터 전송
 - POST, PUT, PATCH
 - 회원가입, 상품주문, 리소스 등록/변경 등

## HTTP 클라이언트에서 서버로 데이터 전송 case

1. 정적 데이터 조회
 - 이미지, 정적 텍스트 문서

2. 동적 데이터 조회
 - 주로 검색, 게시판 목록에서 정렬 필터(검색어)

3. HTML Form을 통한 데이터 전송
 - 회원가입, 상품주문, 데이터 변경
 
4. HTTP API를 통한 데이터 전송
 - 회원가입, 상품주문, 데이터 변경
 - 서버 to 서버, 앱/웹(Ajax) 클라이언트