---
layout: post
title: HTTP 헤더 정보
subtitle: "HTTP 헤더 정보"
categories: header
tags: [network, web, http, header]
---

## 일반 정보

1. From: 유저 에어전트의 이메일 정보

2. Referer: 이전 웹 페이지 주소
 - A -> B로 이동하는 경우 B를 요청할 때 Referer:A 를 포함해서 요청
3. User-Agent: 유저 에이전트 애플리케이션 정보
 - 클라이언트의 애플리케이션 정보(웹 브라우저 정보 등)
 - 통계 및 브라우저별 장애 파악에 용이

4. Server: 요청을 처리하는 오리진 서버의 소프트웨어 정보

5. Date: 메시지가 생성된 날짜

## 특별한 정보

1. Host: 요청한 정보(도메인)
 - 특정 서버(100.100.100.1)에 여러개의 애플리케이션이 구동되고 있을 경우 어느 도메인에 요청하는지에 대한 정보
2. Location: 페이지 리다이렉션

3. Allow: 허용 가능한 HTTP 메서드

4. Retry-After: 유저 에이전트가 다음 요청을 하기까지 기다려야 하는 시간

## 인증 정보
 1. Authorization: 클라이언트 인증 정보를 서버에 전달

 2. WWW-Authenticate: 리소스 접근시 필요한 인증 방법 정의