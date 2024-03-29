# Spring Framework 소개
- Rod Johnson이 개발
- 2004년 1.0 버전 출시
- 2014년 Spring Boot 1.0 버전 출시
- 2017년 Spring Framework 5.0 버전 출시
- 2020년 기준 Spring Boot 2.x 버전대 출시
- 웹 개발만을 위한 프레임워크는 아니지만 주로 웹 애플리케이션 개발을 위해 활용
- 게시판 같은 토이 프로젝트부터 넷플릭스 같은 대규모 웹 애플리케이션까지 개발 가능
- 국내외 많은 기업들이 핵심 기술로 활용중

# 국내 Spring Framework 채용공고 예시
- NAVER: Java/Kotlin&Spring 기반 서비스 개발 경험 3년 이상
- KAKAO: Java 서버 개발 경력 5년 이상 + Java Spring Framework를 이용한 서버 개발 경험
- toss: Spring MVC, Spring Webflux, Spring Boot, Spring Cloud Gateway, Spring Cloud Config
- LINE: Spring, Spring Boot Framework 사용 경험이 있으신 분
- 특히, 백엔드쪽의 대다수 직군에서 요구!

# Spring Framework의 장점
- 경량화된 Java Framework
- POJO의 사용으로 재사용 가능한 코드 개발 가능
- DI와 AOP의 적용
- Transaction 관리의 편의성
- MVC 아키텍처의 지원
- 테스트가 용이함
- 높은 보안성

## 1. 방대한 프로젝트
- Spring은 22개 카테고리의 수백개의 프로젝트 보유
- 대규모 웹 애플리케이션 개발 및 운영을 위한 거의 모든 기술을 제공

## 2. 끊임 없는 개선
- 최근 SW 시스템은 점점 거대해지고 복잡화
- 더 나은 SW 시스템을 위한 다양한 기술과 아키텍처가 소개되고 있음 (마이크로서비스 아키텍처, NoSQL, 클라우드 컴퓨팅)
- Spring은 변화하는 기술에 빠르게 대응하여 꾸준히 새로운 프로젝트를 출시함 (Spring Cloud, Spring Native, etc)
- 어떠한 기술 변화에도 끊임없이 대응해줄거라는 개발자들의 신뢰를 받고 있음!

# Spring Framework의 단점
## 1. 높은 러닝 커브
- Bean, DI, AOP, 객체지향 설게, 디자인 패턴 등 다양한 개념 이해가 필요함
- Spring Framework는 엔터프라이즈급 대규모 서비스 개발을 위한 목적으로 개발됨
- SW의 유연한 확장성을 위해 다양한 기술들이 내포되어 있음

## 2. 복잡한 설정
- 과거에 많이 나온 말 "Spring Framework는 XML 지옥이다"
- 간단한 웹 애플리케이션 개발을 위해서도 상당한 수준의 설정이 필요 (Spring은 무겁다, 대기업에서나 쓸만하다)
- 하지만 Spring Boot가 출시되며 이러한 문제가 해결됨 (자동화된 설정, 간편화된 의존성 관리)

# Spring Boot 소개
- Spring Framework를 보다 손쉽게 활용할 수 있게 지원하는 기술
- 설정 및 의존성 관리, 애플리케이션 모니터링, 서버의 실행 등을 가볍고 빠르게 수행 가능

# Spring Boot의 주요 기능
- 설정 간편화를 위한 Auto Configuration
- 의존성 관리를 위한 Starter Project
- 배포 프로세스 간소화를 위한 Embedded WAS
- 애플리케이션의 모니터링을 위한 Actuator

# 백엔드 개발
- 웹 서비스의 비즈니스 로직을 처리하는 부분
- 브라우저에서의 사용자 요청을 받아 적절하게 처리 (로직 처리, DB 연동, 외부 시스템 연동 Mail CRM 등)
- Web Framework를 활용하여 개발

# DB 설계/운영
- 웹 서비스의 데이터가 저장될 DB를 설계하고 DBMS를 운영 관리
- 데이터는 웹 서비스의 가장 중요한 요소 중 하나
- DB 분석/설계와 DBMS 운영은 다른 역할이지만 규모가 작은 회사에서는 둘다 할 수 있음
- RDBMS는 Oracle, MySQL, PostgreSQL, MSSQL 등 사용
- NoSQL은 MongoDB, Cassandra, DynamoDB, Elasticsearch 등 사용

# 시스템/인프라 엔지니어링
- 웹 서비스가 운영될 인프라를 설계하고 운영
- 서버, 네트워킹, 스토리지, 보안 등을 설계, 구축, 운영
- 기존에는 온 프레미스 기반의 시스템을 운영
- 최근에는 클라우드 및 컨테이너 기반의 시스템 운영으로 전환중 (AWS, Azure, GCP, NCP, Docker, Kubernetes)

