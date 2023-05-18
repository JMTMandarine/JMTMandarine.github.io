---
layout: post
title: HTTP 상태코드
subtitle: "HTTP 상태코드의 종류"
categories: httpStatusCode
tags: [network, web, http, statusCode]
---

## HTTP 상태 코드
클라이언트가 보낸 요청의 처리 상태를 응답에서 알려주는 기능

1. 1xx (Informational): 요청이 수신되어 처리중
 - 거의 사용하지 않음

2. 2xx (Successful): 요청 정상 처리
 - 200 OK: 요청 성공
 - 201 Created: 요청 성공해서 새로운 리소스가 생성됨
 - 202 Accepted: 요청이 접수되었으나 처리가 완료되지 않았음
 - 204 No Content: 서버가 성공적으로 수행했지만, 응답 페이로드 본문에 보낼 데이터가 없음

3. 3xx (Redirection): 요청을 완료하려면 추가 행동이 필요
 - 300 Multiple Choices
 - 301 Moved Permanently: 리다이렉트시 요청 메서드가 GET으로 변하고, 본문이 제거될 수 있음
 - 308 Permanent Redirect: 301과 기능은 같으나, 리다이렉트시 요청 메서드와 본문 유지

4. 4xx (Client Error): 클라이언트 오류, 잘모된 문법등으로 서버가 요청을 수행할 수 없음
5. 5xx (Server Error): 서버 오류, 서버가 정상 요청을 처리하지 못함

## 3xx PRG: Post/Redirect/Get - 일시적인 리다이렉트

1. 302 Found
 - 리다이렉트시 요청 메서드가 GET으로 변하고, 본문이 제거될 수 있음

2. 307 Temporary Redirect 
 - 리다이렉트 요청 메서드와 본문 유지

3. 303 See Other
 - 리다이렉트 요청 메서드가 GET으로 변경

어떻한 경우에 사용을 하는가?
1. /order POST요청
2. 302 Found Location: /order-result/19 리턴
3. /order-result/19 GET 으로 리다이텍트
4. 클라이언트에 주문 결과 페이지로 리다이렉트 처리, 새로고침으로 결과페이지만 조회할 수 있음! 다시 POST 보내 중복주문이 들어가는 등 방지

## 4xx 클라이언트 오류

1. 400 Bad Request
 - 요청 파라미터, API 스펙이 맞지 않을 때

2. 401 Unauthorized
 - 인증 되지 않음
 - 인증(Authentication): 본인이 누구인지 확인, 로그인
 - 인가(Authorization): 권한부여

3. 403 Forbidden
 - 서버가 요청을 이해했지만 승인을 거부함

4. 404 Not Found
 - 요청 리소스를 찾을 수 없음
 - 리소스를 숨기고 싶을 경우도 사용

## 5xx 서버 오류

1. 500 Internal Server Error
 - 서버 내부 문제로 발생

2. 503 Service Unavailable
 - 서비스 이용 불가
 - 서비스 과부하 등 

