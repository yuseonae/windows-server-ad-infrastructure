# Group Policy 기반 운영 보안 통제

Active Directory 환경에서 OU 구조와 Group Policy를 활용하여
사용자 및 시스템 보안 정책을 중앙에서 관리하는 운영 보안 통제 프로젝트입니다.

---

## 1. Project Overview

### 목표

Active Directory 기반 환경에서 사용자 계정 및 시스템에 대한
보안 정책을 중앙에서 관리하고 운영 보안 수준을 향상시키는 것을 목표로 하였습니다.

### 구축 내용

- OU 기반 정책 적용 구조 설계
- Group Policy 기반 보안 정책 적용
- Password Policy 구성
- Account Lockout Policy 구성
- USB 저장장치 접근 통제 정책 적용
- 정책 적용 결과 검증

---

## 2. Environment

| 구분 | 내용 |
|---|---|
| Server OS | Windows Server 2019 |
| Client OS | Windows 10 |
| Directory Service | Active Directory Domain Services |
| Policy Management | Group Policy Management Console |
| Virtualization | VMware Workstation Pro |
| Domain | suntech.local |

---

## 3. Security Policy Architecture

Active Directory OU 구조를 기준으로 Group Policy를 적용하여
조직 단위별 보안 정책 관리 환경을 구성하였습니다.

구성 구조:


Active Directory Domain
|
|
Organizational Unit (OU)

├── Production
├── Quality
└── Management

    |

Group Policy

├── Password Policy
├── Account Lockout Policy
└── USB Control Policy


---

## 4. Implementation

## 4.1 OU 기반 정책 적용 구조 설계

Active Directory 환경에서 조직 구조에 맞는 OU를 구성하고,
OU 단위로 Group Policy를 적용할 수 있도록 정책 적용 구조를 설계하였습니다.

구성:


suntech.local

├── Production OU
├── Quality OU
└── Management OU


OU 단위로 정책 적용 범위를 구분하여
관리 효율성과 정책 운영 일관성을 확보하였습니다.

---

## 4.2 Password Policy 구성

도메인 사용자 계정 보안을 강화하기 위해
Group Policy 기반 Password Policy를 적용하였습니다.

적용 내용:

- 비밀번호 최소 길이 설정
- 복잡성 요구 사항 적용
- 비밀번호 변경 주기 설정

이를 통해 사용자 계정의 기본 보안 기준을 수립하였습니다.

---

## 4.3 Account Lockout Policy 구성

반복적인 로그인 실패를 통한 비정상 접근을 방지하기 위해
Account Lockout Policy를 구성하였습니다.

적용 내용:

- Account Lockout Threshold 설정
- Account Lockout Duration 설정
- Reset Account Lockout Counter 설정

정책 적용 후 Event Viewer를 통해
계정 잠금 이벤트 발생 여부를 확인하였습니다.

---

## 4.4 USB 저장장치 접근 통제 정책 구성

비인가 저장장치를 통한 데이터 반출을 방지하기 위해
Group Policy 기반 USB 접근 통제 정책을 적용하였습니다.

적용 내용:

- 이동식 저장장치 접근 제한
- 사용자 PC USB 사용 통제
- OU별 정책 적용 범위 관리

---

## 4.5 정책 적용 및 검증

구성한 보안 정책이 정상적으로 적용되는지 확인하기 위해
클라이언트 환경에서 정책 검증을 수행하였습니다.

검증 방법:

```bash
gpupdate /force
gpresult

확인 내용:

Group Policy 적용 여부 확인
계정 정책 적용 상태 확인
Event Viewer 보안 로그 확인

---

## 5. Result
Active Directory 기반 보안 정책 중앙 관리 환경 구축
OU 기반 정책 적용 구조 구현
사용자 계정 보안 강화
비인가 USB 저장장치 사용 통제 환경 구성
정책 적용 및 검증 절차 확보

---

## 6. Skills
Active Directory
Group Policy Management
Password Policy
Account Lockout Policy
USB Device Control
gpupdate / gpresult
Event Viewer