# 웹 프레임워크
SW 개발을 효율적으로 하기 위한 반제품으로 특정 분야의 SW 개발에 필요한 공통 기능을 제공하여 사용자는 프레임워크에 필요한 기능을 추가하여 애플리케이션을 개발
- Spring (Java)
- Flask (Python)
- Django (Python)
- NodeJs (JavaScript)
- Laravel (PHP)
- Rails (Ruby)

# 라이브러리 vs 프레임워크
## 공통점
- 재사용 가능한 미리 구현된 유용한 코드(모듈) 제공
- 특정 목적을 위해 구현된 코드를 사용하여 효율적인 개발 가능

## 차이점
- SW 제어의 흐름을 누가 결정하냐에 따라 차이남
- 라이브러리는 제어권이 사용자가 작성한 코드에 있음 (사용자가 작성한 코드에서 라이브러리의 메소드를 호출하여 사용)
- 프레임워크는 제어권이 프레임워크에 있음 (프레임워크에서 사용자가 작성한 코드를 사용)

# Web
인터넷 상에서 정보를 공유하는 기술이다. 기본적으로 Hyper Text 문서로 작성되고 공유된다.

# Web Browser
원격에 있는 Hyper Text 문서를 읽어서 사람이 보기 좋게 만들어주는 프로그램

# Hyper Text
일종의 문서이다. 링크를 포함하고 있어 다른 문서들과 연결 될 수 있다. 모든 문서는 고유의 주소를 갖고 있다.

# HTML
Hyper Text 웹 페이지를 작성하기 위한 언어이다. 웹 페이지의 구조를 결정하고 각 요소들의 의미를 부여한다.

# HTTP
Hyper Text 웹 페이지를 주고 받기 위한 규약이다. 컴퓨터 간 데이터를 주고 받기 위해서 명확한 약속이 필요한데, IETF와 W3C 같은 국제 표준 단체에서 HTTP에 대한 표준을 정하여 배포하였다. 모든 브라우저나 웹서버는 HTTP 표준에 따라 개발되고 통신한다.

# IP 주소
인터넷에 연결된 기기가 가질 수 있는 네트워크 상의 주소로 IP 주소 정보로 원격 자원을 요청이 가능하다.
- IPv4: 2^32개의 IP 주소가 가능, 기기의 증가로 고갈 예정
- IPv6: 2^128개의 IP 주소가 가능, 외울 수 없을 정도로 복잡

# 공인 IP 주소
- 인터넷 상에 고유한 IP 주소
- IP 주소를 관리하는 기관으로부터 할당받아 사용 가능
- 대륙별, 국가별 할당받은 공인 IP 주소가 존재함
- 누구나 접속가능해야 하는 웹 서버 등은 공인 IP 주소가 필요

# 사설 IP 주소
- 특정 조직 내부에의 사설 네트워크 안에서만 통신 가능한 IP 주소 (기관, 회사, 가정)
- 내부에서는 사설 IP로 통신이 가능, 외부에서는 사설 IP로 기기에 접근이 불가능 (회사의 동일한 공유기에 연결된 컴퓨터 간 사설 IP로 통신 가능, 외부에서는 그 회사 컴퓨터의 사설 IP로 통신 불가)
- 사설 네트워크 간에 사설 IP가 중복되어도 무방함 (회사A의 192.0.0.1 회사B의 192.0.0.1은 중복 가능)

# 호스트명
- IP 주소는 외워서 활용하기 어려움
- 사람이 읽고 외우기 쉬운 형태의 주소가 필요
- 호스트는 인터넷 상에 IP 주소를 가진 기기를 의미
- 예를들어 naver.com, google.com
- 호스트명으로 기기의 IP주소를 찾음

# 로컬호스트
- 현재 작업을 수행 중인 기기를 지칭하는 특수한 호스트명
- IP 주소로는 127.0.0.1로 표현
- 웹 서버를 내 컴퓨터에서 실행했을 경우 로컬호스트로 접속

# Port 주소
- IP 주소는 특정 호스트까지의 주소
- Port는 호스트 내부 프로세스의 네트워크 주소 (FTP서버, Web서버, Mail서버, SSH서버)
- 30.129.75.143:80에서 앞은 IP 주소이고 뒤에 :80이 Port 주소
- 0~65,535 까지 사용가능
- 호스트 내부에서 Port 주소는 유일해야 함

# HTML 실습
https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default

# HTML 태그
https://www.w3schools.com/tags/default.asp

# HTML (Hypertext Markup Language)
- HTML은 서로 연결되어 있고, 정보를 구조적으로 표현하는 언어다.
- HTML은 정보를 구조적으로 표현하기 위해 Tag라는 개념을 사용한다.
- 최상위 태그인 html을 기준으로 내부에 head와 body 태그가 위치한다.
- head 태그는 문서의 부가정보를, body 태그는 문서의 컨텐츠를 담는다.
- HTML의 컨텐츠는 태그로 둘러쌓이고, 브라우저가 컨텐츠를 읽어서 태그에 담긴 방식으로 사용자에게 보여준다.
- 많은 태그가 존재하지만 사용되는 종류는 제한적이므로 모두 외울 필요는 없다.

