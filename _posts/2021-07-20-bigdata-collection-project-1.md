---
layout: post
title: "News 데이터 분석 시스템"
info: "빅데이터 수집 시스템 개발"
tech: "Python, Crawling, BeautifulSoup, KoNLPy, WorldCloud, MariaDB, Django, Pycharm, HTML, CSS, jQuery,　　　　Ajax, Bootstrap"
type: Personal
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

# News 데이터 분석 시스템

직접 해당 사이트에 접속하여 기사를 읽어 트렌드를 분석해야 하는 불편함을 해소하기 위한 사이트를 구현하였다. 데이터 분석 시 주관적인 견해가 포함되는 문제점을 해결할 수 있고, 워드 클라우드 기법을 사용하여 통계 자료의 시각적 효과를 높였다.

통계 자료의 경우 Crawling, 자연어 처리, 빈도 분석을 통해 제공된다.<br><br>


## Github
---
<https://github.com/Dauuni/CrawlingB.git>
<br><br>

## Goals
---

1. Daum News 랭킹에서 순서대로 제목을 수집
2. 수집된 자료의 태그를 분석하여 정보 추출
3. 추출한 정보를 MariaDB에 저장
4. 저장된 정보를 이용하여 빈도 분석 진행
5. 워드 클라우드 기법을 이용하여 시각화
6. 사용자가 웹상에서 컨트롤 가능하도록 구현
<br><br>

## Main courses and procedures
---

<br>
![](/assets/img/49.JPG)
<br>

## Techique
---
<br>

| Means | Explanation |
|:--------:|--------|
|개발 방법론|애자일 방법론을 적용하여 개인에게 책임 부여하고 주도적인 개발 환경 구성|
|기본 언어|Python|
|DBMS|MariaDB|
|Front end|HTML, CSS, jQuery, Ajax, Javascript, Bootstrap|
|Back end|Python, Django|
|데이터 수집|BeautifulSoup|
|형태소 분석기|Konlpy, Okit package|
|빈도 분석|Counter class|
|시각화|WorldCloud package|
|Web Framework|Django 3|
|편집기|Anaconda, Jupyter, Notebook, Pycharm 2020.1|

<br>

## Development Sequence
---

1. **jQuery, Ajax, JSON, Django, Beautifulsoup, MariaDB 연동 크롤링, 분석 시스템 개발용 <br>Pycharm 프로젝트 설정**
<br>

	![](/assets/img/50.jpg)
<br>

2. **templates 페이지, HTML · CSS · Ajax 요청 페이지 제작**
<br>

	![](/assets/img/51.jpg)
<br>

3. **models.py를 통한 Table 구조 정의**
<br>

	![](/assets/img/52.jpg)
<br>

4. **관련 Python package install**
<br>

	```{.bash}
	(base) C:\Windows\system32>activate ai
	(ai) C:\Windows\system32>pip install beautifulsoup4
	(ai) C:\Windows\system32>pip install wordcloud
	(ai) C:\Windows\system32>pip install konlpy
	(ai) C:\Windows\system32>pip install nltk
	(ai) C:\Windows\system32>cd
	(ai) C:\>cd ai8/setup
	(ai) C:/ai8/setup> activate ai
	(ai) C:/ai8/setup> pip install JPype1-1.1.2-cp37-cp37m-win_amd64.whl
	```
<br>

5. **수집 시작 및 중지 기능 제작**
<br>

	![](/assets/img/53.jpg)<br>
	![](/assets/img/54.jpg)
<br>

6. **목록 출력 기능 구현**
<br>

	![](/assets/img/55.jpg)
<br>

7. **한 건의 자료를 삭제하는 기능 구현**
<br>

	![](/assets/img/56.jpg)
<br>

8. **모든 자료를 삭제하는 기능 구현**
<br>

	![](/assets/img/57.jpg)
<br>

9. **자연어 처리를 기반으로 한 빈도 분석과 워드 클라우드 제작 및 저장**
<br>

	![](/assets/img/58.jpg)<br>
	![](/assets/img/59.jpg)