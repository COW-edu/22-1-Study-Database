# **과제 내용**
1. 대표적인 DBMS 조사

2. 대표적인 DBMS의 최신 버젼 조사
3. 회사에서 사용하는 DBMS 종류
---

# DBMS
데이터베이스 관리 시스템(영어: database management system, DBMS)은 다수의 사용자들이 데이터베이스 내의 데이터를 접근할 수 있도록 해주는 소프트웨어 도구의 집합이다. DBMS은 사용자 또는 다른 프로그램의 요구를 처리하고 적절히 응답하여 데이터를 사용할 수 있도록 해준다.


## **RDBMS**

### **장점**

- RDBMS는 위에서 설명을 하였듯이 정해진 스키마에 따라 데이터를 저장하여야 하므로 명확한 데이터 구조를 보장하고 있음.
- 또한 관계는 각 데이터를 중복없이 한 번만 저장할 수 있음.

### **단점**

- 테이블간테이블 간 관계를 맺고 있어 시스템이 커질 경우 JOIN문이 많은 복잡한 쿼리가 만들어질 수 있음.
- 성능 향상을 위해서는 서버의 성능을 향상 시켜야하는 Scale-up만을 지원합니다. 이로 인해 비용이 기하급수적으로 늘어날 수 있음.
- 스키마로 인해 데이터가 유연하지 못합니다. 나중에 스키마가 변경 될 경우 번거롭고 어려움.

RDBMS는 데이터 구조가 명확하며 변경 될 여지가 없으며, 명확한 스키마가 중요한 경우 사용하는 것이 좋음. 또한 중복된 데이터가 없어(데이터 무결성) 변경이 용이하기 때문에 관계를 맺고 있는 데이터가 자주 변경이 이루어지는 시스템에 적합함.

## **NoSQL**

### **장점**

- NoSQL에서는 스키마가 없기 때문에 유연하며 자유로운 데이터 구조를 가질 수 있음. 언제든 저장된 데이터를 조정하고 새로운 필드를 추가할 수 있음
- 데이터 분산이 용이하며 성능 향상을 위한 Saclue-up 뿐만이 아닌 Scale-out 또한 가능함.

### **단점**

- 데이터 중복이 발생할 수 있으며 중복된 데이터가 변경 될 경우 수정을 모든 컬렉션에서 수행을 해야 함.
- 스키마가 존재하지 않기에 명확한 데이터 구조를 보장하지 않으며 데이터 구조 결정가 어려울 수 있음.

NoSQL은 정확한 데이터 구조를 알 수 없고 데이터가 변경/확장이 될 수 있는 경우에 사용하는 것이 좋음. 또한 데이터 중복이 발생할 수 있으며 중복된 데이터가 변경될 시에는 모든 컬렉션에서 수정을 해야하므로 주로 Update가 많이 이루어지지 않는 시스템이 좋음.

또한 Scale-out이 가능하다는 장점을 활용해 막대한 데이터를 저장해야 해서 Database를 Scale-Out를 해야 되는 시스템에 적합함.

### etc

이 외에도 IMDBMS, CDBMS 등이 있으며, 계층구조로도 종류를 분류할 수 있다.

ref: https://khj93.tistory.com/entry/Database-RDBMS%EC%99%80-NOSQL-%EC%B0%A8%EC%9D%B4%EC%A0%90


# 1. 대표적인 DBMS
## Oracle DB
미국 오라클사(社)의  관계형 DB 관리 시스템(RDBMS)으로 PL/SQL를 지원한다.

* RDBMS(Relational Database Management System): 관계형 모델을 기반으로 하는 데이터베이스 관리 시스템

* PL/SQL:  오라클 DBMS에서 SQL언어를 확장하기 위해 사용하는 컴퓨터 프로그래밍 언어중 하나. 표준에 가까움.

### 특징
* 대규모 DB를 지원하며 MSSQL, MYSQL보다 대량의 정보관리시 가장 좋은 성능을 보임

* 고성능 트랜잭션 처리 제공으로 빠른 속도

* SQL문을 효율적으로 처리

* 서버가 운영되려면 인스턴스가 메모리에 할당되어야 하고, 이를 위해선 파라미터 파일이 필요

* 통신시 Listener라는 것을 통해 외부 클라이언트와 통신

* 비싸다.

ref: https://t-okk.tistory.com/160


## Microsoft SQL Server

Microsoft사에서 만든 DBMS로, 확장성이 뛰어남.

### 특징
* 모든 버젼의 Windows에서 매우 잘 작동(윈도우와 찰떡궁합)

