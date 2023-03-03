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
https://velog.io/@dongzooo/My-sql-workbench-%EC%97%90%EB%9F%AC%ED%95%B4%EA%B2%B0-could-not-acquire-management-access-for-administration

MySQL에서 Server Status를 누르니까 위와 같은 에러가 발생하여 다음과 같이 해결하였다.

1. 윈도우 -> 설정 -> 시간 및 언어 -> 언어 및 지역 -> 기본 언어 설정
2. 시스템 로캘 변경
3. [Beta: 세계 언어 지원을 위해 Unicode UTF-8 사용] 체크
4. 재부팅

## Workbench 에러 - Cannot Connect to Database Server
<img src=./img/capture-workbench-error2.png>

> 해결방법 출처
https://dhan-description.tistory.com/84

Could not acquire management access for administration 에러를 해결하기 위해서 재부팅을 하니까 서비스에서 MySQL이 실행이 안돼고 Workbench에서는 Cannot Connect to Database Server 에러가 발생하여 다음과 같이 해결하였다.

1. C드라이브 -> ProgramData -> MySQL -> MySQL Server 8.0 -> my.ini 파일
2. 내용 중 [mysqld]가 있는 부분에서 port 아래에 **bind-address=127.0.0.1** 입력 후 저장
3. 다시 서비스로 돌아가서 MySQL80 서비스를 시작하여 확인