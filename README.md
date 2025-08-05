# pyspark-project

## 프로젝트 개요
이 레포지토리는 VMware 기반 리눅스 가상환경에서 Xshell을 이용해 접속하고, Docker를 활용해 PySpark 컨테이너를 띄워 PySpark 실습을 진행하는 프로젝트입니다.  
PySpark 실습 관련 코드 및 환경 설정 파일들이 포함되어 있습니다.

## 환경 구성

1. **호스트 OS**  
   - VMware Workstation 또는 VMware Player 위에 Ubuntu 등 리눅스 배포판 설치

2. **접속 도구**  
   - Xshell을 이용해 VMware 리눅스 가상머신에 SSH 접속

3. **컨테이너 관리**  
   - Docker 설치 및 실행
   - PySpark가 포함된 Docker 컨테이너 실행

4. **PySpark 실습**  
   - Docker 컨테이너 내부에서 PySpark 작업 수행
   - PySpark 웹 UI (Spark UI)를 통해 작업 상태 모니터링 가능 (기본 포트 8080)

## 시작 가이드

### 1. VMware 리눅스 접속
- VMware에서 리눅스 가상머신을 실행한 후, Xshell로 SSH 접속

```bash
ssh username@ip_address
## 2. PySpark 컨테이너 실행 및 포트 포워딩

기존 컨테이너 종료 및 삭제

```bash
docker compose down

컨테이너 빌드 및 백그라운드 실행
docker compose up --build -d

PySpark 작업 시 생성되는 Spark 웹 UI에 접속 가능

웹 브라우저에서 http://localhost:8080 또는 VMware 리눅스 가상머신 IP와 포트 8080으로 접속하여 UI 확인

## 3. GitHub 저장 및 관리
git add .
git commit -m "Initial commit"
git push
