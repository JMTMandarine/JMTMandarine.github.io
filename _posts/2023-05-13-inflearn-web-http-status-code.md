---
layout: post
title: HTTP 상태코드
subtitle: "HTTP 메서드의 속성"
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