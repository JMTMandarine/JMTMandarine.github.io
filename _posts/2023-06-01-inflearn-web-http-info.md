---
layout: post
title: HTTP 헤더
subtitle: "HTTP 일반 헤더"
categories: header
tags: [network, web, http, header]
---

## 일반 헤더 - 표현

1. Content-Type: 표현 데이터의 형식
 - 미디어 타입, 문자 인코딩
 - ex> text/html; charset=utf-8, application/json, image/png
 
2. Content-Encoding: 표현 데이터의 압축 방식
 - 표현 데이터를 압축하기 위해 사용
 - 데이터를 전달하는 곳에서 압축 후 인코딩 헤더를 추가
 - ex> gzip, deflate, identity

3. Content-Language: 표현 데이터의 자연 연어
 - 표현 데이터의 자연 언어를 표현

4. Content-Length: 표현 데이터의 길이
 - 바이트 단위

## 일반 헤더 - 협상: 클라이언트가 선호하는 표현 요청

1. Accept: 클라이언트가 선호하는 미디어 타입 전달

2. Accept-Charset: 클라이언트가 선호하는 문자 인코딩

3. Accept-Encoding: 클라이언트가 선호하는 압축 인코딩 

4. Accept-Language: 클라이언트가 선호하는 자연 언어