WHERE : R에서 filter와 유사  
ORDER BY : 오름차순 또는 내림차순 정렬. 기본적으로 오른차순 정렬, 내림차순은 DESC 사용 (R과 동일)  
INSERT INTO + VALUES : 한세트!  
NULL : 선언만 하고 할당을 안했을 때 나타남. (맞나?) insert 하고 adding value를 안했을 때 나타남.. (자바스크립트랑 비슷한가?) = 로 확인 불가능. IS NULL 또는 IS NOT NULL 사용.  
UPDATE + SET : 업데이트. SELECT 사용안하면 전체 데이터가 변하니 주의.  
DELETE FROM  
SELECT + LIMIT : 상위 몇개만 보여주기...   
COUNT() : 갯수 세기  
AVG() : 평균값 구하기  
LIKE : WHERE 안에서 특정한 패턴 찾기? % : 0,1,여러 문자 _ : 1,하나의 문자  
IN : OR의 short cut?  
BETWEEN : 범위를 제공. 숫자, 텍스트, 데이터 가능. 사이값 출력 가능  
AS : Aliases(별칭). 이름지정. 한번에 여러개 가능 (,) 합치는 것도 가능 (+)  
JOIN : 열 합치기. (+ON..)  
    (INNER) JOIN : 교집합  
    LEFT (OUTER) JOIN : 왼쪽  
    RIGHT (OUTER) JOIN : 오른쪽  
    FULL (OUTER) JOIN : 합집합  
    self join : 표 안에서 자기 끼리 재구성~
UNION : SELECT 문에서 찾은 걸 결합하는데 사용..  
GROUP BY : = R  
HAVING : WHERE 이랑 비슷한데 집계 함수 사용 가능.  
EXISTS : 하위 쿼리에 레코드가 있는지 테스트... T F 반환  
ANY, ALL : 단일 열 값과 다른 값 범위를 비교  
SELECT INTO : 새 표로 값 복사   
INSERT INTO SELECT : 특정 값 복사..  
CASE : =JAVA. CASE -> WHEN, THEN..ELSE  
PROCEDURE : reuse..?  
주석 : -- ~... or /* */  
<> : not equal to   
+= : Add equals  
-= : Subtract equals  
*= : Multiply equals  
/= : Divide equals  
%= : Modulo equals  
&= : Bitwise AND equals  
^-= : Bitwise exclusive equals  
|*= : Bitwise OR equals  
SOME : 하위 쿼리 중 하나라도 조건에 맞으면 T  
  
# Database
CREATE DATABASE  
DROP DATABASE : DELETE  
BACKUP DATABSE ~~ TO DISK = '경로명'  
CREATE TABLE : 복사도 가능,, AS SELECT FORM WHERE...~  
DROP TABLE : DELETE  
TRUNCATE TABLE : 안의 값만 지우고 테이블 자체는 남겨두기  
ALTER TABLE : 데이터 편집기,,   
    - ADD column_name datatype;  
    - DROP column_name; : delete  
    - MODIFY column_name datatype; : change Data  
Constraints... : 제약넣기  
    - NOT NULL - Ensures that a column cannot have a NULL value  
    - UNIQUE - Ensures that all values in a column are different. 열의 모든 값이 다른가요.  
    - PRIMARY KEY (기본키) - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table. 고유하게 식별.   
    - FOREIGN KEY (외래키) - Prevents actions that would destroy links between tables. 한 테이블의 필드(attribute) 중 다른 테이블의 행(row)을 식별할 수 있는 키  
    - CHECK - Ensures that the valFues in a column satisfies a specific condition. 제한 만들기?  
    - DEFAULT - Sets a default value for a column if no value is specified. GETDATE() 같은 것과,, 사용가능.   
    - CREATE INDEX - Used to create and retrieve data from the database very quickly  
VIEW .. 결과 집합을 기반으로 한.. 가상의 표? (자주 쓰는 data join을 가상의 표로 만들어 둔 것. 스크린 샷 같이!)  
    - CREATE  
    - CREATE OR REPLACE : UPDATE  
    - DROP  