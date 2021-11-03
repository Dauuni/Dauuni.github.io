---
layout: post
title: "은행별 예금, 적금 상품 비교 사이트 KM Bank"
info: "웹 사이트 제작"
tech: "Spring Boot, MyBATIS, Oracle, Bootstrap, HTML5, CSS, JSP, JavaScript, jQuery, AJAX, JSON"
type: Team
---

# 은행별 예금, 적금 상품 비교 사이트 KM Bank

예금, 적금 상품을 들기 위해 사람들은 은행에 직접 방문하거나 온라인 사이트에 접속하게 된다. 이럴 경우 해당 은행의 정보만 제공하고 있기 때문에 다른 은행 상품과 비교했을 때 어느 쪽이 효율적인지 판단하는데 어려움이 발생한다.

KM Bank 사이트는 이 점을 고려하여 사용자가 궁금한 두 은행의 상품을 선택하면 상품의 은행명, 상품이름, 가입 방법, 이자율을 한눈에 보여준다. 해당 은행의 상품을 자세히 보고 싶은 경우 사용자의 편리를 위해 은행 이름 클릭 시 온라인 사이트로 넘어가도록 설계하였다.<br><br>

## Github
---
<https://github.com/Dauuni/team1_v2sbm3c_git.git>
<br><br>

## Member
---

**문다은** : 팀장, 웹 퍼블리셔, 데이터 아키텍트(예금, 커뮤니티, 은행사이트)<br>
강민우 : 웹 퍼블리셔, 데이터 아키텍트(적금, 회원)<br><br>

## Develop Period
---

<br>
![](/assets/img/36.jpg)
<br>

## ERD(Entity-Relationship Diagram)
---

- **Logical**
![](/assets/img/37.jpg)

- **Physical**
![](/assets/img/38.jpg)

## Techique
---

- **Spring Boot**

	![](/assets/img/33.jpg){: width="80" height="60"} 스프링 개발과 관련된 기능들을 개발자가 사용하기 편리하도록 지원하는 **STS(Spring Tool Suite)** 4.6 버전을 사용하여 개발하였다.

- **MyBATIS**

	-- SQL을 JAVA와 분리함으로 **독립적인 팀 개발**이 가능하여 개발 시간을 단축시켰고, SQL과 JAVA의 연결을 **XML을 이용**하여 선언하였다.
    ![](/assets/img/34.JPG)

- **Oracle**

	-- **Oracle 11G**를 사용하여 데이터를 관리하였다.

	-- **SQL Developer** 19.2.1버전을 사용하여 Oracle 11G에서 생성한 계정으로 접속하여 테이블과 데이터를 관리하였다.
    ![](/assets/img/35.JPG)

- **UI Style**

	-- **Bootstrap**<br>
    HTML, CSS, JS 프레임워크인 Bootstrap을 사용하여 웹사이트를 디자인을 구성하였다.
    <br><br>
    Bootstrap은 하나의 CSS로 Mobile(휴대폰), 태블릿, 데스크탑 등 많은 기기에서 작동하고, 여러 기능을 제공하여 사용자가 쉽게 웹 사이트를 제작 및 유지 보수 할 수 있도록 도와준다.

	-- **HTML5**<br>
    Layout 구성 및 데이터 출력의 목적으로 사용하였다.

    -- **CSS**<br>
    출력되는 HTML에 시각적인 효과를 적용하기 위해 사용하였다.

- **JSP**

	-- **서버** 프로그램 구현을 위해 HTML 코드 내에 직접 자바 코드를 삽입하는 JSP를 사용하였다.

	-- JSTL에서 제공하는 태그들을 사용하여 선언하였다.

    -- JAVA 코드를 처리하여 출력 결과를 HTML과 CSS로 변환하여 출력한다.

    -- WEB에서 JAVA를 이용한 DBMS 접근을 처리한다.

- **JavaScript**

	-- JSP에서 호출할 함수를 선언하고 WEB 요소의 id를 사용하여 해당 요소의 동작을 지정한다.

- **jQuery**

	-- JavaScript 라이브러리로 **동적 이벤트 처리**를 담당한다.
    <br>
    ex) 체크박스 갯수 제한, 버튼 클릭, 마우스 on/over 등

- **AJAX**

	-- **페이지 이동없이** 화면을 전환하기 위해 사용하였다.

	-- Controller에서 JSON 형태의 변수를 전달하여 JSP에서 선언하고, **동작들을 처리**한다.

- **JSON**

	-- Controller에서 VO에서 선언한 각각의 필드를 AJAX가 사용하기 위해 데이터를 전달하는 개방형 표준 포맷이다.<br><br>


## Development Sequence
---
1. 구현 기능 분석
2. DB 모델링
3. SQL 생성 및 테스트
4. VO(DTO) 생성
	- SQL을 MyBATIS XML로 변환
	- SQL XML Mapping File 생성
5. DAO Interface 생성
6. DAO Interface 구현
7. Process Interface 생성(Business Logic, Manager/Service class)
8. Process Interface 구현
9. Spring Controller MVC Action class 생성
10. Controller, Beans(Tool(Utility 날짜 처리등 각종 메소드), Paging, Download)
11. JSP 제작, Controller, Beans와 연동
12. Test
<br><br>

## Web site
---

- **main**
![](/assets/img/39.jpg)
> 웹 사이트에 접속하자마자 뜨는 메인 화면이다.<br>
현재 관리자 권한으로 로그인한 상태여서 오른쪽 상단에 관리자 버튼이 활성화 되어 있는 상태이다. 아래 메인 컨텐츠 부분은 메인 화면에서 많이 사용 되는 이미지 슬라이드를 추가하였다.

- **예금**
![](/assets/img/40.jpg)
> 배너에 있는 예금 버튼을 눌렀을 때의 화면이다.<br>
상단에 가입 방법, 지역, 검색어에 따라 분류할 수 있는 검색 기능을 추가하였다.

- **적금**