* 데이터 클러스터링(그룹, 군집화) 가능

* 중앙집중식 데이터베이스 제어

* Windows에서만 사용 가능

ref: https://altitudetvm.com/ko/komputer/1459-pengertian-microsoft-sql-server-fungsi-kelebihan-dan-kekurangannya.html


## PostgreSQL

PostgreSQL은 객체-관계형 데이터베이스 시스템(ORDBMS)으로, 엔터프라이즈급 DBMS의 기능과 차세대 DBMS에서나 볼 수 있을 법한 많은 기능을 제공하는 오픈소스 DBMS다.

### 특징

* 객체-관계형 데이터베이스 시스템(ORDBMS)임
* ACID 및 트랜잭션 지원
* 다양한 인덱싱 기법 지원
* 유연한 Full-text search 기능
* 동시성 성능을 높여주는 MVCC 기능
* 다양하고 유연한 복제 방식 지원
* 다양한 프로시져(PL/pgSQL, Perl, Python, Ruby, TCL, 등)/인터페이스 언어(JDBC, ODBC, C/C++, .Net, Perl, Python, 등)
* 질 좋은 커뮤니티 지원 및 상업적인 지원
* 질 좋은 문서 풀
* DB Link 기능

ref: https://d2.naver.com/helloworld/227936

## MongoDB

문서 지향적(Document-Oriented) NoSQL 데이터베이스중 하나로, Humongous(거대한) Database를 줄인 약자인 MongoDB로 이름지어짐.

원래는 AGPL 라이선스였으나 2018년 10월에 SSPL v1.0 라이선스로 변경됨. ->이로 인해 논란된 부분 있음

### 특징

* 오픈소스(공유오픈소스)임.(논란 有)
* NoSQL임.
* 도큐먼트 데이터베이스
    * MongoDB는 JSON 형식으로 데이터 관리
* Schema-less 구조와 비정형 스키마로 인한 유연한 스키마
* 비(非)관계형 데이터베이스
* 비(非)트렌젝션
    * 도큐먼트 단위로 처리
    * 트랜젝션 미지원으로 commit, rollback 개념 없음
-> 모두 Auto Commit처리  

ref: 

https://meetup.toast.com/posts/274
https://tech.kakao.com/2021/09/08/opensource-license/

## SQLite

C언어로 개발된 embeded 데이터베이스 엔진으로 독립적이고, 서버가 필요없으며 트렌젝션이 가능한 SQL 데이터베이스 엔진이다.

- 경량화: SQLite Library는 1MB ~ 0.6MB 이하이다. 또한 보통의 파일시스템 컨트롤 보다 약 30% 빠르다.
- 독립적: 표준 C 라이브러리를 통해 개발되었으며, 외부 라이브러리 또는 인터페이스에 종속적인 부분은 없으며, 단순 운영체제 위에서 독립적으로 잘 작동함.
- 신뢰성: SQLite는 많은 스마트폰, IoT장치, 데스트콥 어플리케이션에서 오래 사용되었다. 수치로 했을 경우, 몇억개의 사용처가 10년 넘게 유지되었으며, 아직까지 업데이트하며 유지보수(지속적인 오픈소스 개발 기여)가 되고 있다.
- 무서버: 데몬을 띄우는 보통의 RDBMS와 달리 서버없이 디스크 I/O를 통해 DB에 접근한다(Neo-Serverless, Application과의 같은 프로세스가 아닌 별도의 프로세스 지만, 그 별도의 프로세스는 Application이 관리하에 존재한다. 결국 Serverless이다. ).
- 무설정: 무서버의 특징으로 인해, 서버 프로세스의 설치, 설정, 초기화(가동), 관리, 트러블슈팅 등의 작업이 존재하지 않기 때문에 편리하다.
- 오픈소스: 오픈소스 라이센스는 public Domain으로 라이센스가 존재하지는 않지만, 지속적인 개발과 매 릴리즈마다 엄격한 테스트 과정이 존재한다. 최신 릴리즈 버전은 2019년 12월로, 20주년 된 오픈소스 프로젝트이다.
- 1개의 데이터 파일: 모든 데이터를 1개의 디스크 파일로 표현할 수 있다.
- 크로스 플랫폼 데이터 파일: 32bit / 64Bit, Big / Little Endian, 운영체제 상관없이 데이터 파일을 사용할 수 있다(VFM을 사용하기 때문).


ref: https://ehdvudee.tistory.com/23
https://crystalcube.co.kr/89

## MariaDB

