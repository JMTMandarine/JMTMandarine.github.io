---
layout: post
title: HTTP API 설계
subtitle: "API 설계"
categories: API
tags: [API, web, http, method]
---

## POST 기반 등록 - 클라이언트가 리소스의 URI를 모를 경우
 - 회원 목록 /members -> GET
 - 회원 등록 /members -> POST
 - 회원 조회 /members/{id} -> GET
 - 회원 수정 /members/{id} -> PATCH, PUT, POST
  - PATCH: 부분수정
  - PUT: 전체수정(게시판 수정)
 - 회원 삭제 /members/{id} -> DELETE

 [컬렉션]
  - 서버가 관리하는 리소스 디렉토리
  - 서버가 리소스의 URI를 생성하고 관리

## PUT 기반 등록 - 클라이언트가 리소스의 URI를 알고 있을 경우
 - 파일 목록 /files -> GET
 - 파일 등록 /files/{filename} -> PUT
 - 파일 조회 /files/{filename} -> GET
 - 파일 삭제 /files/{filename} -> DELETE
 - 파일 대량 등록 /files -> POST

 [스토어]
  - 클라이언트가 관리하는 리소스 저장소
  - 클라이언트가 리소스의 URI를 알고 관리

## HTTP FORM 사용 - GET, POST만 지원, AJAX 같은 기술을 사용해서 해결 가능
 - 회원 목록 /members -> GET
 - 회원 등록 폼 /members/new -> GET
 - 회원 등록 /members/new or /members -> POST
 - 회원 조회 /members/{id} -> GET
 - 회원 수정 폼 /members/{id}/edit or /members/{id} -> POST
 - 회원 삭제 /members/{id}/delete -> POST

 [컨트롤URI]
 - GET, POST만 지원하므로 제약이 있음
 - 동사로 된 리소스 경로를 사용
 - POST 의 /new, /edit, /delete가 컨트롤 URI
 