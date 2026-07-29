# Active Directory 기반 Windows Server 인프라 구축 프로젝트

Windows Server 환경에서 Active Directory 기반 제조업 인프라를 구축하고,
OU/GPO 기반 운영 보안 정책 적용 및 파일 서버 접근 권한 관리 환경을 구현한 프로젝트입니다.

---

## Overview

제조업 환경에서는 안정적인 업무 운영을 위해 사용자 계정 관리, 보안 정책 적용,
데이터 접근 권한 통제가 중요합니다.

본 프로젝트에서는 Windows Server 기반 Active Directory 환경을 구축하고,
사용자 및 그룹 관리부터 운영 보안 정책 적용, 파일 서버 권한 관리까지
단계적으로 구현하였습니다.

---

## Environment

| 구분 | 내용 |
|---|---|
| Server OS | Windows Server 2019 |
| Client OS | Windows 10 |
| Directory Service | Active Directory Domain Services |
| DNS | Windows DNS |
| Virtualization | VMware Workstation Pro |

---

## Architecture

추후 Active Directory 인프라 구성도 추가 예정

---

## Project Structure

### 01. Active Directory Infrastructure

Active Directory 기반 도메인 환경을 구축하고 사용자 및 조직 구조를 관리하는 환경을 구성하였습니다.

주요 내용:

- Domain Controller 구축
- DNS 서비스 구성
- OU 기반 조직 구조 설계
- 사용자 계정 및 보안 그룹 관리
- 클라이언트 도메인 가입

---

### 02. GPO Security Control

Group Policy 기반 운영 보안 정책을 적용하여 사용자 환경 및 보안 설정을 관리하였습니다.

주요 내용:

- OU 기반 정책 적용 구조 설계
- Password Policy 구성
- Account Lockout Policy 구성
- USB 저장장치 통제 정책 적용
- gpupdate / gpresult 기반 정책 적용 검증

---

### 03. File Server & Access Control

파일 서버 환경을 구축하고 그룹 기반 권한 관리 체계를 적용하여 데이터 접근을 통제하였습니다.

주요 내용:

- 파일 서버 구축
- 공유 폴더 구성
- AGDLP 권한 모델 적용
- NTFS Permission 설정
- Windows Server Backup 기반 데이터 보호

---

## Repository Structure


```text
windows-server-ad-infrastructure

├── 01-AD-DS-DNS
│   └── README.md
│
├── 02-GPO-Security
│   └── README.md
│
├── 03-FileServer-AGDLP
│   └── README.md
│
└── docs
    └── images
```


---

## Skills

- Windows Server Administration
- Active Directory
- Group Policy
- DNS
- File Server
- AGDLP
- NTFS Permission
- Windows Server Backup
