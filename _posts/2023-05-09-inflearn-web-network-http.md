---
layout: post
title: HTTP 메서드
subtitle: "HTTP API"
categories: network
tags: [network, web]
---

## HTTP API

[잘못된예시]
- 회원 목록 조회 / read-member-list
- 회원 조회 / read-member-by-id
- 회원 등록 / create-member
- 회원 삭제 / delete-member
- 회원 수정 / update-member

API URI 고민
리소스의 의미는 뭘까?
1. 회원을 등록하고 수정/조회 하는 것은 리소스가 아니다.
2. 리소스와 해당 리소스를 대상으로 하는 행위를 분리
 - 리소스: 회원
 - 행위: 조회, 등록, 삭제, 변경
3. 행위(메서드)는 어떻게 구분?

[예시]
- 회원 목록 조회 / members
- 회원 조회 / members/{id}
- 회원 등록 / members/{id}
- 회원 삭제 / members/{id}
- 회원 수정 / members/{id}

조회/수정/추가/삭제 같은 URI에 어떻게 구분을 할지?