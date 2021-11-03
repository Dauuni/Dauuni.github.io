---
layout: post
title: "은행별 예금, 적금 상품 비교 사이트 KM Bank"
info: "웹 사이트 제작"
tech: "Spring Boot, MyBATIS, Oracle, Bootstrap, JavaScript, jQuery, Ajax, JSON, HTML5, CSS, JSP"
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

	-- **SQL Developer** 19.2.1버전을 사용하여 Oracle 11G에서 생성한 계정으로 접속하여테이블과 데이터를 관리하였다.
    ![](/assets/img/35.JPG)

- **phpMyAdmin**

	-- MySQL **데이터 데이스를 관리**하는 용도로 사용하였다.

	-- bazzi라는 데이터베이스를 생성하여 전체 데이터를 관리하였다.

 > ⓐ 회원가입한 이용자의 아이디, 비밀번호(암호화)의 값을 Login 테이블 userID, userPassword열에 저장
 > 
 > ⓑ 아기의 체온, 맥박 값을 mysql 테이블 temp2, bpm2열에 저장
 > 
 > ⓒ 그래프 작성을 위해 사용자가 입력한 아기의 키, 몸무게 값과 날짜를 babyGraph테이블 babyCM, babyKG, babyDate열에 저장

- **PHP**

	-- APP과 phpMyAdmin을 연결하는데 사용하였다.

	-- APP에서 입력한 데이터를 MySQL에 저장할 때 사용하였다.

	-- 데이터베이스에 있는 값을 APP에 나타내기 위해서 **JSON 형태**로 웹 상에 나타나게 하였고, 그 값을 읽을 때 사용하였다.<br><br>