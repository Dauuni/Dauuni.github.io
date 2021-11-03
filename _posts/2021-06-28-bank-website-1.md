---
layout: post
title: "은행별 예금, 적금 상품 비교 사이트 KM Bank"
info: "웹 사이트 제작"
tech: "Spring Boot, MyBATIS, Oracle, Bootstrap, HTML5, CSS, JSP, JavaScript, jQuery, Ajax, JSON"
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

	-- 서버 프로그램 구현을 위해 HTML 코드 내에 직접 자바 코드를 삽입하는 JSP를 사용하였다.

	-- 많이 사용되는 개발자 정의 태그를 모은 JSTL을 이용하여 JSP 개발하였다.<br><br>

    	라이브러리    기능                                        접두어(prefix)
    	----------------------------------------------------------------------
       	Core          변수지원, 흐름 제어, URL 처리           c
       	관련 URL: http://java.sun.com/jsp/jstl/core ★

       	XML           XML 코어, 흐름 제어, XML 변환         x
       	관련 URL: http://java.sun.com/jsp/jstl/xml

       	국제화        지역, 메시지 형식, 숫자 및 날짜 형식  fmt
       	관련 URL: http://java.sun.com/jsp/jstl/fmt

       	데이터베이스  SQL                                          sql
       	관련 URL: http://java.sun.com/jsp/jstl/sql

       	함수          콜렉션 처리, String 처리                   fn
       	관련 URL: http://java.sun.com/jsp/jstl/functions
     	----------------------------------------------------------------------