# CSS (Cascading Style Sheets)
- HTML에 디자인을 위한 태그가 추가되면서 코드가 복잡해짐
- CSS는 HTML 태그의 한계를 극복하기 위한 기술
- HTML 문서를 시각적으로 꾸미는 기능에 집중한 기술
- HTML은 정보, CSS는 디자인에 집중
- 정보와 디자인을 분리하여 HTML의 한계를 극복
- style 태그 내에 CSS 코드를 삽입하여 사용
- CSS 대상 지정에는 HTML 태그명, id, class를 이용
- 태그명은 전체적, id는 개별적, class는 그룹에 적용할 때 자주 사용

# 계층형 아키텍처
- SW 아키텍처는 실제 개발 전 최종 SW의 모습을 설계
- SW 아키텍처는 SW의 구조를 정의한 것, SW를 구성하는 주요 요소들과 요소들의 관계를 정의한 것
- 이미 많은 사람이 고민했던 특정 상황의 문제 해결을 위해 일반화된 솔루션이 있음 (메신저 서비스 개발 패턴, 웹서비스 개발 패턴, 분석 시스템 개발 패턴)
- 웹 서비스 개발에 주로 쓰이는 패턴은 SW를 3~4개 계층으로 구분 (Presentation Layer, Application Layer, Business Layer, Data Access Layer)
- 계층 간에 호출하고 데이터를 주고 받으며 전체 웹 서비스 구성
- Presentation Layer(@Controller): 클라이언트로부터 요청을 받아 Application Layer에 처리를 위임, Application Layer의 결과를 최종 클라이언트로 전달 (요청과 응답 처리)
- Application Layer(@Service): 특정 목적을 위한 다양한 비즈니스 로직을 처리 (비즈니스 로직 처리)
- Data Access Layer(@Repository): DB에 접근하여 데이터를 저장하거나 조회하는 역할 (데이터 저장 조회)

# Spring Controller
- 계층형 아키텍처의 Presentation Layer에 해당한다.
- 클라이언트의 요청을 받고 Application Layer에 요청에 대한 처리를 위임한다.
- 클라이언트에 최종적으로 응답을 하는 역할을 맡는다.
- view: 클라이언트가 요청에 대한 응답의 결과로 보게되는 웹 페이지
- data: 클라이언트가 요청에 대한 응답으로 받는 데이터
- Spring Controller를 구현하기 위해서는 3개의 Annotation이 필요함
- @Controller: 컨트롤러 역할을 하는 클래스 지정, 클래스 상단에 명시, view를 응답 (html)
- @RestController: 컨트롤러 역할을 하는 클래스 지정, 클래스 상단에 명시, data를 응답 (문자열, 숫자, Json, xml)
- @RequestMapping: 특정 요청을 처리하는 메소드 지정, 클래스 또는 메소드 상단에 명시
- Spring Contoller의 메소드는 URI에 따라 호출한다.
- ex) RequestMapping(value = "/user")
- URI는 계층 관계로 표현이 가능하다. ('/'로 계층을 구분)
- /user/paid, /user/enterprise

# Annotation
- Java 소스코드에 추가적인 정보를 제공하는 방법
- @으로 시작하며 클래스, 메소드, 멤버변수, 파라미터에 부착 가능
- 3가지 유형의 Annotation (자바 컴파일러에게 정보제공, SW툴에 의해 사용되어 코드생성 및 추가작업, 런타임 시 특정 동작 추가실행)
- @RequestMapping은 2번째 유형인 SW툴에 의해 사용되어 코드 생성/추가 작업하는 것에 가깝다.
- Annotation들을 Spring Framework에서 스캔하여 특정 목적으로 사용됨

# URI
- Uniform Resource Locator
- 특정한 자원에 접근하기 위한 이름 또는 주소
- ex) https://www.naver.com
- 웹상의 모든 자원들은 URI를 가진다. (웹페이지, 이미지, 영상)
- URI는 중복 시 에러가 발생한다.

# URI 네이밍 규약
- 소문자를 사용한다.
- 명사로 작성한다.
- 두 단어 이상 연결하면 단어 사이에 '-'를 사용한다.
- 일관성을 가지도록 작성한다.

# @RequestMapping
- RequestMapping은 클라이언트의 특정 요청이 오면 Spring Framework에 의해 호출된다.
- RequestMapping이 붙은 메소드가 여러개라면?
- Spring Framework가 URI에 맞는 메소드를 호출한다.

