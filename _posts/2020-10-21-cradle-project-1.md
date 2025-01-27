---
layout: post
title:  "아기의 안전을 위한 스마트 요람 Bazzi"
info: "졸업작품"
tech: "RaspberryPI, Arduino, Android Studio, phpMyAdmin, PHP"
type: Team
---

<style>
  table {
      border-collapse: collapse;
      border-top: 1px solid #ccc;
      border-left: 1px solid #ccc;
      border-right: 1px solid #ccc;
      border-bottom: 1px solid #ccc;
  }
  table thead th {
  		border-left: 2px solid #ccc;
  		border-right: 2px solid #ccc;
  		border-bottom: 2px solid #ccc;
      background-color: #F2F2F2;
      text-align: center;
      line-height: 1.5;
      padding: 10px;
      font-weight: bold;
      vertical-align: middle;
      color: #1b3453;
  }
  table td {
      padding: 10px 15px;
      vertical-align: middle;
      border-left: 1px solid #ccc;
      border-right: 1px solid #ccc;
      border-bottom: 1px solid #ccc;
}
</style>

# 아기의 안전을 위한 스마트요람 Bazzi

아기가 태어난 후 부모는 필수적으로 아기의 침대 또는 요람을 구입하게 된다. 24시간 아기의 상태를 신경 써야 하는 부모는 아기를 중심으로 행동반경이 넓지 않게 된다.

이때, 스마트 요람 'Bazzi'는 부모의 눈과 손을 대신해 주는 역할을 한다. Bazzi를 통해 실시간 모니터링과 체온&맥박 상태 등 아기의 상태를 APP을 통해 확인할 수 있기 때문이다.<br><br>

## Github
---
<https://github.com/Dauuni/Bazzi.git>
<br><br>

## Member
---

**문다은** : 안드로이드 APP 제작<br>
권영인 : 리즈베리파이 및 아두이노<br>
나새영 : 라즈베리파이 및 아두이노<br>
김혜선 : 안드로이드 APP 제작<br><br>

## Develop Period
---

![](/assets/img/26.JPG){: width="600" height="400"}
<br>


## Techique
---

- **Raspberry PI 4**

	-- 아기의 모습을 **실시간으로 모니터링**하기 위해 카메라 모듈을 사용하여 웹으로 화면을 하였다.

	-- 디스플레이 모듈에서 동요나 영상이 나오면서 아기의 관심을 끌고, 위쪽에 달린 온도 센서가 체온을 잘 측정할 수 있도록 도와준다.

- **Arduino**

	-- **맥박 센서**를 부착하여 **아기의 심장 BPM을 측정**하여 데이터베이스에 값을 저장한다.

	-- 디스플레이 위에 **온도 센서**를 부착하여 **아기의 체온을 측정**하여 데이터베이스에 값을 저장한다.

- **Android**

	-- Android Studio로 개발한 APP에서 요람에서 제공하는 아기의 상태를 확인할 수 있다.

	-- **회원가입&로그인 기능**을 통해 데이터를 저장하며 사용할 수 있다.

	-- 한 화면에서 카메라 모듈이 웹에 전송한 **실시간 화면**과 **아기의 맥박과 체온 값**을 볼 수 있다.

	--  날짜별로 아기의 키와 몸무게를 입력하면 성장 속도를 한눈에 볼 수 있는 **성장 그래프**를 생성한다.

	-- **일기장** 기능을 통해 아기와 함께한 하루를 기록할 수 있다.

	-- 날마다 다른 수유량을 날짜, 시간과 함께 저장하여 리스트 형식으로 볼 수 있다.

- **phpMyAdmin**

	-- MySQL **데이터 데이스를 관리**하는 용도로 사용하였다.

	-- bazzi라는 데이터베이스를 생성하여 전체 데이터를 관리하였다.

 > ⓐ 회원가입한 이용자의 아이디, 비밀번호(암호화)의 값을 Login 테이블 userID, userPassword 열에 저장
 > 
 > ⓑ 아기의 체온, 맥박 값을 mysql 테이블 temp2, bpm2 열에 저장
 > 
 > ⓒ 그래프 작성을 위해 사용자가 입력한 아기의 키, 몸무게 값과 날짜를 babyGraph 테이블 babyCM, babyKG, babyDate 열에 저장

- **PHP**

	-- APP과 phpMyAdmin을 연결하는 데 사용하였다.

	-- APP에서 입력한 데이터를 MySQL에 저장할 때 사용하였다.

	-- 데이터베이스에 있는 값을 APP에 나타내기 위해서 **JSON 형태**로 웹상에 나타나게 하였고, 그 값을 읽을 때 사용하였다.<br><br>

## Concept Design
---

<br>

![](/assets/img/2.jpg)
<center>[Bazzi 단면도]</center>
<br>

![](/assets/img/3.jpg)
<center>[라즈베리파이 및 아두이노 기능 블록도]</center>
<br>

![](/assets/img/4.jpg)
<center>[라즈베리파이 및 아두이노 기능 블록도]<br>(함수화)</center>
<br>

![](/assets/img/5.jpg)
<center>[APP 기능 블록도]</center>
<br><br>

## SRS(Software Requirements Specification)
---

<br>