오픈소스 관계형 데이터베이스 관리 시스템(RDBMS)로 MySQL과 동일한 소스코드를 기반으로 만들어졌으며 GPL v2 라이선스를 따른다.

MySQL 라이센스 정책에 대한 대안으로 만들어졌으며, MySQL APIs와 호환성이 매우 좋다(거의 같다).

또한 사용방법과 구조가 MySQL과 동일하다.

기존에 MySQL 엔터프라이즈에서 플러그인으로 제공한 쓰레드풀 기능이 내장됐으며, 스토리지 엔진을 활용한 샤딩 기술을 제공한다. 즉, MySQL의 오픈소스 버전을 넘어 모든 버전을 대체할 수 있는 특징들을 갖추고 있다.

### 특징

- 멀티 소스/병렬 복제
- Global Transaction ID로 안정성 강화
- ROLE 기반 권한 관리 지원
- 카산드라, TokuDB, Connect, 스파이더 스토리지 엔진 추가
- 서브 쿼리 개선 : EXISTS-to-IN
- Slow Query Log 로깅과 동시에 실행계획을 같이 출력.
- 세션별 메모리 사용량 추적 기능
- Insert/Update/Delete 문 EXPLAIN 지원
- 중소기업 및 개인 프로젝트에서의 활용도가 좋음

ref: https://rockplace.co.kr/dbms/mariadb/

https://kodori-sw-programmer.tistory.com/entry/2-RDBMS-%EC%9D%98-%EC%A2%85%EB%A5%98-%EB%B0%8F-%ED%8A%B9%EC%A7%95

## MySQL
세계에서 가장 많이 쓰이는 오픈소스 관계형 데이터베이스 관리 시스템(RDBMS)이다.

C, C++로 만들어졌으며 다중 스레드, 다중 사용자 형식의 구조질의어 형식의 데이터베이스 관리 시스템으로서 현재는 최종적으로 오라클에게 인수되어 오라클이 관리 및 지원하고 있다.

MySQL은 대부분 ANSI C로 구현되었다.

### 특징


-  오픈 소스 라이센스이며, 무료이다.

-  다양한 운영체제에서 사용할 수 있으며, 다양한 프로그래밍 언어(C/C++, python, ruby, perl, PHP 등)의 API를 지원한다.

- 크기가 큰 데이터 집합도 아주 빠르고 효과적으로 처리할 수 있다.

-  널리 알려진 표준 SQL 형식(Structured Query Language)을 사용한다.

-  MySQL 응용 프로그램을 사용자 용도에 맞게 수정이 가능하다.

-  다중 플렛폼 데이터베이스를 처리할 수 있다.

- 웹 애플리케이션으로서의 MySQL의 인기는 PHP의 인기도와 맞물려있다.

ref: 

http://www.tcpschool.com/mysql/mysql_intro_intro

https://altitudetvm.com/ko/komputer/1522-15-kelebihan-dan-kekurangan-mysql-server-yang-p

https://velog.io/@fall031/TIL-37.-MySQL

https://blog.siner.io/2021/10/11/rdbms-comparison/

# 2. 대표적인 DBMS의 최신 버젼 조사

# OracleDB
## Oracle 21C

- 네이티브 블록체인 테이블을 통한 향상된 멀티 모델 지원
- JSON 형식 지원
    - JSON 저장 지원
    - 병렬 SQL분석 가능
    - 여러개의 JSON 문서와 Collection들간에 복잡한
Join 가능

- JavaSrcipt 실행 지원(PL/SQL과 동일 수준)
    - In-DB Graal VM 엔진
    - JavaScript내 데이터 Type과
Oracle 데이터베이스 데이터
Type은 상호 자동 매핑되어 처리
- 샤딩(NoSQL 기술)을 통한 대용량 데이터 분산저장
- AutoML 과 같은 멀티 워크로드 개선

ref: https://velog.io/@sezzzini/DB-Oracle-%EB%B2%84%EC%A0%84%EB%B3%84-%ED%8A%B9%EC%A7%95

https://www.mktg.co.kr/oracle/eDM/210224_Oracle/session_01.pdf

# Microsoft SQL Server

## SQL Server 2019(15.x)

- 데이터 가상화 및 SQL Server 2019 빅 데이터 클러스터
- 지능형 데이터베이스
- 메모리내 데이터베이스 기술로 성능이 빨라졌다.
- 중요 업무용 보안이 좋아졌다.
- 고가용성
    - 그룹 내에서 자동 장애 조치가 수행되도록 이 그룹을 5개 복제본으로 구성할 수 있다. 등