# @RestController
- REST API, HTTP API를 위한 클래스를 명시한다.
- @RestController를 붙인 클래스 내부에서 @RequestMapping을 붙인 개별 메소드들이 API가 된다.
- @RestController를 붙인 클래스에 @RequestMapping을 붙여서 공통적으로 쓸 주소를 쓸 수 있다.
- ex) 클래스에 /user를 매핑, 내부 메소드에 2개에 각각 /paid와 /enterprise 매핑 시 /user/paid와 /user/enterprise가 된다.

# HTTP API
- Application Programming Interface
- Interface: 두 개체 간의 정보를 공유하기 위한 방법
- ex) 키오스크, 리모콘
- API: 컴퓨터 간 정보를 공유하기 위한 방법
- ex) 함수/메소드 호출하는 형식의 API, HTTP 기술로 네트워크를 통한 원격 자원을 호출하는 API

# HTTP API & REST API
- HTTP API: HTTP(S)를 활용하여 원격 데이터를 공유하기 위한 API
- REST API: 웹 상에서 효율적으로 데이터를 공유하기 위한 아키텍쳐 스타일, 다양한 조건이 만족되어야 하지만 실무에서는 모든 조건을 만족하기 어렵다.
- 실무에서는 두가지를 혼용하여 사용하지만 명칭으로는 대부분 REST API라고 부른다.

# 서버 요청 데이터 예시
- 서버에 요청하기 위해서는 추가적인 데이터를 필요로 할 수 있다.
- 페이스북 피드 조회 -> 로그인한 사용자 정보와 페이지 데이터를 요청과 함께 전송한다.
- 블로그 글 작성 -> 사용자 정보와 작성된 제목 및 글의 데이터를 요청과 함께 전송한다.
- 인스타그램 게시물 삭제 -> 사용자 정보와 삭제하려는 게시물의 정보를 요청과 함께 전송한다.

# Request 파라미터
- 클라이언트가 서버에 요청 시 추가적으로 전송하는 데이터
- 대표적인 파라미터 유형: Query String, Path Parameter

# Query String
- URI와 파라미터 영역을 구분하여 사용
- URI 뒤에 ?key1=value1&key2=value2&... 과 같은 형태로 작성된다.
- key는 파라미터명, value는 파라미터값

# Path Parameter
- URI의 일부로 파라미터 값을 사용한다.
- 파라미터값인 계정명이나 숫자값이 URI에 넣어진다.

# Query String & Path Parameter
1. 일반적인 추천 사항
- 특정 자원 요청 시 Path Param 사용
- 정렬 혹은 추가 필터링 데이터는 Query String 사용

2. 다른 추천 사항
- 필수 데이터 Path Param
- 선택적 데이터 Query String
- Path Param이 포함된 URI는 클라이언트가 영향을 받아서 변경 비용 높음
- Query String은 상대적으로 편하게 확장 가능

3. 조직 추천 사항
- 회사 또는 팀마다 표준이 존재하므로 표준에 따라 개발한다.

# @RequestParam (Query String)
- Request 파라미터를 활용하는 Annotation이다.
- name: Query String의 key와 매핑, key와 변수명이 같으면 생략 가능
- required: 필수 여부 (true, false)
- defaultValue: 데이터가 없을경우 설정할 기본 값

# @RequestParam (Path Parameter)
- @RequestMapping value 값으로 넣은 URI에 {}중괄호로 Path Parameter가 들어갈 곳을 표시한다.
- 메소드 파라미터에 @PathVariable 어노테이션을 사용한다.
- 필수 데이터가 아닌 선택적 데이터의 경우 주로 Query String을 사용한다.

# JSON
- JavaScript Object Notation
- 데이터를 교환하는 데 사용
- XML 보다 가볍고 읽기 쉬움
- key와 value를 사용한 형태
- 중괄호로 묶이며, 배열은 대괄호 사용
- 웹 개발 시 가장 일반적인 데이터 포맷
- 프론트엔드는 JSON 형식 데이터를 응답받아서 화면 구성
- 어떤 JSON 데이터로 응답할 지 사전에 정하고 프론트엔드와 백엔드는 거기에 맞게 개발

# RestController의 객체 응답
- 객체를 반환하면 JSON 형식으로 변환하여 데이터가 응답된다.
- 객체를 JSON 형식으로 변환하는 역할은 Spring이 해준다.

# HTTP 메소드
- HTTP 규약 중 하나로서, 특정 자원에 대해 수행하는 행동의 종류를 명시한다. (생성, 조회, 수정, 삭제 등)
- HTTP 메소드 사용 시 단일 URI로 다양한 행동을 정의할 수 있다.
- HTTP 메소드는 9개의 메소드가 존재하지만 보통 4~5개를 주로 사용한다.
- 알맞는 메소드로 처리하지 않아도 상관없지만 설계에 맞추는 것이 권장된다.
- 종류: GET, POST, PUT, DELETE, PATCH, OPTIONS, TRACE, CONNECT, HEAD
- 주로 사용되는 메소드: GET, POST, PUT, DELETE
- GET (자원 조회)
- POST (자원 생성)
- PUT (자원 수정)
- DELETE (자원 삭제)

