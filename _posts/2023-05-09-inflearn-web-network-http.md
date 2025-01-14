---
layout: post
title: HTTP 메서드
subtitle: "HTTP URI"
categories: network
tags: [network, web, http, method]
---

## API URLI

API URI 고민
리소스의 의미는 뭘까?
1. 회원을 등록하고 수정/조회 하는 것은 리소스가 아니다.
2. 리소스와 해당 리소스를 대상으로 하는 행위를 분리
 - 리소스: 회원
 - 행위: 조회, 등록, 삭제, 변경
3. 행위(메서드)는 어떻게 구분?

[잘못된예시]
- 회원 목록 조회 / read-member-list
- 회원 조회 / read-member-by-id
- 회원 등록 / create-member
- 회원 삭제 / delete-member
- 회원 수정 / update-member

[예시]
- 회원 목록 조회 / members
- 회원 조회 / members/{id}
- 회원 등록 / members
- 회원 삭제 / members/{id}
- 회원 수정 / members/{id}

그렇다면 위 예시에서 같은 URI에 <조회/수정/추가/삭제>를 어떻게 구분을 할지?

## HTTP Method

GET : 리소스 조회
POST : 요청 데이터를 처리, 주로 등록
PUT : 리소스를 대체, 해당 리소스가 없으면 생성
PATCH : 리소스 부분 변경
DELETE : 리소스 삭제

1. GET
 - 리소스 조회
 - 데이터를 쿼리스트링을 통해서 전달
 - 메시지 바디를 사용해서 데이터를 전달할 수 있지만, 지원하지 않는 곳이 많아서 권장하지 않음

2. POST
 - 요청 데이터를 처리
 - 메시지 바디를 통해 서버로 요청 데이터 전달
 - 서버는 요청 데이터를 처리
 - 주로 전달된 데이터를 신규 리소스 등록, 프로세스 처리에 사용

[정리]
POST를 어떻게 사용한다는 것 일까?에 대한 고민
예를 들어 아래와 같은 기능에 사용(생성)
 - 회원가입, 주문, 게시판 글쓰기
 => URI에 POST 요청이 오면 요청 데이터를 어떻게 처리할지 리소스 마다 따로 정의해야함
 - 단순히 데이터를 생성하거나, 변경하는 것을 넘어서 프로세스를 처리해야 하는 경우
 => 주문에서 결제완료 -> 배달시작 -> 배달완료 처럼 단순히 값 변경을 넘어 프로세스의 상태가 변경되는 경우
 - POST의 결과로 새로운 리소스가 생성되지 않을 수도 있음
 => 예시) POST /orders/{orderID}/start-delivery (컨트롤 URI)
 - 다른 메서드로 처리하기 애매한 경우?
 => JSON으로 조회 데이터를 넘겨야하는데, GET 메서드를 사용하기 어려운 경우

3. PUT
 - 리소스를 완전히 대체
  - 리소스가 있으면 대체
  - 리소스가 없으면 생성
  - 데이터를 덮어버림
 - 클라이언트가 리소를 식별
  - 클라이언트가 리소스 위치를 알고 URI를 지정
  - POST와 차이점

POST는 리소스를 식별하지 못하고 데이터를 처리
PUT은 100번이라는 것 을 식별하고 데이터 처리
POST /members
PUT /members/100

4. PATCH

