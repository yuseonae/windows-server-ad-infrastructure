# Active Directory 기반 Windows Server 인프라 구축 프로젝트

Windows Server 환경에서 Active Directory 기반 중앙 인증 인프라를 구축하고,
OU/GPO 기반 운영 보안 정책 및 파일 서버 접근 권한 관리 환경을 구현한 프로젝트입니다.

## Overview

기업 환경에서는 사용자 계정 관리, 보안 정책 적용, 데이터 접근 통제가 안정적인 IT 인프라 운영을 위한 핵심 요소입니다.

본 프로젝트에서는 Active Directory 기반 환경을 구성하고,
중앙 인증 체계 구축부터 운영 보안 정책 적용, 파일 서버 권한 관리까지 단계적으로 구현하였습니다.

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

추후 인프라 구성도 추가 예정

---

## Project Structure

### 01. Active Directory Infrastructure

- Domain Controller 구축
- DNS 서비스 구성
- OU 기반 조직 구조 설계
- 사용자 및 보안 그룹 관리
- 클라이언트 도메인 가입

---

### 02. GPO Security Control

- OU 기반 정책 적용 구조 설계
- Password Policy 구성
- Account Lockout Policy 구성
- USB 저장장치 통제 정책 적용
- gpupdate / gpresult 기반 정책 검증

---

### 03. File Server & Access Control

- 파일 서버 구축
- SMB Share 구성
- AGDLP 권한 모델 적용
- NTFS Permission 설정
- Windows Server Backup 기반 데이터 보호

---

## Repository Structure


windows-server-ad-infrastructure

├── 01-AD-DS-DNS
├── 02-GPO-Security
├── 03-FileServer-AGDLP
└── docs
└── images


---

## Skills

- Windows Server Administration
- Active Directory
- DNS
- Group Policy
- File Server
- NTFS Permission
- AGDLP
- Backup & Restore
