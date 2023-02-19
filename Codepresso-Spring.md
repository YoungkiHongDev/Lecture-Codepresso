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

# 계층형 아키텍처
- SW 아키텍처는 실제 개발 전 최종 SW의 모습을 설계
- SW 아키텍처는 SW의 구조를 정의한 것, SW를 구성하는 주요 요소들과 요소들의 관계를 정의한 것
- 이미 많은 사람이 고민했던 특정 상황의 문제 해결을 위해 일반화된 솔루션이 있음 (메신저 서비스 개발 패턴, 웹서비스 개발 패턴, 분석 시스템 개발 패턴)
- 웹 서비스 개발에 주로 쓰이는 패턴은 SW를 3~4개 계층으로 구분 (Presentation Layer, Application Layer, Business Layer, Data Access Layer)
- 계층 간에 호출하고 데이터를 주고 받으며 전체 웹 서비스 구성
- Presentation Layer(@Controller): 클라이언트로부터 요청을 받아 Application Layer에 처리를 위임, Application Layer의 결과를 최종 클라이언트로 전달
- Application Layer(@Service): 특정 목적을 위한 다양한 비즈니스 로직을 처리
- Data Access Layer(@Repository): DB에 접근하여 데이터를 저장하거나 조회하는 역할

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

# @RequestMapping
- RequestMapping은 클라이언트의 특정 요청이 오면 Spring Framework에 의해 호출된다.
- RequestMapping이 붙은 메소드가 여러개라면?
- Spring Framework가 URI에 맞는 메소드를 호출한다.

# @RestController
- REST API, HTTP API를 위한 클래스를 명시한다.
- @RestController를 붙인 클래스 내부에서 @RequestMapping을 붙인 개별 메소드들이 API가 된다.
- @RestController를 붙인 클래스에 @RequestMapping을 붙여서 공통적으로 쓸 주소를 쓸 수 있다.
- ex) 클래스에 /user를 매핑, 내부 메소드에 2개에 각각 /paid와 /enterprise 매핑 시 /user/paid와 /user/enterprise가 된다.

# @RequestParam (Query String)
- Request 파라미터를 활용하는 Annotation이다.
- name: Query String의 key와 매핑, key와 변수명이 같으면 생략 가능
- required: 필수 여부 (true, false)
- defaultValue: 데이터가 없을경우 설정할 기본 값

# @RequestParam (Path Parameter)
- @RequestMapping value 값으로 넣은 URI에 {}중괄호로 Path Parameter가 들어갈 곳을 표시한다.
- 메소드 파라미터에 @PathVariable 어노테이션을 사용한다.
- 필수 데이터가 아닌 선택적 데이터의 경우 주로 Query String을 사용한다.

# RestController의 객체 응답
- 객체를 반환하면 JSON 형식으로 변환하여 데이터가 응답된다.
- 객체를 JSON 형식으로 변환하는 역할은 Spring이 해준다.