# 데이터베이스 CRUD
- DB의 4가지 기본 동작을 CRUD라고 부른다.
- C (CRETAE)
- R (Read)
- U (Update)
- D (Delete)

# HTTP 메소드 & 데이터베이스 CRUD
- HTTP 메소드와 데이터베이스 CRUD에서 비슷한 것끼리 대응하여 사용한다.
- Create -> POST (데이터 저장)
- Read -> GET (데이터 조회)
- Update -> PUT (데이터 수정)
- Delete -> DELETE (데이터 삭제)

# Spring의 HTTP 메소드 구현
- @RequestMapping(method = GET) 이와 같은 형식을 사용한다. (default는 GET)
- 요청된 HTTP 메소드에 따라 Java 메소드를 호출한다.
- 각 Java 메소드에서 HTTP 메소드에 따른 처리를 수행하도록 설계가 권장된다.

# 간소화된 HTTP 메소드 Annotation
- @RequestMapping(method = GET) -> @GetMapping
- @RequestMapping(method = POST) -> @PostMapping
- @RequestMapping(method = PUT) -> @PutMapping
- @RequestMapping(method = DELETE) -> @ DeleteMapping

# Request Body
- 게시판 글이나 회원가입 양식 등 크기가 큰 데이터를 보내려면 Query String과 Path Parameter와는 다른 방식이 필요하다.
- Request Body는 데이터를 저장/수정하는 POST, PUT 메소드에서 사용된다. (GET, DELETE는 Query String과 Path Parameter 주로 사용)
- Request Body는 다양한 형식의 데이터를 전송할 수 있다. (주로 사용하는건 JSON 형식)
- 클라이언트 -> JSON 데이터 전송
- Spring -> JSON 데이터를 Java 객체의 파라미터로 저장

# @RequestBody Annotaion
- Spring에서 @RequestBody를 HTTP 메소드의 파라미터 앞에 넣어서 RequestBody를 구현한다.
- Dto 클래스를 만들고 id, title, content 같은 데이터를 받아서 객체로 만든다.

# Request Body를 Postman에서 실습하기
- URI 입력하는 곳 아래의 Body 메뉴 -> raw 체크 -> 오른쪽에 나오는 데이터 형식 JSON 선택
- 텍스트 상자 안에 JSON 형식의 데이터를 작성하고 전송하여 결과 확인

# API 문서
- API를 사용법을 명세한 문서
- API는 정보를 주고 받기 위한 약속
- API는 사용 방법을 알아야 사용 가능

# REST API 문서
- 프론트엔드에서 호출하기 위한 REST API 정보가 명세된 문서
- 백엔드 개발자 주도로 프론트엔드 개발자와 함께 설계
- 프론트엔드 개발자는 REST API 문서에 의존하여 프론트엔드 개발
- 따라서, 프론트엔드에서 활용할 수 있도록 상세하게 작성 필요

# REST API 문서 내용
- REST API 설명
- URI
- HTTP 메소드
- Request 파라미터 (필수 파라미터 & 선택 파라미터)
- Response 데이터 (필수 응답 데이터 & 선택 응답 데이터)
- 에러코드 및 대응방법
- 호출 예시

# REST API 문서 활용
- 프론트엔드 개발자와 백엔드 개발자 모두 REST API 문서를 읽고 이해할 수 있어야함
- 백엔드 개발자는 프론트엔드를 위해 REST API 문서를 작성할 수 있어야함
- REST API가 잘 만들어지면 커뮤니케이션 비용 감소

# Spring Service
- 시스템의 핵심 비즈니스 로직을 구현하는 계층
- view의 종류(프론트엔드 프레임워크)와 DB의 종류에 영향을 받지 않는 독립적인 계층 (영향받지 않도록 설계)

# Spring Service 예시 - SNS 시스템
- 컨텐츠 정보 저장: 이미지, 글 등의 컨텐츠 정보 저장
- 컨텐츠 추천: 사용자 선호 컨텐츠 추천
- 회원 관련 처리: 회원가입, 로그인, 회원탈퇴 등 회원 정보 처리

# Spring Service 구현
- @Service 어노테이션을 클래스에 사용
- 파라미터로 전달된 데이터 검증 작업 수행
- Repository 계층을 활용하여 DB에 접근 (Service 계층의 단일 메소드가 트랙잭션 단위가 됨)
- 세부 영역(유저, 글, 댓글, 검색 등)별로 클래스 생성하여 구현
- 인터페이스의 사용이 권장, 다형성을 활용한 기능 확장 요구가 없으면 일반 클래스 사용

