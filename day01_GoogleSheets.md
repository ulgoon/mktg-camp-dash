# Fastcampus
## 퍼포먼스 마케터를 위한 업무자동화 실전 CAMP
### Day1. Intro to Google Sheets

---
<!--
page_number: true
$size: A4
footer : fastcampus 퍼포먼스 마케터를 위한 업무자동화 실전 CAMP, Wooyoung Choi, 2018
-->

## Introduce
### 최우영

- Developer, Co-founder at Disceptio
- Solution Architect, Web Developer, Instructor
- Publish: Python Web Crawling Bootcamp(gilbut,2019)
- Skills: Python, Golang, Julia, Node.js, Google tag manager ...

#### blog: https://blog.ulgoon.com/
#### github: https://github.com/ulgoon/
#### email: me@ulgoon.com

---
## Curriculum
- Week 1: Google sheets 기초
- Week 2: 마케터를 위한 대시보드 만들기
- Week 3: Google Apps Script를 위한 javaScript
- Week 4: Google Apps Script를 이용한 업무자동화

---
## Goal
- 구글 시트의 쓰임새와 MS의 엑셀과 다른 특징을 이해한다.
- 구글 시트의 여러 함수들을 알고, 필요한 함수를 적절히 활용할 수 있다.
- 구글 시트를 활용하여 웹의 데이터를 내 시트에 표현할 수 있다.
- query 함수를 이용하여 원하는 데이터를 필터링 해 가져올 수 있다.

---
## Google Sheets
![](https://www.tmmdata.com/img/integrations/Google%20Sheets%20Logo-1.png)

---
### Google Sheets
- Google의 스프레드시트 문서 편집을 위한 문서편집툴

---
### Pros & Cons
#### Pros

- 협업! 협업!!
- 구글 서비스와 유기적 통합
- javaScript 기반 -> Google Apps Script
- 인터넷만 있다면(심지어 없어도) 어디서나 편집
- .xlsx도 편집가능
- 수정내역이 남음(편집자도!)
- ...

---
### Pros & Cons
#### Cons

- 속도..
- 데이터의 제한(2M cells)

---
## We can do these with google sheets ..

- 엑셀로 하는 모든 작업
- Web Scraping
- CRUD such as Database
- Automate Process with G Apps
- Co-work
- Publish to web
- ..

---
## Difference with MS Excel

- javaScript <> VBA
- web based <> local
- G Apps <> MS Office

---
## Google sheets basic


---
### Create new document

---
### Layout

---
### Add on

---
### Functions

---
- sum
- average
- round

---
- if
- ifs
- iferror

---
- today
- now
- date
- days

---
- concatenate
- split
- left
- mid
- right


---
### SCRAP with Google sheets

---
## Caution!!
저작권 침해 위반 소지
- 웹사이트 운영자의 크롤링 금지 룰을 어길경우 
- 월권하여 데이터베이스에 접근
- 타인의 경제적 이익을 침해할 경우
- 개인정보를 수집할 경우(전화번호, 주소, ..)

---
## IMPORTFEED
> RSS 또는 Atom 피드를 가져옵니다.

`IMPORTFEED(URL, [쿼리], [헤더], [항목_개수])`

- URL - RSS 또는 Atom 피드의 URL로 프로토콜(예: http://)을 포함

- "feed"는 제목, 설명 및 URL 등의 피드 정보를 포함하는 하나의 행을 반환

	- "feed "은 피드의 특정 속성을 반환 은 제목, 설명, 작성자 또는 URL 중 하나

- "items"는 피드의 항목을 포함하는 표 전체를 반환 
	- 항목_개수를 지정하지 않을 경우 현재 피드에 게재된 모든 항목이 반환

	- "items "은 요청한 항목의 특정 속성을 반환

---
## IMPORTFEED
> RSS 또는 Atom 피드를 가져옵니다.

`IMPORTFEED(URL, [쿼리], [헤더], [항목_개수])`


- 헤더: [ 선택사항 - 기본값은 FALSE] - 반환된 값의 상단에 행을 추가해 열 헤더를 포함할지 여부

- 항목_개수: [ 선택사항 ] - 항목의 검색어에 대해 가장 최근 순서로 반환할 항목의 개수

- 항목_개수를 지정하지 않을 경우 현재 피드에 게재된 모든 항목이 반환

---
### Get Articles
https://www.theguardian.com/technology/mobilephones/

---
### Get Podcast Feed
http://getrssfeed.com/
https://soundcloud.com/xsfm

---
## IMPORTDATA
> 웹에 게재된 csv, tsv 등의 파일 데이터를 가져옵니다.

`IMPORTDATA(url)`
- url: 웹에 게재된 데이터 파일의 고유주소

---
## Let's get theatre data
https://ulgoon.github.io/file/theatre_20180403.csv

---
## IMPORTHTML
> HTML 페이지에서 표 또는 목록에 있는 데이터를 가져옵니다.

`IMPORTHTML(url, query, index)`

- url: 검토할 페이지의 URL이며 프로토콜(예: http://)을 포함
- query: 원하는 데이터가 어떤 구조에 포함되었는지에 따라 '목록' 또는 '표'
	- ul, ol, dl, table, ..
- index: 여러개의 요소가 존재할 때 선택할 요소의 순서

---
### Let's get 2018 Russia WorldCup Table Data
https://en.wikipedia.org/wiki/FIFA_World_Cup

---
### Rotten Tomatoes TOP BOX OFFICE
https://www.rottentomatoes.com/

---
## IMPORTXML
> XML, HTML, CSV, TSV, RSS 및 Atom XML 피드를 포함한 다양한 구조화된 데이터로부터 데이터를 가져옵니다.

`IMPORTXML(url, xpath_검색어)`

- url: 검토할 페이지의 URL이며 프로토콜(예: http://)을 포함

	- url 값은 따옴표로 묶거나, 적절한 텍스트를 포함하는 셀에 대한 참조

- xpath_검색어: 구조화된 데이터에서 실행되는 XPath 검색어
	- https://www.w3schools.com/xml/xpath_intro.asp

---
### Popular news in media Daum
http://media.daum.net/

---
## IMPORTRANGE
> 지정된 스프레드시트에서 셀 범위를 가져옵니다.

`IMPORTRANGE(spreadsheet_key, range_string)`

spreadsheet_key: 가져올 데이터가 있는 스프레드시트의 URL
range_string - "`sheet_name`!`range`" 형식의 문자열이며 가져올 범위를 지정

---
## Let's make Currency Report

---
### Let's make Currency Report
http://finance.daum.net/exchange/exchangeMain.daum?nil_profile=stockgnb&nil_menu=exchange_top

https://finance.yahoo.com/quote/KRW=X?p=KRW=X


<link href="https://fonts.googleapis.com/css?family=Nanum+Gothic:400,800" rel="stylesheet">
<link rel='stylesheet' href='//cdn.jsdelivr.net/npm/hack-font@3.3.0/build/web/hack-subset.css'>

<style>
h1,h2,h3,h4,h5,h6,
p,li, dd {
font-family: 'Nanum Gothic', Gothic;
}
span, pre {
font-family: Hack, monospace;
}
</style>