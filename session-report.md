# Session report

**Тестер:** [Т.Мөнхцэцэн]

**Огноо:** [2026-10-25, 15:40 – 16:40]

**Mission:** Уншлагын жагсаалт аппын чанарыг шинжлэх

**Charter:** Ном нэмэх, хайх, устгах, хүснэгт ба тоолуурын нийцэл, API-ийн буруу оролтын боловсруулалтыг шалгах.

## Тэмдэглэл (он цагийн дарааллаар)

### 15:40–15:43 - Ehnii tuluv shalgah

- App: http://localhost:3000
- Ehnii husnegtiin muriin too : [3] table header oroogui
- Niit nomiin too: [4]
- Husnegtiin baganuud: [4]
- Ustgah tovchnii ungu: [Nogoon]
- Hamgiin shine on 2008
- Screenshot: screenshots/initial_state.png
- Ajiglalt: Husnegted 3 nom baigaa bolovch niit nomiin tooluur 4 gej garsan. Iimees ehnii tuluv deer tooluur bolon husnegtiin bodit ugugdliin too zuruutei baina.

### 15:43-15:48 T01: Ner zohiogch, 1999 gesen onii utgiig hiigeed nemeh tovch darsan

- Expected: [Nom amjilttai nemegdej, husnegted shine mur uusch niit nomiin tooluud 1 eer nemegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdsen, niit nomiin too 1 eer nemegdej 5 bolson, husnegtiin muriin too 1 eer nemegdej 4 bolson]
- Result: Pass - nom nemeh uildel amijilttai bolson
- Issues: [Саад гараагүй]

### 15:48-15:56 T02: Nomiin ner hooson uyd shalgah

- Expected: [Nom nemegdehgui aldaanii medeelel gargana]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdsen gedhee garchig heseg hooson, niit nomiin too 1 eer nemegdej 6 bolson, niit muriin too 1 eer nemegdej 5 bolson]
- Result: Fail hooson garchigtai nomiig app zuvshuurch nemsen
- Issues: [Саад гараагүй]
- bug ID: bug-01

### 15:56-15:59 T03: Zohiogchiin ner hooson

- Expected: [Nom nemegdehgui aldaanii medeelel gargana]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdsen gedhee garchig heseg hooson, niit nomiin too 1 eer nemegdej 7 bolson, husnegtiin mur 6 bolson]
- Result: Fail hooson Zohiogchiin nertei nomiig app zuvshuurch nemsen
- Issues: [Саад гараагүй]
- bug ID: bug-02

### 15:59-16:05 T04: Huchintei bus on - 999

- Expected: [Nom nemegdehgui buruu oniig medegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdej 7 bolson, niit nomiin too 1 eer nemegdej 8 bolson]
- Result: Fail zuvshuurugduugui onii nomiig app zuvshuurch nemsen
- Issues: [Саад гараагүй]
- bug ID: bug-03

### 16:05-16:10 T05: Huchintei bus on - 2101

- Expected: [Nom nemegdehgui buruu oniig medegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine nur nemegdej 8 bolson, niit nomiin too 1 eer nemegdej 9 bolson, hamgiin shine on 2101 bolson]
- Result: Fail zuvshuurugduugui onii nomiig app zuvshuurch nemsen
- Issues: [Саад гараагүй]
- bug ID: bug-04

### 16:10-16:15 T06: Davhardsan nom nemeh oroldlogo hiisen

- Expected: [Ijil ner, zohiogchtoi nom davhar nemegdehgui]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdej 9 bolson, niit nomiin too 1 eer nemegdej 10 bolson]
- Result: fail Davhardsan Ner, zohiogchtoi nomiig app zuvshuurch nemsen
- Issues: [Саад гараагүй]
- bug ID: bug-05

### 16:15-16:20 T07: Nom haih uildel

- Expected: [Haisan nom husnegted haragdana, hailtad tohiroogui busad nom haragdahgui, niit nomiin tooluur uurchlugduhgui]
- Actual: [hailtiin hesegt nomiin buten neriig oruulaad haih tovchiig darahad husnegted tuhain nertei nomuud haradgsan mun busad nom haragdaagui, niit nomiin tooluur uurchlugduugui]
- Result: Pass app hailtad tohirson nomiig husnegted haruulsan
- Issues: [Саад гараагүй]
- bug ID: baihgui

### 16:20-16:26 T08: API test - Nom nemeh

- Endpoint : POST http://localhost:3000/api/books
- Request body:
  {
  "author": "Munkhtstesen",
  "title": "test nom 6",
  "year": "2000"
  }
- Expected: [Huchintei ugugdultei huselt ilgeehed nom amjilttai nemegdej amjiltiin hariu butsna]
- Actual: \
  {
  "result": "OK",
  "id": 10
  }
- Result: Pass api huselt amijilttai bolovsruulagdaj id: 10 buhii burtgel uussen
- Issues: [Саад гараагүй]
- bug ID: baihgui

### 16:26-16:33 T09: Nom ustgah test

- Ustgahaas umnuh niit nom: 11
- Ustgahaas umnuh husnegtiin muriin too: 10
- Expected: [Songoson nom husnegtees ustgaj, husnegtiin muriin too bolon niit nomiin too tus bur 1 eer buurna]
- Actual: [Ustgah tovchiig darsnii daraa songoson nom husnegtees arilsan, husnegtiin muriin too 10->9 bolj niit nomiin too 11-> 10 bolson]
- Result: PASS - nom ustgah uildel amjilltai ajilsan
- Issues: [Саад гараагүй]
- bug ID: baihgui

### 16:33-16:40 T10: API surug test - hooson nomiin ner

- Endpoint: POST http://localhost:3000/api/books
- Request body:
  {
  "title": "",
  "author": "Munkhtstesen",
  "year": 2000
  }
- Expected: [API 400 bad request esvel 422 butsaaj nom uusgehgui baih]
- Actual: [API 201 created hariu butsaaj {"result":"OK","id":11} gesen hariugaar shine burtgel uusgesen]
- Result: FAIL hooson nertei nomiin ugugdliig api huleen avsan
- Issues: [Саад гараагүй]
- bug ID: bug-06
- Evidence: evidence/T10_api_empty_title.txt evidence/T10_api_empty_title.png

## Цагийн задаргаа

- Session 60 minute
- Setup: 5 minute [8.3]%
- Тест дизайн ба гүйцэтгэл: 45 minute [75]%
- Согог судлах: 10 minute [16.7]%