# Spring Service 예시
- @Controller: UserController, PostController, ReplyController, SearchController
- @Service: UserService, PostService, ReplyService, SearchService 
- @Repository: UserRepository, PostRepository, ReplyRepository, SearchRepository

# 객체 의존성 활용
- 의존성: 하나의 모듈이 다른 모듈을 사용 (클래스, 패키지 등)
- 일반적으로 다른 객체를 사용하려면 멤버 변수에 new 키워드로 객체 생성하여 참조
- 생성한 객체에서 메소드를 호출하여 사용
- 어떤 객체를 생성하여 사용할 것인지 코드 상에 명시 (컴파일 타임 의존성)

# 의존성 주입 DI (Dependency Injection)
- 객체 생성을 외부에서 대신 수행
- 활용할 객체에 대한 의존성 설정을 외부에서 대신 수행
- 활용할 클래스(인터페이스) 타입의 멤버 변수만 선언 후 생성자 구현 (new를 직접하지않음)

# Spring 프레임워크의 객체 생성 및 관리 역할
- 스프링 프레임워크가 특정 조건을 만나면 객체를 생성
- 조건 1. 클래스 상단의 Annotation (@Controller, @RestController, @Service 등등)
- 조건 2. @Configuration 클래스의 @Bean Annotation
- 조건 3. XML 설정 (최근에는 조건 1, 2를 주로 사용)
- Component Scan: 객체로 생성할 대상을 검색하는 과정
- 조건에 따라 객체들의 의존성을 관리한다.

# Spring 프레임워크의 객체 생성 및 관리 역할 예시
- 스프링이 Controller 어노테이션을 스캔
- Controller 생성자에서 필요한 객체 스캔
- 필요한 객체의 클래스에 가서 Service 어노테이션을 스캔하면 스프링이 직접 객체 생성
- 스프링이 생성한 Service 객체로 생성자에 인자로 넣고 Controller 객체 생성

# Spring IoC 컨테이너
- 스프링에서 객체의 생성과 관리의 역할을 하는 컴포넌트

# Spring Bean
- IoC 컨테이너에 의해서 생성되어 관리되는 Java 객체

# 의존성 주입 단계
- 1. Spring에 의해 객체가 생성되도록 Annotation 설정
- 2. 사용할 객체를 멤버 변수와 생성자에 추가
- 3. 객체를 사용

# @Configuration
- Java 클래스에 @Configuration 어노테이션을 사용 가능
- @Configuration을 사용한 클래스는 Spring에 의해 설정 정보를 위한 클래스로 활용

# @Bean Annotation
- @Configuration 클래스 내에 @Bean 메소드로 Bean 생성 가능
- Bean으로 등록할 객체를 생성 후 리턴

# 의존성 주입 정리
[Java 소스코드, Controller 클래스, Service 클래스]와 [Spring Framework의 설정 정보 @Controller, @RestController, Service, Bean]을 스프링 내부의 컴포넌트인 Spring IoC 컨테이너에 입력되면 컨테이너가 이것들을 분석하여 Bean을 생성하고 Bean 간의 의존성을 설정한다.

# 의존성 주입 디버깅
- logging.level.org.springframework.beans = DEBUG
- 위 코드를 appliction.properties에 작성하고 서버를 실행시키면 콘솔에 세세하게 나온다.
- 콘솔에서 bean이 생성되고 컨트롤러나 서비스를 연결하는걸 로그로 볼 수 있다.

# 의존성 주입 실습
- PostDto 클래스 생성, id, title, content, username을 생성자로 받고, getter 메소드를 만듬
- PostService 클래스 생성, @Service 어노테이션 작성, PostDto 객체를 생성하여 리턴
- PostController 클래스 생성, @RestController와 @RequestMapping 어노테이션 작성, PostService 객체를 new를 쓰지않고 작성, 생성자에서 PostService 객체를 인자로 받음, 스프링의 IoC 컨테이너에서 @RestController 어노테이션을 스캔하고 생성자에서 PostService 객체 인자를 보고 PostService 클래스로 찾아가서 객체를 직접 생성, 따라서 객체를 스프링에서 생성하여 인자로 받음, 그 후 스프링에서 Controller 객체 또한 생성
- GET 요청이 들어오면 Controller의 @GetMapping 메소드에서 DTO 객체에 Service 객체에서 리턴한 DTO를 넣고 리턴
- @Service를 사용하지 않는다면, Configurantion 어노테이션 클래스에서 Bean 어노테이션 메소드로 PostService 객체를 생성할 수 있도록 만듬, 이제 PostService의 Service 어노테이션을 지워도 Bean 메소드에서 PostService 객체를 생성하고 반환하고 있으므로 스프링은 PostService 객체를 Bean으로 만들어 관리, 여기서 만든 Bean을 PostController의 생성자의 인자로 넣어서 PostController가 PostService를 사용할 수 있게 됨
- 만약 Bean 어노테이션으로도 생성하고 Service 어노테이션으로도 생성하면 2개가 충돌이 나서 에러가 발생
- 이를 해결하는 가장 간단한 방법은 Bean 어노테이션이 붙은 메소드의 이름을 바꾸면 가능
- 같은 종류의 Bean을 만들어도 이름이 다르면 여러개 생성이 가능

