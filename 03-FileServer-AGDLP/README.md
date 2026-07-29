# File Server & AGDLP 기반 접근 권한 관리

Windows Server 파일 서버 환경을 구축하고,
AGDLP 권한 모델과 NTFS Permission을 적용하여
사용자별 데이터 접근 권한을 관리하는 프로젝트입니다.

---

## 1. Project Overview

### 목표

파일 서버 환경에서 사용자와 그룹 기반의 권한 관리 체계를 구성하고,
데이터 접근 통제를 통한 보안 관리 환경 구축을 목표로 하였습니다.

### 구축 내용

- File Server 구축
- 공유 폴더 구성
- AGDLP 권한 모델 적용
- NTFS Permission 설정
- Windows Server Backup 구성
- 데이터 복구 검증

---

## 2. Environment

| 구분 | 내용 |
|---|---|
| Server OS | Windows Server 2019 |
| Client OS | Windows 10 |
| Directory Service | Active Directory Domain Services |
| File Service | Windows File Server |
| Permission Model | AGDLP |
| Virtualization | VMware Workstation Pro |
| Domain | suntech.local |

---

## 3. Access Control Architecture

Active Directory 사용자 및 그룹 구조를 기반으로
AGDLP 권한 모델을 적용하여 파일 서버 접근 권한 관리 구조를 설계하였습니다.

구성 구조:


User Account

  ↓

Global Group

  ↓

Domain Local Group

  ↓

Shared Folder Permission


AGDLP 구조를 적용하여 사용자와 리소스 권한을 분리하고,
권한 변경 및 관리 효율성을 확보하였습니다.

---

## 4. Implementation

### 4.1 File Server 구축

Windows Server 환경에서 파일 서버를 구성하고,
사용자가 공유 자원에 접근할 수 있는 환경을 구축하였습니다.

구축 내용:

- 파일 서버 역할 구성
- 공유 폴더 생성
- 사용자 접근 환경 구성
- Active Directory 연동


---

### 4.2 공유 폴더 구성

부서별 데이터 관리를 위해 공유 폴더 구조를 구성하였습니다.

구성 예시:


File Server

├── Production
├── Quality
└── Management


사용자 그룹에 따라 필요한 공유 폴더에 접근할 수 있도록
권한 관리 기준을 구성하였습니다.


---

### 4.3 AGDLP 권한 모델 적용

사용자에게 직접 권한을 부여하는 방식이 아닌,
그룹 기반 권한 관리 구조를 적용하였습니다.

구성:


Account

↓

Global Group

↓

Domain Local Group

↓

Resource Permission


AGDLP 모델 적용을 통해 사용자 변경 시 권한 관리 작업을 최소화하고,
확장 가능한 권한 관리 구조를 구현하였습니다.


---

### 4.4 NTFS Permission 설정

파일 및 폴더 접근 제어를 위해 NTFS Permission을 설정하였습니다.

적용 내용:

- 사용자 그룹별 접근 권한 설정
- 읽기 / 수정 권한 구분
- 공유 폴더 접근 제어
- 권한 상속 구조 확인

권한 설정 후 사용자 계정으로 접근 테스트를 수행하여
정상적인 접근 제어 여부를 확인하였습니다.


---

### 4.5 Backup 및 Restore 검증

Windows Server Backup 기능을 활용하여
파일 서버 데이터 보호 환경을 구성하였습니다.

구성 내용:

- 백업 정책 설정
- 데이터 백업 수행
- 복구 테스트 진행
- 데이터 정상 복원 확인


---

## 5. Result

- Active Directory 기반 파일 서버 환경 구축
- AGDLP 기반 그룹 권한 관리 구조 구현
- NTFS Permission 기반 접근 제어 적용
- 사용자별 데이터 접근 권한 관리 환경 구성
- Backup & Restore 기반 데이터 보호 환경 확보


---

## 6. Skills

- Windows File Server
- Active Directory
- AGDLP
- NTFS Permission
- Access Control
- Windows Server Backup
- Backup & Restore