- 그래프 및 공간 데이터 형식에 대한 향상된 기능, UTF-8 지원

ref: 
https://docs.microsoft.com/ko-kr/sql/sql-server/what-s-new-in-sql-server-ver15?view=sql-server-ver15

https://docs.microsoft.com/ko-kr/sql/sql-server/editions-and-components-of-sql-server-version-15?view=sql-server-ver15

# PostgreSQL

## PostgreSQL 11
- 파티션 테이블 견고성과 성능 향상
    - 해시 파티션 테이블 지원 -> 나열 list 파티션, 범위 range 파티션과 함께 파티션 키로 해시 키를 사용할 수 있게 됨.
- 병렬 처리 기능 향상
    - 순차적 병렬 탐색 비용이 줄었으며, 파티션 테이블 대상 해시 조인 작업에서도 병렬 처리가 가능
    - 여러 자료 정의 명령(DDL)에 대해서도 병렬 처리 가능
- 표현식 처리용 JIT(Just-in-Time) Compilation (JIT 컴파일러를 통한 짜깁기) 지원
    - 쿼리 실행 중 특정 표현식의 실행을 더 빠르게 하며 LLVM 프로젝트에서 제공하는 JIT 라이브러리를 이용하여, WHERE 절에 있는 표현식, 대상 목록, 집계함수, 예측, 몇몇 내부 연산 등의 처리 속도를 높임.

ref: https://www.postgresql.org/about/press/presskit11/kr/


# SQLite

## 2.3.0-alpha(2022년 2월 23일)
- API 변경사항 있음

## 2.2.0(2021년 12월 15일)
- SupportSQLiteDatabase에 execPerConnectionSQL()의 기본 메서드를 추가

# MariaDB

## MariaDB 10.6

- Atomic DDL 안전성 개선
    - 10.6 버전부터는 CREATE TABLE, ALTER TABLE, RENAME TABLE, DROP TABLE, DROP DATABASE 및 관련 DDL 문은 비정상 종료에 안전하도록 개선
-   INNODB(MySQL데이터베이스 엔진 이름) Bulk Insert시 속도를 최적화 -> 롤백 상태이거나 insert 작업에 영향을 주는 롤백일 때, 유지될 exclusive table lock으로 빈 테이블 또는 파티션에 대한 삽입을 커버하여 Insert시 빠른 속도로 처리가 가능함.
- 변수명, 예약어 변경사항 有
    - 클러스터(Galera Cluster) 관련 변수 변경사항 및, 추가/삭제된 변수, 예약어 추가 있음

- 문자셋이 utf8에서 utf8m3으로 변경됨
- 시스템 변수 기본값 변경됨
    - 메모리의 버퍼 풀과 OS캐시에 중복 저장되는 더블 버퍼링을 막아 메모리를 효율적으로 사용할 수 있는 O_DIRECT를 기본값으로 채택함.
- SQL 구문 변경 사항 있음

- ORACLE와의 호환성 
    - ORACLE 호환을 위해 몇 가지 함수 및 기능이 추가됨
- 스토리지 엔진 변화
    - 토쿠DB(TokuDB) 엔진과 카산드라(Cassandra) 엔진이 제거됨.

ref: https://www.samsungsds.com/kr/insights/mariadb.html


# MySQL

## MySQL 8.0.28 (2022-01-18, General Availability)

- 문자셋 지원 변경
    
- InnoDB 버그 수정 및 알려진 버그 有 
    - 몇가지 컴파일러 경고와 컴파일 문제 해결
    - 시스템 curl 라이브러리에 연결하지 않고 curl을 포함하는 바이너리 패키지가 curl 7.80.0을 사용하도록 업그레이드됨
- 데이터 타입(CHAR, TIMESTAMP. BIGINT 등) 버그 수정 사항 있음
- 캐릭터셋 미지원
    - ASCII CHARACTER SET latin1, UNICODE CHARACTER SET ucs2 미지원
    - ucs2, macroman, macce ,dec ,hp8 미지원 
- 이벤트 스케줄러 변화 
-  DATE_ADD(), DATE_SUB()함수 버그 개선 및 알려진 버그 有
- 퍼포먼스 스키마 변경 사항 있음
- InnoDB DDL 작업 기능 수정 사항 및 버그 개선

ref: https://dev.mysql.com/doc/relnotes/mysql/8.0/en/news-8-0-28.html

# 3. 회사에서 사용하는 DBMS 종류

1. Oracle DB
2. MySQL
3. Microsoft SQL Server
4. PostgreSQL
