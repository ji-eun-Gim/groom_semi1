# 🕵️‍♀️ 실시간 다크웹 OSINT 수집 및 유출 탐지 시스템

## 📌 프로젝트 설명
goorm x kakao : 정보보호 11회차
2025.2.17 - 2025.2.28

본 프로젝트는 다크웹과 딥웹에서 실시간으로 정보를 수집하고,  
사용자 지정 키워드 기반으로 **데이터 유출 및 위협 정황을 자동 탐지**하여  
**디스코드 알림 및 일간 리포트** 형태로 제공하는 OSINT 기반 보안 자동화 시스템입니다.

- 다양한 다크웹 소스를 비정기적으로 크롤링하여 수집  
- 수집 데이터에 대해 중복 제거 및 구조화된 형태로 정제  
- 사용자 등록 키워드가 탐지되면 **디스코드 알림** 즉시 발송  
- 매일 00:00 기준으로 **요약 HTML 리포트 자동 생성**  
- MongoDB에 유저 및 키워드 정보 저장, Elasticsearch에 수집 데이터 저장  
- 향후 키워드 기반 탐지율, 위협 통계 시각화 웹 대시보드 확장 예정  

본 시스템은 **실제 위협 기반 탐지 시나리오**를 포함하고 있으며,  
보안 실무 및 CERT 대응 프로세스를 자동화하는 것을 목표로 설계되었습니다.

---

## 🛠️ 사용 기술 스택

- **Python 3.12.8** : 크롤러, 디스코드 봇, 자동화 스크립트 구현  
- **discord.py** : 사용자 알림 및 리포트 전송 디스코드 봇 개발  
- **MongoDB Atlas** : 사용자 및 키워드 정보 저장  
- **Elasticsearch** : 수집된 OSINT 데이터 저장 및 검색  
- **Docker / Git** : 팀 개발 협업 환경 및 컨테이너 기반 실행  
- **Google Cloud (예정)** : 24/7 운영을 위한 클라우드 호스팅  

---

## 👥 참여자

| 이름     | 역할           | 
|----------|----------------|
| 김지은(팀장) | 프로젝트 기획 및 총괄, 도커 및 db 구성, 코드 통합 보조   | 
| 이순우(부팀장)  | 텔레그램 크롤러, discord 봇 기능 개발, 코드 통합 |
| 이우진  | 다크웹 크롤러 개발, 스케줄러 및 템플릿 제작, 코드 통합 보조     | 
| 조수민  | 다크웹 크롤러 개발, 리포트 알림 기능 개발  | 


docker compose -up  
src/main.py  
! requirement.txt setup !  
