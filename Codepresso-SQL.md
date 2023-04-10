# 데이터베이스
데이터베이스는 혼자 사용하는 엑셀과는 달리 여럿이 공유하여 사용할 목적으로 데이터를 통합 및 관리하기 위해 사용된다.

# DBMS
데이터베이스를 관리하는 프로그램이다. MySQL, Oracle, PostgreSQL, SQL Server, SQLite 등이 있다.

# SQL
데이터베이스에 데이터를 요청하는 언어이다. ANSI, ISO 표준이 있지만 DBMS마다 조금씩 다르고 핵심 문법은 유사하다.

## SQL 예시
Q. 20살 이상 여성 고객의 정보를 얻기 위한 SQL은?

```SQL
SELECT *
FROM customer
WHERE age>=20 AND gender='female'
```

# MySQL
오픈소스 관계형 데이터베이스로 오라클에서 인수하였다. 많이 사용하는 DBMS 중 하나로 2023년 3월 기준으로 DB 랭킹에서 2위를 차지하고 있다. (1위는 오라클)

## MySQL 구조
클라이언트인 Workbench와 서버인 MySQL Server로 구성되어 있다. Workbench에서 어떤 데이터에 대한 요청을 MySQL Server로 보내면 MySQL Server에서 응답을 보내준다.

## MySQL 설치
> https://dev.mysql.com/downloads/installer/

작성하지 않은 부분은 default 옵션으로 두고 넘어가기
1. Choosing a Setup Type에서 Developer Default 옵션 선택
2. Manual은 그대로 두고 넘어가서 Execute
3. Accounts and Roles에서 root 패스워드 설정
4. Apply Configuration에서 Execute 후 finish
5. Connect To Server에서 root, 패스워드 입력 후 체크하여 정상적으로 접속되면 넘어가기
6. Apply Configuration에서 Execute 후 finish
7. Installation Complete에서 Shell은 안쓴다면 체크 해제하고 finish하여 설치를 끝내기

## MySQL 에러 - 3306 포트가 이미 사용중일 경우
원인은 이전에 제거한 MySQL이 동일한 포트를 사용했었기 때문이다. 그래서 포트를 삭제해야한다.

1. Win + R 실행창에서 **resmon.exe** 실행
2. 리소스 모니터에서 **수신 대기 포트** 항목에서 3306포트를 사용중인 PID 확인
3. CMD를 관리자 권한으로 열고 **taskkill /F /PID [PID번호]** 입력하여 삭제
4. MySQL 설치 창으로 돌아가서 TCP/IP 체크를 풀었다가 다시 체크하면 빨간 느낌표 에러표시가 사라진다.

## Workbench
MySQL을 다루기 위한 도구로 SQL을 작성하고 실행시켜서 결과를 볼 수 있다. CSV 파일의 import, export를 지원한다.

## Workbench 에러 - Could not acquire management access for administration
<img src=./img/capture-workbench-error1.png>

> 해결방법 출처  
> https://velog.io/@dongzooo/My-sql-workbench-%EC%97%90%EB%9F%AC%ED%95%B4%EA%B2%B0-could-not-acquire-management-access-for-administration

MySQL에서 Server Status를 누르니까 위와 같은 에러가 발생하여 다음과 같이 해결하였다.

1. 윈도우 -> 설정 -> 시간 및 언어 -> 언어 및 지역 -> 기본 언어 설정
2. 시스템 로캘 변경
3. [Beta: 세계 언어 지원을 위해 Unicode UTF-8 사용] 체크
4. 재부팅

## Workbench 에러 - Cannot Connect to Database Server
<img src=./img/capture-workbench-error2.png>

> 해결방법 출처  
> https://dhan-description.tistory.com/84

Could not acquire management access for administration 에러를 해결하기 위해서 재부팅을 하니까 서비스에서 MySQL이 실행이 안돼고 Workbench에서는 Cannot Connect to Database Server 에러가 발생하여 다음과 같이 해결하였다.

