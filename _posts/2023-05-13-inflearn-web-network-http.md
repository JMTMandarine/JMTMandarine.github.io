---
layout: post
title: HTTP 메서드
subtitle: "HTTP 메서드의 속성"
categories: network
tags: [network, web, http, method]
---

## HTTP 메서드의 속성

1. 안전(Safe Methods)
 - 호출해도 리소스를 변경하지 않는다. (ex> GET)
2. 멱등(Idempotent Methods)
 - 한 번 호출하든 여러 번 호출하든 결과가 똑같다.
 GET, PUT, DELETE - 멱등
 POST - 멱등이 아님
 - 자동 복구 매커니즘, 요청이 지연되거나 TIMEOUT 등의 이유로 재요청할 경우
 1. 사용자 1 : GET
 2. 사용자 2 : PUT
 3. 사용자 3 : GET
 => 외부 요인으로 중간에 변경되는 경우는 고려하지 않음
3. 캐시가능(Cacheable Methods)
 - 응답 결과 리소스를 캐시해서 사용해도 되는가?
 - GET, HEAD, POST, PATCH 캐시가능
 - 실제로는 GET, HEAD 정도만 캐시로 사용, POST, PATCH는 본문 내용까지 캐시 키로 고려해야 하므로 구현이 쉽지않음.