# Data Access Layer
데이터베이스에 접근하여 데이터를 저장하거나 조회하는 레이어이다. 서비스 계층과 데이터베이스 사이의 추상화된 계층이다. 데이터베이스 기술이 변경되면 레이어의 코드는 변경될 수 있지만 서비스 계층의 코드는 변경되지 않는다. 오라클이든 MySQL이든 프레젠테이션 레이어와 애플리케이션 레이어는 영향받지 않는다.

# 데이터 접근 기술
> JDBC

데이터베이스에 접근하기 위한 Java의 표준 API이다. 로우 레벨의 기술이라 단순 기능까지 모두 코드로 작성하여 코드의 양이 많아진다.

> JDBC Template

JDBC를 효율적으로 사용하기 위한 Spring API이다. JDBC보다 훨씬 더 적은 코드의 양으로 데이터베이스에 접근할 수 있다.
> SQL Mapper

SQL과 Java 객체를 매핑하는 기술이다. SQL의 input 또는 output을 Java 객체와 매핑한다. Java의 SQL Mapper는 일반적으로 **Mybatis**가 사용된다. 세계적으로 SQL Mapper의 사용률은 떨어지고 있지만, 국내에서는 많은 기업에서 대규모 프로젝트에서 활용하고 있다.

> ORM

RDBMS의 테이블과 Java 객체를 매핑하는 기술이다. ORM Framework가 객체와 테이블을 매핑하며, SQL을 자동으로 생성한다. Java, Spring에서 ORM 적용을 위해 **Hibernate**와 **Spring Data JPA**가 주로 사용되고 있다. 세계적으로 SQL Mapper보다 사용률이 월등히 높고, 국내에서도 사용률이 점점 높아지고 있다.

# Maven
Java 프로젝트에서 사용되는 빌드 자동화 도구이다 빌드는 소스코드를 실행 가능한 SW 산출물로 만드는 과정인데, 이것을 Maven이 단순화 시켜준다.

> Maven의 주요 기능
- 프로젝트 구성 및 빌드 관리
- 라이브러리 의존성 관리

> Maven 라이브러리 의존성 관리

이전에는 외부 라이브러리를 직접 다운받아 설정했지만, Maven을 사용할 때 외부 라이브러리를 명시하면 자동으로 다운로드해준다. **pom.xml**파일의 **dependencies** 태그 안에 사용할 외부 라이브러리를 선언하면 된다.

> Maven Central Repository

Maven에서 관리하는 중앙 Repository이다. pom.xml에 외부 라이브러리 정보를 명시하면 중앙 Repository에 외부 라이브러리를 요청해서 다운로드 받고, 애플리케이션에서 외부 라이브러리를 활용할 수 있도록 설정한다.

> Maven pom.xml

Maven이 프로젝트를 빌드하기 위해서 필요한 정보를 기술하는 XML 파일이다. 프로젝트의 정보, 필요한 라이브러리 의존성 정보, 빌드 단계에서 사용되는 정보 등을 기술한다.

> pom.xml 태그
1. project: 최상단의 태그
2. modelVersion: pom.xml 구조의 버전
3. groupId: 일반적으로 회사 url의 역순으로 설정하며, 프로젝트 간 식별 가능한 고유 이름
4. artifactId: 실제로 만드는 애플리케이션 산출물의 이름
5. version: 현재 개발중인 애플리케이션의 버전
6. dependencis: 하위에 다수의 dependency로 라이브러리 명시
7. dependency: groupId, artifactId, version 등 외부 라이브러리의 정보 명시

> Maven 의존성 검색  
> https://mvnrepository.com/

# Mybatis
Java의 SQL Mapper
```XML
<!-- Mybatis 의존성 추가 -->
<dependency>
    <groupId>org.mybatis.spring.boot</groupId>
    <artifactId>mybatis-spring-boot-starter</artifactId>
    <version>2.2.2</version>
</dependency>
```

## Mybatis 설정
> mybatis.config-location=classpath:mybatis/mybatis-config.xml
> - application.properties에 설정하면 Spring이 읽고 수행한다.
> - 위 설정은 Mybatis의 설정 파일의 위치를 명시한 것이다.
> - classpath는 경로의 모음을 뜻한다.
> - resources가 classpath의 경로 중 하나이므로 그 밑의 폴더 안에 파일이 있다는 뜻이다.

> mybatis-config.xml  
> - Mybatis가 읽는 파일이다.
> - SQL이 작성된 Mapper 파일의 위치 정보 등 다양한 설정이 가능하다.

