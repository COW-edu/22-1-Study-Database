# Chap5. SQL의 사용법

## 실습 환경 셋업
### 사용된 데이터
[MySQL Employees Sample Database](https://dev.mysql.com/doc/employee/en/)  
### Local Mysql 이용하기
#### Mysql 설치
1. [MySQL Community Server 설치](https://dev.mysql.com/downloads/mysql/)
2. [Sample Database 데이터 다운로드](https://github.com/datacharmer/test_db)
3. MySQL에 데이터 추가
    ```shell
    mysql -uroot -p < employees.sql
    ```
### Docker Mysql 이용하기
1. [Docker](https://www.docker.com/) 설치
2. [Docker Image](https://hub.docker.com/r/genschsa/mysql-employees) pull 받기
   ```shell
   docker pull genschsa/mysql-employees
   ```
3. Docker Container 생성
   ```shell
   docker run --name coin-sample-db -e MYSQL_ROOT_PASSWORD=coindb -d -p 3306:3306 genschsa/mysql-employees 
   ```