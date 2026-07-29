# Active Directory Domain Services & DNS 구축

Windows Server 환경에서 Active Directory 기반 중앙 관리 인프라를 구축하고,
사용자 계정 및 시스템을 효율적으로 관리할 수 있는 도메인 환경을 구성한 프로젝트입니다.

---

## 1. Project Overview

### 목표

Active Directory 기반 중앙 인증 환경을 구축하고,
조직 내 사용자 및 시스템 관리 체계를 구성하는 것을 목표로 하였습니다.

### 구축 내용

- Domain Controller 구축
- Active Directory Domain Services(AD DS) 설치
- Windows DNS 구성
- OU 기반 조직 구조 설계
- 사용자 및 보안 그룹 관리
- 클라이언트 PC 도메인 가입

---

## 2. Environment

| 구분 | 내용 |
|---|---|
| Server OS | Windows Server 2019 |
| Client OS | Windows 10 |
| Directory Service | Active Directory Domain Services |
| DNS | Windows DNS |
| Virtualization | VMware Workstation Pro |
| Domain | suntech.local |

---

## 3. Architecture

추후 Active Directory 인프라 구성도 추가 예정


구성 환경:


Active Directory Domain
|
|
ST-DC01
Domain Controller
AD DS / DNS

    |

ST-CL01
Windows 10 Client


---

## 4. Implementation

## 4.1 Domain Controller 구축

Windows Server 2019 환경에서 Active Directory Domain Services 역할을 설치하고
Domain Controller를 구축하였습니다.

구축 내용:

- AD DS 역할 설치
- 도메인 생성
- Domain Controller 구성
- 사용자 및 시스템 중앙 관리 환경 구축


---

## 4.2 DNS 서비스 구성

Active Directory 도메인 환경의 정상적인 인증과 시스템 간 통신을 위해
Windows DNS 서비스를 구성하였습니다.

구성 내용:

- 도메인 이름 해석 환경 구성
- Domain Controller 기반 DNS 연동
- 클라이언트 도메인 접근 환경 구성


---

## 4.3 OU 기반 조직 구조 설계

조직 구조를 Active Directory 환경에 반영하기 위해
부서 단위 OU 구조를 설계하였습니다.

구성:


suntech.local

├── Production
├── Quality
└── Management


OU 구조를 기반으로 사용자 및 컴퓨터 객체를 관리하고,
향후 Group Policy 적용 기준으로 활용할 수 있도록 구성하였습니다.


---

## 4.4 사용자 및 보안 그룹 관리

사용자 계정을 개별적으로 관리하는 방식이 아닌
보안 그룹 기반 관리 구조를 적용하였습니다.

구성:


User

↓

Security Group

↓

Resource Access


보안 그룹을 활용하여 사용자 관리와 권한 관리를 분리하고
관리 효율성과 확장성을 확보하였습니다.


---

## 4.5 Client Domain Join

Windows 10 Client PC를 Active Directory 도메인에 가입시켜
도메인 계정을 이용한 중앙 인증 환경을 구성하였습니다.

검증 내용:

- 클라이언트 도메인 가입 확인
- 도메인 계정 로그인 확인
- 공유 자원 접근 확인


---

## 5. Result

- Active Directory 기반 중앙 관리 환경 구축
- 사용자 및 시스템 관리 체계 구성
- OU 기반 조직 구조 설계
- DNS 연동을 통한 안정적인 도메인 환경 구성
- 도메인 기반 인증 환경 구현


---

## 6. Skills

- Windows Server Administration
- Active Directory Domain Services
- Windows DNS
- OU Design
- User & Group Management
- Domain Join
