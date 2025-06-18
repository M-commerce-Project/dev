# 아는사람마켓

아는사람마켓은 지인 기반의 신뢰할 수 있는 중고 거래 환경을 제공하는 애플리케이션입니다. 본 프로젝트는 효율적인 개발과 안정적인 서비스를 위해 다음 기술 스택을 활용합니다.

## 1. 백엔드 (Backend)

* **언어:** Java 17+
* **프레임워크:** Spring Boot 3.x
    * Spring Security (인증 및 권한 관리)
    * JPA / Hibernate (데이터베이스 ORM)
* **빌드 도구:** Gradle
* **주요 기능:** 사용자 관리, 인증/인가, 연락처 기반 지인 매칭 로직, 상점/아이템 CRUD, 메시징 기능, AWS 서비스 연동.

## 2. 프론트엔드 (Frontend)

* **프레임워크:** Vue.js 3.x (Composition API)
* **라우터:** Vue Router
* **상태 관리:** Pinia
* **HTTP 통신:** Axios
* **빌드 도구:** npm (Vite)
* **주요 기능:** 회원가입/로그인 UI, 상점/아이템 관리 UI, 지인 상점 목록 UI, 아이템 상세 UI, 반응형 웹 디자인.

## 3. 데이터베이스 (Database)

* **종류:** MySQL 8.x
* **환경:** AWS RDS (Managed Database Service)
* **주요 스키마:** users, user_contacts, shops, shop_visibility, items 테이블. (수정중)

## 4. 인프라 및 클라우드 (Infrastructure & Cloud)

* **클라우드 서비스:** Amazon Web Services (AWS)
    * **애플리케이션 서버:** AWS EC2 (Spring Boot 애플리케이션 호스팅)
    * **스토리지:** AWS S3 (아이템 이미지 및 파일 저장
    * **데이터베이스:** AWS RDS for MySQL
* **컨테이너 (선택적):** Docker (EC2 내 애플리케이션 배포 및 관리 용이성 증대)

## 5. CI/CD (Continuous Integration / Continuous Delivery)

* **버전 관리 시스템:** GitHub
* **자동화 도구:** GitHub Actions
* **주요 파이프라인:**
    * 코드 푸시 시 자동 빌드 및 테스트 (CI).
    * `main` 브랜치 병합 시 AWS EC2 (백엔드) 및 S3/CloudFront (프론트엔드)로 자동 배포 (CD).
    * 이를 통해 개발 프로세스의 효율성 및 배포 안정성 확보.

---