> mapper.xml  
> - mapper 파일은 한 애플케이션에서 여러개가 있을 수 있다.
> - 일반적으로 테이블마다 혹은 조인된 데이터마다 mapper를 만든다.

> Mybatis 설정 공식문서  
> https://mybatis.org/mybatis-3/configuration.html

```XML
<!-- mybatis-config.xml 파일 내용 예시 -->
<!-- mapper.xml 안에는 DB에 접근하기 위한 SQL문이 들어간다. -->
<configuration>
    <mappers>
        <mapper resource="mybatis/mapper/todo-mapper.xml" />
    </mappers>
</configuration>
```

```XML
<!-- todo-mapper.xml 파일 내용 예시 -->
<mapper namespace="com.codepresso.todo.mapper.TodoMapper">
    <insert id="save">
        INSERT INTO TODO(CONTENT, ISCOMPLETED)
        VALUES (#{todo.content}, #{todo.isCompleted});
    </insert>
</mapper>
```

```Java
// MyBatis Mapper 예시
@Mapper
public interface TodoMapper {
    void save(@Param("todo")) Todo todo);
}
```

## Mybatis Mapper의 동작
```mermaid
graph LR;
A[Application Layer Service]
B[Mapper 인터페이스]
C[Mapper xml SQL]
D[(Database)]
E[DTO]
A --> B
B --> A
B --> C
C --> B
C --> D
D --> C
E <--> B
E <--> C
```

- Application 레이어의 Service에서 Mapper 인터페이스를 호출한다.
- 호출된 Mapper 인터페이스의 메소드에 해당하는 Mapper.xml의 SQL문이 실행된다.
- Mapper 인터페이스와 Mapper.xml 사이에서 DTO 혹은 단일 value를 주고 받는다.
- 이것들은 모두 Mybatis에 의해 관리된다.

# H2 Database
Java의 관계형 데이터베이스 관리 시스템
```XML
<!-- H2 Database 의존성 추가 -->
<dependency>
    <gropudId>com.h2database</gropudId>
    <artifactId>h2</artifactId>
</dependency>
```
- 경량화된 RDBMS로 메모리에 데이터를 저장 할 수 있다.
- 별도 설치 없이 Maven 의존성만으로 Spring Boot에서 쓸 수 있다.
- 테스트용으로 가볍게 활용이 가능하다.

## H2 Database 설정
> spring.datasource.driver-class-name=org.h2.Driver
> - DB 연결을 위한 h2 드라이버 사용
> - MySQL의 경우 com.mysql.cj.jdbc.Driver
> - Oracle의 경우 oracle.jdbc.driver.OracleDriver

> spring.datasource.url=jdbc:h2:mem:[DB명]
> - DB 접속을 위한 URL
> - MySQL의 경우 jdbc:mysql://localhost:3306/[DB명]
> - PostgreSQL의 경우 jdbc:postgresql://localhost:5432/[DB명]

> spring.datasource.username=[사용자명]
> - DB에 접속하기 위한 사용자 이름

> spring.datasource.password=[패스워드]
> - DB에 접속하기 위한 패스워드

> spring.h2.console.enabled=true
> - h2 웹 콘솔 사용 선언

> spring.h2.console.path=/h2-console
> - 웹 콘솔을 접속할 수 있는 uri 패스 설정 이 경우 /h2-console
> - localhost:8080/h2-console

# Maven & H2 의존성 추가 실습
1. 프로젝트의 pom.xml을 연다.
2. dependencies 태그 하위에 Maven과 H2의 의존성을 추가한다.
3. 저장 후 오른쪽에 m 마크의 아이콘으로 Load Maven Changes가 뜨면 누르고 아래쪽에 진행 바가 없어지기를 기다린다.
4. 왼쪽 프로젝트 구조에서 External Libraries 안에 추가 되었는지 확인한다.

# Spring 애플리케이션 설정
Spring 애플리케이션의 구성에 대한 부가적인 정보로 시작 시점에 읽는다.  
프로젝트 구조에서 src-main-resources 하위에 위치하는 application.properties 파일에 설정 정보를 추가할 수 있으며, application.yaml 파일을 쓰기도 한다.  
설정 정보는 key=value 형태로 작성한다.

> Spring Boot 설정 공식 문서  
> https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html

> 예시) 포트 변경 8080 -> 8081  
> server.port=8081

# Spring의 DB 테이블 및 데이터 초기화
1. DB 테이블 초기화  
Spring 프로젝트 구조에서 resources 디렉터리 하위에 schema.sql 파일 생성 후 SQL을 작성한다.  
ex) CREATE문

2. 데이터 초기화  
Spring 프로젝트 구조에서 resources 디렉터리 하위에 data.sql 파일 생성 후 SQL을 작성한다.  
ex) INSERT문