1. C드라이브 -> ProgramData -> MySQL -> MySQL Server 8.0 -> my.ini 파일
2. 내용 중 [mysqld]가 있는 부분에서 port 아래에 **bind-address=127.0.0.1** 입력 후 저장
3. 다시 서비스로 돌아가서 MySQL80 서비스를 시작하여 확인

## MySQL 데이터 타입
일반적으로 데이터 타입은 데이터베이스의 종류마다 다르다.

> MySQL 데이터 타입 공식문서  
> https://dev.mysql.com/doc/refman/8.0/en/data-types.html

- 숫자 Numeric 예시: 나이, 점수, 가격, 아이디 등
- 문자 Character 예시: 이름, 성별, 상품명 등
- 날짜/시간 Date/Time 예시: 저장시점 날짜시간, 수정시점 날짜시간, 가입시점 날짜시간 등

# 데이터베이스의 구성 요소
1. 스키마: 일반적으로 애플리케이션마다 하나가 존재하고, 스케일이 큰 경우 여러개가 존재하는 경우도 있다.
2. 테이블: 애플리케이션의 기능마다 정의한다.
3. 컬럼: 기능에 필요한 요소들을 정의한다.
4. 로우: 하나의 데이터 (레코드)

> 구성 요소의 예시
> - 게시판 스키마
> - 유저 테이블 (unique 아이디 컬럼, 이메일 컬럼, 패스워드 컬럼, 회원가입날짜시간 컬럼)
> - 게시물 테이블 (unique 아이디 컬럼, 유저아이디 컬럼, 게시물제목 컬럼, 게시물내용 컬럼, 게시물작성날짜시간 컬럼)
> - 댓글 테이블 (unique 아이디 컬럼, 유저아이디 컬럼, 게시물아이디 컬럼, 댓글내용 컬럼, 댓글작성날짜시간 컬럼)

# MySQL 스키마 생성 실습
1. 네비게이터 우클릭 Create Schema
2. 이름, 캐릭터셋(utf8), 컬렉션(utf8_general_ci) 설정
3. Apply
4. Finish
5. 생성된 스키마 우클릭 Set as Default Schema 선택하여 기본 스키마로 지정 (이렇게 하면 SQL문 작성 시 스키마 명을 생략할 수 있다.)

# MySQL 테이블 생성 실습
1. basic-table 우클릭 Create Table
2. 테이블명을 정하고 캐릭터셋과 컬렉션은 default로 하면 스키마꺼를 상속받는다.
3. 컬럼을 작성하고 Apply
4. 생성된 테이블을 우클릭하여 Select Rows Limit 1000 눌러서 조회 테스트

# 테이블 옵션
- PK: 테이블당 하나만 존재가능한 유니크한 값 (Not Null)
- NN: Not Null 데이터가 반드시 저장되어야 한다.
- UQ: 유니크한 값 (Null 가능)
- UN: 숫자 입력 시 Unsigned 사용
- AI: Auto Increment 데이터가 늘어날때마다 0부터 1씩 숫자가 늘어난다. (게시물 번호 등에 사용)
- Default: 기본 값 (날짜 등에 사용)

# 예제 데이터 실습
> 실습데이터 다운로드 (MySQL SQL scripts)  
> https://forta.com/books/0672336073/

1. shop 스키마 생성
2. create.txt 내용으로 Query 입력하여 테이블 생성
3. populate.txt 내용으로 Query 입력하여 데이터 추가

# CREATE TABLE
새로운 테이블을 생성한다.

```SQL
CREATE TABLE table_name
(
    column_name1 data_type options,
    column_name2 data_type options,
);
```

# INSERT INTO
테이블에 새로운 row를 추가한다.

```SQL
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);

-- 모든 컬럼에 데이터 입력 시 컬럼 생략 가능
INSERT INTO table_name
VALUES (value1, value2, value3);
```

# SELECT
테이블의 데이터를 조회한다.

