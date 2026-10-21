# Session report

**Тестер:** [Т.Мөнхцэцэн]

**Огноо:** [2026-10-21, 10:22 – 11:46]

**Mission:** Уншлагын жагсаалт аппын чанарыг шинжлэх

**Charter:** Ном нэмэх, хайх, устгах, хүснэгт ба тоолуурын нийцэл, API-ийн буруу оролтын боловсруулалтыг шалгах.

## Тэмдэглэл (он цагийн дарааллаар)

### 10:22–10:30 - Ehnii tuluv shalgah

- App: http://localhost:3000
- Ehnii husnegtiin muriin too : [4] table header orson
- Niit nomiin too: [4]
- Husnegtiin baganuud: [4]
- Ustgah tovchnii ungu: [Nogoon]
- Screenchot: screenshots/initial_state.png

### 10:33 T01: Ner zohiogch, 1999 gesen onii utgiig hiigeed nemeh tovch darsan

- Expected: [Nom amjilttai nemegdej, husnegted shine mur uusch niit nomiin tooluud 1 eer nemegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine nur nemegdsen, niit nomiin too 1 eer nemegdej 5 bolson]
- Result: Pass - nom nemeh uildel amijilttai bolson

### 10:39 T02: Nomiin ner hooson uyd shalgah

- Expected: [Nom nemegdehgui aldaanii medeelel gargana]
- Actual: [Nom nemegdlee gesen text garch husnegted shine mur nemegdsen gedhee garchig heseg hooson, niit nomiin too 1 eer nemegdej 6 bolson]
- Result: Fail hooson garchigtai nomiig app zuvshuurch nemsen
  [Тест хийхэд саад болсон зүйлс. Саад гараагүй бол "Саад гараагүй" гэж бичнэ.]
- Bug ID: BUG-01

### 10:45 T03: Zohiogchiin ner hooson

- Expected: [Nom nemegdehgui aldaanii medeelel gargana]
- Actual: [Nom nemegdlee gesen text garch husnegted shine nur nemegdsen gedhee garchig heseg hooson, niit nomiin too 1 eer nemegdej 7 bolson]
- Result: Fail hooson Zohiogchiin nertei nomiig app zuvshuurch nemsen
  [Тест хийхэд саад болсон зүйлс. Саад гараагүй бол "Саад гараагүй" гэж бичнэ.]
- Bug ID: BUG-02

### 10:49 T04: Huchintei bus on - 999

- Expected: [Nom nemegdehgui buruu oniig medegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine nur nemegdsen, niit nomiin too 1 eer nemegdej 8 bolson]
- Result: Fail zuvshuurugduugui onii nomiig app zuvshuurch nemsen
  [Тест хийхэд саад болсон зүйлс. Саад гараагүй бол "Саад гараагүй" гэж бичнэ.]
- Bug ID: BUG-03

### 10:54 T05: Huchintei bus on - 2101

- Expected: [Nom nemegdehgui buruu oniig medegdene]
- Actual: [Nom nemegdlee gesen text garch husnegted shine nur nemegdsen, niit nomiin too 1 eer nemegdej 9 bolson]
- Result: Fail zuvshuurugduugui onii nomiig app zuvshuurch nemsen
  [Тест хийхэд саад болсон зүйлс. Саад гараагүй бол "Саад гараагүй" гэж бичнэ.]
- Bug ID: BUG-04

### 10:54 T06: Davhardsan nom 2 udaa nemeh oroldlogo hiisen

- Expected: [Ijil ner, zohiogchtoi nom davhar nemegdehgui]
- Actual: [Nom nemeh uildliig sanamsarguigeer 2 udaa guitsetgnii ulmaas husnegted 2 shine mur nemegdej Nom nemegdlee gesen text garch husnegted shine murnuud nemegdsen, niit nomiin too 2 oor nemegdej 11 bolson]
- Result: Davhardsan nertei, zohoigchtoi nomiig 2 udaa nemehed 2 uuland ni app zuvshuurch nemsen
- Tailbar: Testiin uildliig tuluvlusnuud olon udaa guitsetgesen tul dung batalgaajuulah bolomjgui bolson. Testiig dahin zuv guitsetgene
- Bug ID: BUG-05 batalgaagui

### 11:04 T06: Davhardsan nom 1 udaa nemeh oroldlogo hiisen

- Expected: [Ijil ner, zohiogchtoi nom davhar nemegdehgui]
- Actual: [Nom nemegdlee gesen text garch husnegted shine murnuud nemegdsen, niit nomiin too 1 eer nemegdej 12 bolson]
- Result: Davhardsan Ner, zohiogchtoi nomiig app zuvshuurch nemsen
- Bug ID: BUG-06

### 11:10 T07: Nom haih uildel

- Expected: [Haisan nom husnegted haragdana, hailtad tohiroogui busad nom haragdahgui, niit nomiin tooluur uurchlugduhgui]
- Actual: [hailtiin hesegt nomiin buten neriig oruulaad haih tovchiig darahad husnegted tuhain nertei nomuud haradgsan mun husad nom haragdaagui, niit nomiin tooluur uurchlugduugui]
- Result: Pass app hailtad tohirson nomiig husnegted haruulsan
- Bug ID: baihgui

### 11:13 T08: API test - Nom nemeh

- Endpoint : POST http://localhost:3000/api/books
- Request body:
  {
  "author": "Munkhtstesen",
  "title": "test nom 6",
  "year": "2000"
  }
- Expected: [Huchintei ugugdultei huselt ilgeehed nom amjilttai nemegdej amilitiin hariu butsna]
- Actual: \
  {
  "result": "OK",
  "id": 12
  }
- Result: Pass api hulet amijilttai bolovsruulagdaj id: 12 buhii burtgel uussen
- Bug ID: baihgui

### 11:32 T09: Nom ustgah test

- Ustgahaas umnuh niit nom: 13
- Ustgahaas umnuh husnegtiin muriin too: 13
- Expected: [Songoson nom husnegtees ustaj, husnegtiin muriin too bolon niit nomiin too tus bur 1 eer buurna]
- Actual: [Ustgah tovchiig darsnii daraa songoson nom husnegtees arilsan, husnegtiin muriin too 13->12 bolj niit nomiin too 13-> 12 bolson]
- Result: PASS - num ustgah uildel amjilltai ajilsan
- Bug ID: baihgui

### 11:39 T10: API surug test - hooson nomiin ner

- Endpoint: POST http://localhost:3000/api/books
- Request body:
  {
  "title": "",
  "author": "Munkhtstesen",
  "year": 2000
  }
- Expected: [API 400 bad request esvel 422 butsaaj nom uusgehgui baih]
- Actual: [API 201 created hariu butsaaj {"result":"OK","id":15} gesen hariugaar shine burtgel uusgesen]
- Result: FAIL hooson nertei nomiin ugugdliig api huleen avsan
- Bug ID: BUG-07
- Evidence: evidence/T10_api_empty_title.txt evidence/T10_api_empty_title.png

## Цагийн задаргаа

- Session 84 minute
- Setup: 11 minute [13]%
- Тест дизайн ба гүйцэтгэл: 56 minute [67]%
- Согог судлах: 17 minute [20]%