| ID | 요구사항 | 내용 | 우선순위 | 달성률(%) |
|:----:|----|----|:----:|:----:|
| B_01 | 실시간<br>모니터링 | - 라즈베리파이에 부착된 카메라를 통해 아기의 모습을 실시간으로 모니터링할 수 있다.<br>  - 라즈베리파이에 전원을 가하면 mjpg-stream이 자동으로 실행되고, 모니터링 화면은 APP을 통해 확인할 수 있다. | 2 | 100 |
| B_02 | 디스플레이를 통한 영상 시청 | - APP에서 아기가 좋아하는 동영상을 실행시켜 아기의 관심을 유도할 수 있다.<br> - 5inch 디스플레이를 라즈베리파이의 GPIO 핀에 직접 연결한 뒤 config 파일을 수정하여 실행시킨다.<br> - 라즈베리파이에 동영상 파일을 저장하여 OMX player를 통해 영상을 실행시킨다. | 3 | 90 |
| B_03 | 체온, 맥박<br>상태 확인 | - APP에서 아기의 체온과 맥박 측정값을 실시간으로 확인할 수 있어서 부모는 위급 상황에 빠르게 대처할 수 있다.<br> - 디스플레이 실행 시 아기의 시선을 고정하여, 아기의 머리를 향하고 있는 비접촉식 온도 센서의 측정을 용이하기 한다. | 1 | 100|
| B_04 | 성장 그래프 | - APP에서 날짜별로 아기의 키와 몸무게를 입력하여 성장 그래프를 생성한다.<br> - 아기의 성장 속도를 한눈에 볼 수 있다. | 5 | 100 |
| B_05 | 육아 일기 | - APP에서 육아 일기를 작성할 수 있고, 이후에 날짜별로 기록된 일기를 열어볼 수 있다. | 6 | 100 |
| B_06 | 아기 정보<br>입력 | - APP에서 아기의 사진, 이름, 성별, 나이 정보를 입력하여 아기 정보를 등록할 수 있다.<br> - 입력된 정보는 DB에 저장된다. | 4 | 100 |
| B_07 | 수유 시간 및 수유량 기록 | - 수유 시간을 기록할 수 있다.<br> - 아기가 먹은 양을 기록할 수 있다. | 7 | 90 |

<br>
<br>

## Development(APP)
---

<br>

**▶ APP 아이콘**

![](/assets/img/8.jpg)<br>

**▶ App 메인화면, Navigation Drawer**

| 메인화면 | Navigation | 아기 정보 수정 및 등록 화면 |
|:-------:|:--------:|:--------:|
| ![](/assets/img/9.jpg) | ![](/assets/img/10.jpg) | ![](/assets/img/11.jpg) |

<br>

**▶ App과 데이터베이스 연동**

![](/assets/img/12.jpg)<br>

**▶ App 기능 화면**

| 아기 상태 화면 | 알림 화면 | 디스플레이 화면 | 수유 화면 |
|:--------:|:--------:|:--------:|:--------:|
| ![](/assets/img/13.jpg) | ![](/assets/img/14.jpg) | ![](/assets/img/15.jpg) |  ![](/assets/img/16.jpg)  |

<br>

| 일기장 리스트 화면 | 작성 화면 | 성장 그래프 화면 |
|:-------:|:-------:|:-------:|
| ![](/assets/img/17.jpg) | ![](/assets/img/18.jpg) | ![](/assets/img/19.jpg) |

<br>

**▶ App 사용 방법 화면**

|![](/assets/img/20.jpg)|![](/assets/img/21.jpg)|![](/assets/img/22.jpg)|
|:----:|:----:|:----:|
|![](/assets/img/23.jpg)|![](/assets/img/24.jpg)|![](/assets/img/25.jpg)|


<br><br>

## Appearance of the work
---

<br>

| img | contents |
|:----:|----|
|![](/assets/img/27.jpg){: width="350px" height="280px"}|- 요람 외부 모습<br> - 요람의 옆에 같은 색의 천을 덧대어 디스플레이를 장착할 거치대를 고정|
|![](/assets/img/28.jpg){: width="350px" height="280px"}|- 위쪽에서 본 전체적인 요람 내부 모습|
|![](/assets/img/29.jpg){: width="350px" height="280px"}|- 라즈베리파이에 부착된 유선 스피커를 통해 영상의 소리가 출력|
|![](/assets/img/30.jpg){: width="350px" height="280px"}|- 디스플레이 위쪽에 부착된 카메라를 통해 아기의 모습을 실시간으로 모니터링 가능<br>- 디스플레이로 영상을 송출하여 아기의 관심을 끌어주면서 아기의 이마가 온도 센서를 향해 있게 되면서 체온 측정에 도움을 줌|
|![](/assets/img/31.jpg){: width="350px" height="280px"}|- 요람 안쪽에 흰색 천을 덧대어 시리얼 통신 선과 온도 센서의 선을 가려줌과 동시에 소리 감지 센서의 필요 부분만 빼줌|
|![](/assets/img/32.jpg){: width="350px" height="280px"}|- 아기가 소리를 내면 센서에서 인식<br>- 아기의 발목 부분에 맥박 센서를 부착하여 맥박 측정|