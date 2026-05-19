<div align="center">

# 🥖 모두의빵 

### 실시간 주문 · 배달 흐름 기반 지역 매칭 플랫폼

다중 사용자 환경에서의 역할 분리와  
상태 기반 주문/배달 흐름 관리에 초점을 맞춘  
Spring Boot 기반 실시간 웹 서비스 프로젝트

<br>

<img src="https://img.shields.io/badge/Java-17-orange?style=for-the-badge">
<img src="https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge">
<img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge">
<img src="https://img.shields.io/badge/WebSocket-STOMP-blue?style=for-the-badge">
<img src="https://img.shields.io/badge/JPA-Hibernate-blue?style=for-the-badge">
<img src="https://img.shields.io/badge/Oracle_DB-F80000?style=for-the-badge">
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge">
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge">

<br><br>

![GitHub last commit](https://img.shields.io/github/last-commit/Ahn0204/everyoneBread_backend)
![GitHub repo size](https://img.shields.io/github/repo-size/Ahn0204/everyoneBread_backend)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Ahn0204/everyoneBread_backend)

</div>

---

# 📌 Project Introduction

모두의빵은  
사용자(USER), 판매자(SHOP), 배달기사(RIDER), 관리자(ADMIN) 환경에서  
권한 분리, 상태 기반 주문 흐름, 실시간 통신(WebSocket)을 중심으로 설계한  
Spring Boot 기반 주문·배달 플랫폼입니다.

단순 CRUD 기능 구현을 넘어  
실제 서비스 흐름과 유지보수성을 고려한 구조 설계 경험을 목표로 개발했습니다.

---

# 👨‍💻 Project Overview

| 항목 | 내용 |
|---|---|
| 프로젝트명 | 모두의빵 |
| 개발 기간 | 2025.10 ~ 2026.01 |
| 개발 인원 | 3인 팀 프로젝트 |
| 담당 역할 | 인증·보안 설계 / 주문·배달 도메인 설계 / 실시간 통신 구조 구현 |
| 개발 환경 | Spring Boot 기반 웹 서비스 |

---

# ✨ Key Features

| 기능 | 설명 |
|---|---|
| 🔐 인증 시스템 | Spring Security 기반 인증 및 권한 처리 |
| 👥 역할 분리 | USER / SHOP / RIDER / ADMIN 권한 분리 |
| 📦 주문 관리 | 상태 기반 주문 흐름 처리 |
| 🛵 배달 시스템 | 라이더 배달 상태 관리 |
| ⚡ 실시간 처리 | WebSocket(STOMP) 기반 상태 동기화 |
| 🛠 관리자 시스템 | 회원 및 서비스 운영 관리 |
| ☁ 운영 환경 | AWS EC2 기반 배포 및 운영 |

---

# 🛠 Tech Stack

<div align="center">

| Backend | Frontend | Database | Infra |
|---|---|---|---|
| Java 17 | HTML5 | Oracle DB | AWS EC2 |
| Spring Boot | CSS3 | JPA | GitHub |
| Spring Security | JavaScript | Hibernate | Git |
| WebSocket(STOMP) | jQuery | MyBatis |  |
| Hibernate | Thymeleaf |  |  |

</div>

---

# 📌 Service Architecture

```text
USER / SHOP / RIDER / ADMIN

                ↓

Spring Security 기반 인증 및 권한 처리

                ↓

Controller → Service → Repository

                ↓

WebSocket(STOMP) 실시간 이벤트 처리

                ↓

Oracle DB
```

---

# 📂 Project Structure

```text
com.ex
 ┣ admin
 ┣ alert
 ┣ common
 ┣ delivery
 ┣ member
 ┣ order
 ┣ product
 ┣ rider
 ┣ shop
 ┣ websocket
```

---

# 🧩 Service Flow

## 👤 사용자 흐름

회원가입  
→ 로그인  
→ 상품 조회  
→ 주문 요청  
→ 주문 상태 확인  
→ 배달 현황 조회

---

## 🏪 판매자 흐름

판매자 로그인  
→ 주문 확인  
→ 주문 수락 / 거절  
→ 상품 준비 상태 변경  
→ 라이더 배차 요청

---

## 🛵 라이더 흐름

라이더 로그인  
→ 배달 요청 확인  
→ 배달 수락  
→ 배달 시작  
→ 배달 완료 처리

---

## 🛠 관리자 흐름

관리자 로그인  
→ 회원 관리  
→ 판매자 승인 및 제재 처리  
→ 주문/배달 상태 모니터링  
→ 공지사항 관리  
→ 서비스 운영 및 통계 관리

---

# 👨‍💻 My Focus

프로젝트에서  
인증 및 권한 구조, 주문·배달 상태 흐름, 실시간 이벤트 처리 구조를 중심으로 개발했습니다.

특히 아래 기능 구현에 집중했습니다.

- Spring Security 기반 인증 구조 설계
- ROLE 기반 접근 제어 구현
- 주문/배달 상태 Enum 설계
- 상태 기반 흐름 처리 로직 구현
- WebSocket(STOMP) 기반 실시간 이벤트 처리
- ERD 재설계를 통한 데이터 정합성 개선
- 논리 삭제(Soft Delete) 구조 적용
- AWS EC2 배포 및 운영 환경 구성

---

# 📌 Main Features

## 🔐 인증 및 보안

- Spring Security 기반 인증/인가 처리
- USER / SHOP / RIDER / ADMIN 역할 분리
- CustomAuthenticationProvider 구현
- 로그인 성공/실패 핸들러 분리
- URL 접근 권한 계층화
- BCrypt 기반 비밀번호 암호화
- CSRF 보안 처리

---

## 📦 주문 및 배달 시스템

- 주문 상태 기반 흐름 설계
- 주문 단계별 상태 전이 처리
- 배달 상태 관리
- 라이더 배차 흐름 처리
- 상태 기반 서비스 로직 구성
- 실시간 주문 상태 반영

---

## ⚡ 실시간 통신

- WebSocket(STOMP) 기반 이벤트 처리
- 주문 상태 실시간 반영
- 판매자/라이더 상태 즉시 동기화
- Polling 대비 서버 부하 감소

---

## 🛠 관리자 시스템

- 회원 및 판매자 계정 관리
- 판매자 승인 및 제재 처리
- 주문/배달 상태 모니터링
- 공지사항 관리 기능
- 서비스 운영 통계 관리

---

# 🔥 Trouble Shooting

## 1️⃣ 참조 무결성 문제 해결

### 문제

주문 및 배달 데이터 삭제 시  
참조 무결성 제약으로 인해 삭제가 불가능한 문제 발생

### 해결

ERD 구조를 재설계하고

- ON DELETE CASCADE 적용
- Soft Delete 병행 구조 도입
- 상태 기반 데이터 관리 방식 적용

### 결과

- 데이터 정합성 확보
- 삭제 관련 오류 감소
- 유지보수 가능한 구조 개선

---

## 2️⃣ 실시간 상태 반영 구조 개선

### 문제

주문 상태 변경 시  
클라이언트 화면 갱신 지연 발생

### 해결

Polling 방식 대신  
WebSocket(STOMP) 기반 실시간 이벤트 처리 구조 도입

### 결과

- 상태 즉시 반영
- 불필요한 요청 감소
- 사용자 경험 개선
- 서버 부하 감소

---

# 📚 What I Learned

- 다중 역할 기반 인증 및 권한 구조 설계 경험
- 상태 기반(State Driven) 서비스 설계 경험
- WebSocket(STOMP) 기반 실시간 통신 경험
- 데이터 정합성과 참조 무결성 관리 경험
- 운영 환경(AWS EC2) 기반 배포 경험
- 유지보수성과 확장성을 고려한 백엔드 설계 경험

---

# 🚀 Result

단순 기능 구현을 넘어  
권한 분리, 상태 기반 흐름 관리, 실시간 통신 구조까지 고려하며  
실제 서비스 형태의 백엔드 프로젝트를 경험했습니다.

특히 인증 구조와 실시간 이벤트 처리 구조를 직접 설계·구현하며  
서비스 구조와 유지보수성을 고려하는 개발 경험을 할 수 있었습니다.

---

# 👤 Contributor

안성진  
Backend Developer