```SQL
-- 전체 컬럼 조회
SELECT *
FROM table_name;

-- 특정 컬럼만 조회
SELECT column1, column2
FROM table_name;
```

# WHERE
원하는 조건으로 데이터를 필터링한다.  
SELECT, UPDATE, DELETE 문에서 사용 가능하다.

```SQL
-- Customers 테이블에서 성별이 여성인 사람만 조회
SELECT *
FROM Customers
WHERE gender = 'Female';
```

# 비교 연산자
- 같다: =
- 같지 않다: <>
- 크다: >
- 작다: <
- 크거나 같다: >=
- 작거나 같다: <=

# 조건의 결합
여러 조건들을 결합하여 데이터를 필터링한다.  

## AND 연산자
주어진 모든 조건을 모두 만족시키는 데이터만 조회한다.  

```SQL
-- 서울에 사는 남성 고객의 데이터
SELECT *
FROM Customers
WHERE Address = 'Seoul'
AND gender = 'Male';
```

## OR 연산자
주어진 조건 중 하나라도 만족시키는 데이터만 조회한다.

```SQL
-- 서울 혹은 부산에 사는 고객의 데이터
SELECT *
FROM Customers
WHERE Address = 'Seoul'
OR Address = 'Busan';
```

# ORDER BY
특정 컬럼을 기준으로 내림차순 혹은 오름차순하여 데이터를 정렬한다.  
정렬 조건은 1개 이상 할 수 있다.  
- ASC : 오름차순 (default)
- DESC : 내림차순

```SQL
-- 고객 데이터를 아이디 순으로 내림차순 정렬
SELECT *
FROM Customers
ORDER BY customer_id DESC;

-- 고객 데이터를 아이디 순으로 오름차순, 전화번호로 내림차순 정렬
SELECT *
FROM Customers
ORDER BY customer_id ASC, phone_number DESC;
```

# LIMIT & OFFSET
- LIMIT : 조회된 결과 값의 개수를 제한한다.
- OFFSET : LIMIT과 함께 자주 쓰는 명령으로 몇번째 행부터 출력할지 처리한다.

```SQL
-- 고객 데이터에서 나이가 가장 많은 3명 조회
SELECT *
FROM Customers
ORDER BY age DESC LIMIT 3;

-- 고객 데이터에서 나이가 3, 4번째 많은 사람 조회
SELECT *
FROM Customers
ORDER BY age DESC LIMIT 2 OFFSET 3;
```

# IN 연산자
조회하려는 데이터에서 원하는 데이터를 포함한 데이터를 필터링 할 수 있는 명령이다.

```SQL
-- 고객 데이터에서 '서울' 혹은 '인천'에 거주하는 고객 조회
SELECT *
FROM Customers
ORDER BY address IN ('Seoul', 'Incheon');
```

# BETWEEN 연산자
조회하려는 데이터에서 주어진 범위에 대한 조건에 해당하는 데이터를 필터링 할 수 있는 명령이다.  
숫자, 날짜, 문자 데이터에 사용이 가능하다.  
주어진 범위를 모두 포함한다.  

```SQL
-- 상품 데이터에서 상품 번호가 1000번 ~ 1010번인 데이터 조회
SELECT *
FROM Products
WHERE product_number BETWEEN 1000 AND 1010;
```

# LIKE 연산자
문자열 데이터 안에서 특정 문자열로 시작 또는 끝나거나 포함된 데이터를 검색하기 위해 사용한다.  
'%' 기호를 사용하여 원하는 방식으로 검색할 수 있다.

```SQL
-- "A"로 시작하는 학생의 이름 검색
SELECT name
FROM student
WHERE name LIKE 'A%';

-- "A"로 끝나는 학생의 이름 검색
SELECT name
FROM student
WHERE name LIKE '%A';

-- "A"가 포함된 학생의 이름 검색
SELECT name
FROM student
WHERE name LIKE '%A%';

-- "A로 시작하고 D로 끝나는 학생의 이름 검색"
SELECT name
FROM student
WHERE name LIKE 'A%D';
```