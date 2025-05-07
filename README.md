# TIL


-----


## VS code 주요 단축키
* `ctrl+k` -> `ctrl+\`위-아래 수직 화면 분할
* `ctrl+k` 좌-우 화면 수평 분할
* `ctrl+j` 터미널 실행-닫기
* `q` or `ctrl+c` 터미널 입력 불가 에러 해결


-----


## 작업폴더 설명
* `html_basic/` : html 기초 연습 파일 모음
* `take/` : 과제 제출 폴더, 파일 모음 (폴더 명은 날짜 별로 구성)
* `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록


-----


## 웹폰트 코드
* 구글 폰트 : https://fonts.google.com/?lang=ko_Kore

* 프리텐다드 :
```
<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard-dynamic-subset.min.css" />
```

* 노토 산스 :
```
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100..900&display=swap" rel="stylesheet">
```


-----


## 웹폰트 사이즈 (px to em) 단위 변환 사이트
* https://nekocalc.com/px-to-em-converter


-----


## 2025-04-04 : HTML(3)
* `h1~h6`, `p`, `br`, `strong`, `em`, `del`, `s`, `sup`, `sub`
* `<blockquote></blockquote>`: 긴 인용문 태그
* `<blockquote cite="출처 주소"></blockquote>`로 사용
* 블록 태그, 사용은 잘 안 함
* `<q></q>` : 짧은 인용문에 사용하는 인라인 태그로 잘 사용되지 않음
* `<adress></adress>` : 웹사이트의 관련 연락처 소개 고객센터 정보 등을 담을 때 사용하는 블록 태그로 주로 풋터 영역에 위치
* `<code></code>` : 컴퓨터가 지원하는 다양한 명령어를 화면에 표시할 경우에 사용하는 인라인 태그로 자주 쓰이지 않지만 강의 사이트 등에서 사용
* `<hr>` : 수평선 태그로 사이트 각 영역을 구분, 태그 구조 이해할 때 사용되며 css에서는 표현하지 않고 숨김
* 특수문자를 쓰기 위한 태그 : `&lt;`, `&gt; `, `&coopy;` -> 특수 문장 부호를 html 문서가 인식하게끔 표현


-----


## 2025-04-07 : HTML(4)
* `div`, `span`
* `<div></div>`, `<span></span>`
* 웹, 앱 레이아웃 방향과 의미에 따라 2개 이상의 요소를 묶어주는 태그
* 레이아웃 태그 div, span은 2개 이상의 블록 또는 인라인 태그를 묶어주는 그룹 용도로 묶는 대상이 블록이라면 div 태그, 인라인라면 span 태그로 사용
* `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 선택해야 하지만 `span`은 선택
* `div`는 줄바꿈이 되지만 `span`은 줄바꿈이 되지 않음
* 이름 작성 시 반드시 용도에 맞는 의미있는 영단어 사용 (해시태그 개념)
* `a` : 링크 태그 (인라인 태그)
* `<a></a>`
* `<a href="주소"></a>` : href 속성을 통해 다른 페이지나 같은 페이지의 다른 url로 연결할 수 있는 하이퍼링크 만듦
* href 속성 안 값은 링크 목적지 주소를 정확히 입력
* 링크 주소는 일반적으로 '절대 경로'와 '상대 경로'로 나뉨
* 링크 영역 넓게 잡아야
* `<a href="주소" target="_blank"></a>` : url을 새로운 창에 표시


-----


### html 구조 공부 순서
1. 클론 코딩 & 클론 디자인할 사이트 정하기
2. 피그마에서 와이어프레임 만들기 (레이어, 폴더 이름 주의)
3. 피그잼에서 일부 화면 넘겨서 태그 계획
4. 계획한 태그를 가족 관계에 맞게 트리 구조 만들기
5. vs code에서 실제 html 작성하기 (트리구조 순서에 맞게 바깥쪽 -> 안쪽으로)


-----


### 다른 환경에서 git 이어서 작업하기
1. 새 폴더 연결하기
2. `git clone 저장소 주소 붙여넣기`
3. 터미널 경로 오른쪽에 `main` 또는 `master`표시 확인
4. 위 3번이 없으면 `cd+복제한 폴더명`입력
5. 자유롭게 수정 후 파일 저장
6. 터미널에 `git status` 업로드 안 된 파일 빨간색 확인
7. 터미널에 `git add .` 수정한 파일 스테이지에 업로드
8. `git status` 위 7번 업로드 녹색 됐는지 확인
9. `git commit -m '기록 메세지'` 수정 파일에 대한 기록 작성
10. `git push origin main` 깃허브 저장소에 업로드
### 이어서, 다른 환경에서 git 이어서 작업하기 (학원)
1. `git pull origin main` 집에서 올린 파일 내려받기
* 집에서 고정 연결된 후에는 저장소 받지 않고 `pull`하면 됨


-----


## 2025-04-08 : HTML(5)
* 상대 경로 : 경로를 작성하는 파일 기준으로 연결하는 파일의 위치 작성
* 파일 위치 같을 때 :  `./파일명/확장자`
    * `<a href=”./파일명.확장자”>파일 이동</a>`
    * `<a href="./link.css">link css 이동</a>`
* 파일 위치 다를 때 - 하위 위치 경로 : `./폴더명/파일명.확장자`
    * `<a href=”./폴더명/파일명.확장자”>파일 이동</a>` 
    * `<a href="./styles/link.css">link css 이동</a>`
* 파일 위치 다를 때 - 상위 위치 경로 : `../파일명.확장자`
    * `<a href="../파일명.확장자">파일 이동</a>`
    * `<a href="../link.css">link css 이동</a>`
* 상대 경로 준비 되어 있지 않을 때는 `#`으로 임시 링크를 걸어둠

### 바로가기 링크 만들기
0. 화면이 수직으로 충분히 이동할 수 있을만큼 긴 세로 스크롤 준비
1. 바로 가기 할 메뉴에 `a` 태그 작성
2. 바로가기 할 곳 `div`그룹 상위에 `<div id="아이디명"><div>` 설정
3. 1번 바로가기 메뉴 `a` 태그에 속성 `href` 값으로 2번 이름 `아이디명` 작성
    * `<a href="link"></a>` 태그 중 링크에 `#아이디명`입력
    * `href`에 `#`만 있으면 임시 링크이지만 `#아이디명`이 되면 `#`이 `id`를 대체, 아이디명으로 바로가기 링크가 됨
4. 최종 바로가기 링크 : `<a href="#아이디명"></a>`
    * 바로 가기 링크는 같은 파일 내 다른 위치로 이동

### 응용
* `<a href="./basic/index.html#main">이동 하기</a>`
    * 상대 경로의 파일(문서)에서 아이디 main으로 이동
* 파비콘 공통 코드
    * 
    ```
    <link rel="shortcut icon" href="파비콘.ico 경로" type="image/x-icon">`, `<link rel="icon" href="파비콘.ico 경로" type="image/x-icon">
    ```

-----

## 2025-04-09 : HTML(6)
### `<img>` : 이미지 태그(인라인, 빈 태그)
* `<img src="이미지 주소, 경로">`
* 대체 텍스트 `alt`필수 작성 (의미 없는 이미지에는 값 안 써도 됨)
* `<img src="url" alt="대체 텍스트>` 
* src 이미지 경로 속성의 값으로는 상대 경로 방식으로 작성 권장

-----


#### `<video></video>` : 동영상 태그 (블록 태그)
* 작성 방법 1. 
```
<video src="동영상 경로, 주소"></video>
```
* 작성 방법 2. 
```
<video><source src="동영상 경로, 주소" type="동영상 타입1"><source src="동영상 경로, 주소" type="동영상 타입2"></video>
```
    * 브라우저에서 동영상 재생 될 수 있는 타입을 선택해서 자동으로 재생됨, 1번 방식을 더 자주 씀
* 동영상 태그의 주요 속성 종류와 뜻
    - autoplay : 자동 재생
    - muted : 음소거
    - controls : 동영상 컨트롤러 보이기
    - loop : 동영상 반복 설정
    * 
    ```
    <video src="동영상 경로, 주소" autoplay muted controls loop></video>
    ```
* `autoplay` 사용 시, `muted` 필수
* `poster=""` 동영상에 썸네일 (미리보기) 기능, autoplay 불가
```
<video src="동영상 경로, 주소" muted controls loop poster="이미지 경로, 주소"></video>
```
* 이미지와 영상은 임시 링크 `#` 사용 불가


### 유튜브에서 영상 가져왔을 때 자동 재생하게 만드는 법
1. 유튜브에서 영상 소스 코드 복사
2. `ifram` 형태의 소스 코드 붙여넣기
3. `<ifram>` 속성 `src=""`에서 마지막 따옴표 직전에 `?autoplay=1&mute=1&loop=1&playlist=영상 이름` 입력
4. 3에서 영상 이름은 src 값에서 embed의 뒤에 있는 코드
    * `유튜브닷컴/embed/영상 이름`


-----


### `<ol><li></li></ol>` : 순서가 있는 목록 태그 (블록 태그)
* `<li></li>` 2개 이상의 목록
* `<ol></ol>` 목록을 묶는 그룹 태그, 순서가 있는 목록 태그, 목록의 div격
    * o를 one(1)으로, 숫자 목록 태그라고 외우면 편함
* `<li>`의 형제는 `<li>`만 가능, 다른 태그 쓸 때는 자식 태그로 작성
* `<ol>` 태그는 반드시 `<li>` 태그의 가장 근접한 부모 태그로 작성
* `<ol>`은 그룹이므로 `class=""` 작성
* `<ul><li></li></ul>` : 순서가 없는 목록 태그 (블록 태그)
* 목록`<li>`의 순서와 연관 없을 경우 `<ul>` 사용
* `<ul>`은 그룹이므로 `class=""` 작성, 목록의 div격
* 주의사항 : 목록 태그 사용 시 다른 블록 및 인라인 태그를 사용하려며 반드시 `<li>` 안에 작성
* `<ul>`또는 `<ol>` 과 `<li>`에 다른 태그 사용 불가


-----


## 2025-04-10 : HTML (7)
* `html:5` : vs code에서 자동 완성 되어 기본 양식 작성해줌
* `viewport` : 사용자가 보는 화면


-----


### `<dl><dt></dt><dd></dd></dl>` : 정의형 목록 태그, `h` 태그를 따로 설정하지 않아도 됨
* `<dl>`은 정의형 목록 태그에서 제목과 내용을 묶는 그룹, div 
* `<dt>`는 `<dl>` 안에 속하며 제목이 됨, 제목에서 레벨은 존재하지 않음, h2~3과 비슷함
* `<dt>`다음에는 무조건 `<dl>`이 와야함
* `<dt>`는 항상 `<dd>`보다 먼저 시작
* `<dd>`는 `<dl>` 안에 속하며 `<dt>`이후 작성, `<dt>`와 형제이며 `<dd>`와도 형제 가능
* `a`태그에서 링크 새 창으로 열기 속성 태그
```
onclick="window.open(this.href, '_blank', 'width=500 height=500'); return false;"
```


-----


* 집에서 공부한 내용 (퀴즈가 납득 안 됨)
1. p태그는 ul태그보다 우선 순위가 낮다?
2. p태그는 li태그보다 우선 순위가 높다?
    * 문장에서 기준이 분명하고 명료하지 않아 출제가 잘못 되었음
* 이유
    * `<p>`, `<ul>`, `<li>` 태그는 전부 HTML에서 블록 레벨 요소
    * `<p>`태그 안에는 "인라인 태그"만 삽입 가능
    * 따라서 `<ul><li><p>OK!</p></li></ul>`로 사용해야 문법적으로 문제가 없음
    * 그러므로 중첩 가능성 기준으로는 ul > li > p 순으로 감싸는 게 가능하고 자연스러움
* p와 ul은 블록 태그로 각각 단독으로 쓸 수 있어 우선 순위를 매기는 게 무의미하나, 페이지 내에서 중요도에 초점이 맞춰지면 ul이 우선순위 높을 수도 있음
* p와 li만 두고 봤을 때 단독으로 쓸 수 있냐 없냐 차이면 p가 우선순위가 높지만, p는 li 안에 속할 수 있으나 li는 p안에 속할 수 없음 -> 이 경우 p는 li보다 우선순위 낮음


-----


* a 태그는 블럭태그이다? -> 아님
* 이유 : `<a>`태그는 인라인 태그로 html5에서 패치되면서 블록 태그의 기능을 할 수 있게 되었으나 어디까지나 정의는 "인라인 태그"임
* a태그를 블록 태그라고 표현하면 안 됨


-----


* `<a>` 태그 안에 `<p>` 태그를 넣는 건 HTML5에서 가능하게 패치된 기능
    * `<a href="#"><p>이제는 이렇게도 쓸 수 있어요!</p></a>`
    * **하지만! 실무에서는 이렇게 쓰는 건 주의가 필요** 
    * 대부분은 이렇게 쓰는 게 더 자연스럽고 문제 없음: `<p><a href="#">여기에 링크 걸기</a></p>`


-----


## 2025-04-11 : html(7)
### gnb(global navigation bar) : 사이트 최상단 내비게이션, 어떤 페이지에 들어가도 고정되어있는 주 메뉴

### lnb(local navigation bar) : gnb의 하단에 배치된 서브 메뉴, 중분류 메뉴
    * 알파벳 순서 (g가 먼저, l이 나중)로 외움 : gnb가 최상단, lnb가 그 다음

### snb(side navigation bar) : 페이지 내에 좌/우측에 일반적으로 존재하는 추가 메뉴, 서브메뉴X

### fnb(footer navigation bar) : 사이트 최하단 내비게이션, footer영역에 존재하는 회사소개, 저작권 등의 보조메뉴

### BreadCrumbs(브레드크럼) : 서브페이지에 표시된 현재 페이지 경로(헨젤과 그레텔의 집을 찾아가기 위해 길에 빵부스러기를 버린 예시)
* 위의 것들은 ul, ol 등의 목록 태그에서 클래스명으로 쓰임


-----


## 2025-04-14 : CSS(1)
### css (cascading style sheets) : 사용자에게 시각적으로 보이는 문서를 꾸미는 언어
* 단계별로 적용 디자인


-----


* css selector : 선택자 {속성:값;}
* 선택자 : css로 디자인하고자하는 대상
* {} : 속성과 값을 묶어주는 css 디자인 괄호
* 속성 : 선택자에 적용하는 속성
* ; : 속성 값 종료
* 속성 : color 글자색, background-color 배경색


-----


### 글자 및 배경색 설정 속성은 아래와 같다.
- `color:rgb(255,255,255);`
- `color:rgba(255,255,255,0.5);`
- `color:#ffffff;`
- `color:#fff;`
- `color:white;`
* 보통 rgba, 헥사코드를 많이 사용
* 헥사코드 사용 시 6자리 모두 같은 숫자 또는 알파벳일 때 3자리로 압축 가능


-----


### 내부 스타일 : `<head>` 태그 내에 `<style>`태그로 작성
### 외부스타일 : 별도의 css 파일을 생성하여 `<link>`태그로 연결하는 방법
* `<link>`태그는  `<head>` 태그 내에 작성
* `<link href="./styles/first.css" rel="stylesheet">`
* html 내부에 작성하는 css는 해당 html파일에만 종속되어 외부 html 에 연결할 수 없으므로 효율적이지 못함
    * 따라서 외부스타일이 더 많이 사용됨


-----


* Cross-Browsing :  internet browser간의 호환성을 뜻함


-----


## 2025-04-15 : CSS(2)
### font-family (글꼴 지정) : `font-family:dotum, gulim, '맑은 고딕', sans-serif;`
* 가장 첫번째 위치에 오는 글꼴이 메인 글꼴이고 그 뒤에 따라오는 글꼴은 메인 글꼴 적용되지 않는 상황에서 사용하는 후보 글꼴 
글꼴명이 한글 또는 공백이 포함되었을 경우(영문 폰트 포함) 따옴표 사용
* 폰트 유형에 따라 마지막에 sans-serif 또는 serif 입력
* 웹폰트 사용 시 html 헤드 부분에 스타일 시트처럼 웹글꼴 연결해야 적용 됨

* **font-weitght (글꼴 굵기)** : `font-weight: 400;`
* 기본 사이즈는 400, 글꼴마다 적용 가능 정도가 다름

### font-size (글자 크기)
* 글자 크기 적용 코드는 아래와 같다.
    - `font-size:16px;`
    - `font-size:100%;`
    - `font-size:1.0em;`
* 데스크톱 환경의 글자 내용 크기 16pt, 모바일 태블릿 환경 글자 내용 크기 14pt
* 픽셀 단위는 절대 크기값으로 사용자별 글자 크기 지원 안 함
* 픽셀 단위가 아닌 em rem % 상대적 단위 사용해야 함
* 보통 rem 사용
    * 이유 : em 사이즈를 적용하게 되면 태그에 자식이 있을 때 00@0로 추가 적용되기 때문 (글자 크기를 0상대적로 인식)
    * 자식은 부모 사이즈+본인사이즈 갖게 됨
* 사이트에서 글꼴 사이즈를 px->em 단위 변환하여 em을 rem(부모 글자 크기 관계 없이 절대적으로 인식)으로 하면 해결 완료

### **line-height (행간)
* 글자 행간 적용 코드는 아래와 같다
    - `line-height:1.5;`
    - `line-height:150%;`
    - `line-height:150px;`
* 디자인 상황에 따라 px과 % 유동적으로 사용
* line-height를 이용한 수직 정렬 주의사항
* 요소의 height 값이 px로 작성된 경우 그 값을 그대로 line-height의 px값으로 작성하여 수직 가운데 정렬을 적용
* 단, 글자가 2줄 이상일 경우에는 적용 금지 -> 무조건 1줄 일 때만 사용

### letter-spacing (자간)
* 자간 적용 코드는 아래와 같다.
    - letter-spacing:0;
    - letter-spacing:-0.5px;
    - letter-spacing:-0.05em;
* 자간과 행간은 디자인 프로그램 상 보이는 것과 코딩 시 보이는 것이 미세한 차이 발생할 수 있음
* 주로 em 사용
* 기본값 : 0
* -0.02em = 피그마 -2%

### word-spacing 단어와 단어 사이 간격
* 적용 코드는 아래와 같다.
    - word-spacing:1px;
    - word-spacing:-0.05em;
* 주로 em 사용
* 기본값 : 0
* css 크기 속성 : `width: 200px; height: 200px;`

### css 글자 정렬 : `text-align: center(orleft, right);`
* text-align 속성은 속성 값을 입력한 대상 기준으로 그 자식 또는 자손이 인라인 요소일 경우에만 적용
    → 단순 글자도 인라인으로 인식하기 때문


-----


### `display: inline-block;` : a태그를 css 속성을 이용하여 크기를 인식하는 블럭으로 변환

### `border-radius: 30px;` : 박스에 모서리 라운드, 모서리마다 따로 라운드 줄 수 있음

### `list-style-type: ;` : 목록 머리 기호
- none : 지정하지 않음
- disc : 검은 원형
- lower-roman : 소문자 로마자
- decimal : 1부터 시작하는 10진수
- upper-alpha : 대문자 알파벳
- circle : 원형
- square : 사각형
- lower-alpha : 소문자 알파벳
- upper-roman : 대문자 로마자

### `list-style-position: inside or outside;` : 글머리 기호의 위치
* 가운데 정렬 글자 가운데에 배치하고 싶을 때 둘 다 적용
```
width: <width>`,`margin-left: auto;`, margin-right: auto;` 
```


-----


### css style sheet
* 외부 스타일 시트 파일 저장 **styles**폴더에 `파일명.css`저장
* css 파일 생성 후 css 연결 원하는 html파일 head위치에 `<link>`태그로 연결
* html 작성 후 html의 모든 디자인 설정을 초기화하는 `reset.css`을 `파일명.css` 위에 연결
* 웹글꼴 연결 시 html 파일에 `<link>`태그로 `파일명.css` 위에 연결

### head 태그 내에 들어가는 link 태그 작성 순서
1. 웹글꼴 포함 기타 플러그인 연결
2. reset.css
3. 해당 html별 디자인.css

### 디자인 css 작성 시 순서 및 주의사항
* **부모 > 자식** 순서로 가장 바깥쪽 부모부터 먼저 선택자를 만들고 디자인
* 레이아웃 관련 요소에 `width, height` 속성 작성 시 영역 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분 -> 이때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink` 등의 밝은 색상 위주로 사용하고 영역 확인과 디자인 작업을 모두 마친 후 `background-color` 제거, 마무리
* 실제 디자인에 들어가는 색상은 **rgba 또는 헥사코드**로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력

### 자주 이용하는 css 속성 값과 기본값
* `color` : 글꼴 색 -> `color:black;`
* `background-color` : 바탕색 -> `background-color:black;`
* `font-family` : 메인 글꼴 설정 -> `font family:'굴림', sans-serif;`
* `font-size` : 글꼴 크기 설정 / 기본 1rem(16pt) -> `font-size:1.5rem;`
* `font-weight` : 글꼴 굵기 설정 / 기본 400 -> `font-weight:800;`
* `letter-spcing` : 자간 설정 / 기본 0rem -> `letter-spacing:0.2rem;`
* `line-height` : 줄간격 설정 / 기본 100% -> `line-height:150%;`
* `width` : 가로 사이즈 -> `width:300px;`
* `hieght` : 세로 사이즈 -> `hieght:150px;`
* `margin` : 여백 -> `margin:20px;`
* `border-radius` : 모서리 둥글게 -> `border-radius:30px;`


-----


## 2025-04-16 : html(9)
* **시멘틱 태그 (semantic tag)** : 레이아웃 태그를 더욱 의미있게 사용하기 위한 공통 단어들을 태그 형태로 만들어둔 태그 모음 -> div가 아님

### `<header></header>`
* 로고 및 내비게이션을 묶어주는 웹 사이트 레이아웃 태그
* 제목, 로고, 검색 폼, 작성자 이름 등의 요소도 포함할 수 있음
* 블럭 태그

### `<nav></nav>`
* 로고 및 웹사이트 주요 내비게이션을 묶어주는 웹 사이트 레이아웃 태그
* 다른 페이지로의 링크를 보여주는 구획
* 자주 쓰이는 예제는 메뉴, 목차, 색인 -> gnb
* 블럭 태그

### `<section></section>`
* 문서의 독립적인 구획
* 제목(H)을 포함하는 경우많음, 필수는 아님
* 블럭 태그
    
### `<aside></aside>`
* 사이드바 혹은 콜아웃 박스로 표현 : 광고, 링크 등 사이드 바
* aside 안에 section
* 블럭 태그

### `<article></article>`
* 사이트 안에서 독립적으로 구분해 배포하거나 재사용할 수 있는 구획
* 게시판과 블로그 글, 매거진이나 뉴스 기사 등
* 블럭 태그

### `<footer></footer>`
* 웹페이지 가장 하단에 위치
* 구획의 작성자, 저작권 정보, 관련 문서 등의 내용
* 블럭 태그
* class 작성 필수

### `<main></main>`
* 문서 `<body>`의 주요 콘텐츠
* 문서의 핵심 주제나 앱의 핵심 기능에 직접적으로 연결됐거나 확장하는 콘텐츠

### `<figure> <img src=”” alt=””><figcaption>설명</figcaption> </figure>`
* 이미지와 그에 대한 설명을 표현 할 때 묶음(figure) 설명(figcaption)순으로 사용
* 블럭 태그

### `<details> <summary>요약</summary> 내용 </details>`
* "열림" 상태일 때만 내부 정보를 보여주는 정보 공개 위젯을 생성
* 요약이나 레이블은 `<summary>` 요소를 통해 제공 가능

### `<mark></mark>`
* 현재 맥락에 관련이 깊거나 중요해 표시 또는 하이라이트한 부분
* em도 가능

### `<time datetime></time>`
* 시간의 특정 지점 또는 구간
* datetime 속성 : 요소의 시간 또는 날짜 값
* datetime 속성을 지정해 보다 적절한 검색 결과나, 알림 같은 특정 기능을 구현할 때 사용

### `<form></from>` : 사용자 입력, 선택 컨트롤 묶음 틀
* ex) 
```
<form action="#" method="post" id="join_frm"></form>
```
* 블럭 태그
* action
    * 사용자가 입력 선택한 데이터 전송하는 서버
    * 값에 서버주소 입력
* method : 데이터 전송 시 전송방법
    * post : 폼 데이터를 http 본문에 포함하여 서버 전송 - 보안 높음
    * get : 폼 데이터를 url에 추가해 서버로 전송 - 보안 낮음

### `<fieldset></fieldset>` : 전체 폼 태그 안 그룹이 필요할 경우 작성
* 폼의 양식을 더 읽기 쉽고 이해하기 편하게 구성하려는 목적
* form의 자식 요소로 배치
* 블럭 태그

### `<legend></legend>` : 그룹 제목, 데이터 구분 목적
* 인라인 태그
* fieldset의 자식으로 배치
* 실제 디자인은 css로 숨김
    * `legend {display: none;} `
    * `reset.css`에 등록

### input : 입력/선택 컨트롤 양식
* 인라인 태그, 빈태그
* 속성은 입력양식 / 선택&목록 컨트롤 양식 종류에 따라 의미가 달라짐
    * **입력 양식 속성**
        * **type : 인풋 요소가 나타낼 입력 필드 종류**
            * text : 한줄 입력
            * file : 파일 첨부
            * password : 입력 보안
            * number : 숫자 (카운트)
            * email : 이메일
            * search : 검색어
            * date
            * time : 시간입력
            * url
            * tell : 전화번호
            * week : 날짜입력(시간x)
            * hidden : 서버로 전송되는 숨김영역의 값


        * **textarea : 여러줄의 텍스트를 입력할 수 있는 입력 필드**
            * **인풋 작성 필요 없음**
            * name :  요소 이름
            * value : 요소 초기값 
            * rows : 요소 세로 크기 지정
            * cols : 요소 가로 크기 지정
            * disabled : 요소 비활성화
            * placeholder : 요소 입력 텍스트 지정
            *  required : 필수 입력 처리
            *  form : 요소가 속한 폼


        * **입력 양식 안에 쓸 수 있는 속성**
            * **name : 인풋 요소이 이름 지정 (데이터 구분)**
            * **value : 인풋 요소의 초기값**
            * size : 크기, 보통 css로 조정
            * **maxlength : 글자 수 제한** : type="number"에서 maxlength 적용 불가
            * required : 필수 입력 필드 지정
            * readonly : 읽기 전용
            * disabled : 필드 비활성화
            * autocomplete : 자동 완성 기능, 값은 on/off로 작성
            * accept : 요소에서 허용하는 파일 형식 지정
                * `accept=“img/png, application/pdf, img/*”`
            * multiple : 입력 필드에 여러 이름 입력 시 각 개별 값 처리
            *  **placeholder : 요소 입력 텍스트 지정**

    * **선택&목록 양식 속성**
        *  type : 요소가 나타낼 타입
            * checkbox : 다중 선택
            * radio : 단일 선택
        * **select : 목록(option)을 묶어주는 부모 대상으로 그룹 속성 (name)적용**
            * **option은 select의 자식으로 목록을 의미**
                * 사용자가 실제 선택하는 값으로 데이터 구분값 속성 (value)작성하나 모든 값에 쓸 필요는 없음 -> 사용자가 선택하는 데이터만 사용
        * name : 요소의 이름 지정 같은 선택에 포함될 경우 동일한 이름 처리, 그룹명(동일 그룹)
        * value : 요소의 고유 초기값 지정, 개별 데이터 값
        
        * **label : 글자와 함께 배치된 형태의 input 작업 시 입력, 선택 필드의 편의성, 접근성을 높이기 위해 사용하는 태그**
            * 인라인 태그
            * 모든 input에 사용 가능하나 일반적으로 checkbox, radio에서 편의성 목적으로 많이 사용
            * input의 부모로 감싸거나 **형제 요소**로 사용 가능
                * `for`속성 작성하며 input의 id와 동일하게 입력
                * 반대로 input의 부모라면 for입력 안 해도 됨 (이 경우 반드시 다른 인라인 태그로 묶어야 함) -> 라벨(인풋-스팬)
                * css 불가능 -> `display:none`으로 숨기고 선택글자를 묶은 태그에 `background-image`로 디자인
                    * **상태 선택자 : `:checked`**
                    * 사용자가 체크박스 또는 래디오 버튼 선택했을 때 상태에 따라 스타일 적용
                    ```
                    <input type=”checkbox” name=”ck” value=”ck1”>
                    <input type=”radio” name=”ck” value=”ck2” id=”ck2”>
                    <label for=”ck2”>로그인 상태 유지</label>

                    input[type^=check]:checked{color: pink;}
                    input[name=ck]:checked~label{color: red;}
                    [type^=check] 속성 선택자
                    ```
                    ```
                    <!-- 체크박스 이미지 적용 -->
                    #wrap section .tap_container #login_frm .stay_signed label {
                        font-size: 0.75rem;
                        font-weight: 300;
                    }
                    /* 체크박스 상태에 따라 디자인 변경 */
                    /* background: color image repeat attachment position */
                    /* 체크 안 됐을 때 */
                    #wrap section .tap_container #login_frm .stay_signed input[name$=stay] + label {
                        background: url(../images/unchecked.png) no-repeat 0px 1.5px;
                        background-size: 16px;
                        padding-left: 25px;
                    }
                    /* 체크 됐을 때 */
                    #wrap section .tap_container #login_frm .stay_signed input[name$=stay]:checked + label {
                        background: url(../images/checked.png) no-repeat 0ox 1.5px;
                        background-size: 16px;
                        padding-left: 25px;
                    }
                    ```
            * 연결하려는 input이 가진 id 명(input의 value와 id 값 같음)과 동일한 값을 label의 for 속성 값으로 입력
            * 사용자가 선택하려는 이미지 또는 글자를 묶어서 작성


*  **버튼 요소 : reset, submit, button**
    * `button type="속성 종류" id="버튼 구분명"> 보이는 글자 or 이미지</button>`
    * 인라인 태그
    * 컨트롤 양식들을 입력 후 최종 전송 형태를 결정할 때 사용
    * 컨트롤 양식 전송할 경우 submit : `form action`주소에 `method`값 형태로 전달되는 최종 서버 전송 버튼
    * 컨트롤 양식 초기화할 경우 reset : 취소 또는 삭제
    * 다양한 용도의 범용 버튼으로 사용 시 button을 사용 : 주소 찾기, 중복 확인, 이전, 다음 재생, 정지 등
    * input type 속성 값으로 시작하는 방법과 button 태그를 입력하는 방법으로 나뉨


-----


## 2025-04-17 html(10)
### `reset.css`
```
/* 모든 태그 공통 초기값 */
html, body, h1, h2, h3, h4, h5, h6, 
p, div, dl, dt, dd, ul, ol, li, blockquote, address, video, hr, 
header, footer, aside, form, nav, article, section, figure, figcaption, main, details, summary,
form, fieldset, legend, input, button, section, option, textarea,
a, span, em, del, img, br, code, q, sup, sub, s, strong, mark,
table, thead, tbody, tfoot, tr, th, td {
    font-size: 1em;
    font-weight: 400;
    line-height: 100%;
    letter-spacing: 0;
    word-spacing: 0;
    color: #808080;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "pretendard", sans-serif;
    font-style: normal;
}

/* 개별 태그 초기값 */
a {text-decoration: none;}
ul, ol, li {list-style: none;}
fieldset {border: 0;}
legend {display: none;}
input {border: 0; outline: none;}W
button {border: 0; background: none; cursor: pointer;}
table, tr, th, td {border-collapse: collapse;}
select, option {border: 0; background: none; appearance: none; outline: none;}

/* 크로스브라우징을 위한 인풋 태그 초기화==================================== */
/* 웹브라우저 엔진 -webkit-, -moz-, -m-, -o- */
/* 크롬 사파리 엣지 오페라 */
input[type=number]::-webkit-outer-spin-button,
input[type=number]::-webkit-inner-spin-button {
    -webkit-appearance: none; margin: 0;}
/* 파이어폭스 */
input[type=number] {
    -moz-appearance: none;
    margin: 0;
}
```

### placeholder 선택자
```
 #main_wrap #login_frm input::placeholder {
    color: #B3B3B3;
    font-size: 0.75rem;
    font-weight: 300;
}
```


-----


## 2025-04-18 html(11), css(3)
### css
### `display`
* display 요소 표시 속성
* HTML이 가지는 기본 요소의 속성을 다른 속성으로 변경 시 또는 요소를 숨기거나 표시할 경우 사용
* 블록 또는 인라인 표시 속성을 변경하여 외부 표시 유형 설정
* 크기나 여백을 사용할 때는 그 대상이 블록/인라인 어느쪽에 해당되는 대상인지를 먼저 체크하고 그에 따른 속성과 값을 배치해야

### `display: block;`
* 기본 너비 100%
* 크기, 여백 적용이 가능
* **너비100%와는 별도로 항상 줄바꿈**

### `display: inline;`
* 인라인 태그 내 내용(텍스트 및 이미지)의 크기만큼만 인식
* 크기를 적용할 수 없음
* 여백(margin, padding)이 적용은 되나 크기 적용불가 특징으로 인해 주변 요소와 겹침현상이 발생
* 줄바꿈이 되지 않고 옆으로 나열

### `display: inline-block;`
* CSS display 명령으로 적용
* 크기, 여백 적용이 가능
* **줄바꿈이 되지 않고 옆으로 나열**
* 인라인-블록 요소 사이 기본 공백이 포함

### `display:none;`
* 요소의 위치, 크기 포함 숨기기

### `visibility : visible or hidden;`
* display:none과 달리 레이아웃을 변화시키지 않고 요소를 숨기는 속성
* 자바 스크립트 동적 처리 시 요소의 자리는 유지하고 숨겨야 하는 경우 주로 사용

### `margin` 바깥쪽 여백 / `padding` 안쪽 여백
* margin : 부모-자식 요소 여백
* padding : 형제 요소 여백
* 값이 0일때는 단위를 생략 가능, 1 이상일 경우는 반드시 단위를 작성
* 값을 1개 작성할 경우 상/하/좌/우에 모두 동일한 값이 적용 -> `padding: 10px;`, `margin: 10px;`
* 상 우 하 좌 값이 각각 다를 때 : `padding: 50px 100px 200px 0;`
    * 읽는 순서 : top -> right -> bottom -> left
* 상하 / 좌우에 각각 다른 값일 때 : `margin: 10px 20px`, `padding: 10px 20px`
* 상/좌우/하에 각각 다른 값d일 때 : `margin: 10px 20px 5px`, `padding: 10px 20px 5px`

### `border` 테두리
```
<!-- 테두리 두께 / 테두리 형태 / 색 -->
border:1px solid red;
border:1px dashed black;
border:1px dotted coral;

<!-- 변마다 따로 값 적용 -->
border-top:1px solid #aaa;
border-bottom:1px solid #aaa;
border-left:1px solid #aaa;
border-right:1px solid #aaa;

<!-- 테두리 두께, 모양, 색 -->
border-width:1px;
border-style:solid;
border-color:red;

<!-- 꼭지점 둥글게 -->
border-radius:10px;
border-radius:10%;
border-radius:50%;
``` 
* 테두리 모양 종류 : solid, dashed, dotted, double, inset, outset, groove, ridge


## html
### `table` : 표 태그(block)
* 행,열을 자식, 자손으로 가지는 부모로써 존재
* 테이블의 테두리 기본값은 0
* 블록 태그여도 크기는 내용(텍스트)만큼 사용
    * `thead`, `tbody`, `tfoot` 행 그룹
        * 행그룹은 행(tr)의 부모로 사용
        * `thead` : 제목행그룹, th위주로 구성된 제목행(tr)을 묶을 때 사용
        * `tbody` : 내용행그룹, td위주로 구성된 내용행(tr)을 묶을 때 사용
        * `tfoot` : 결과행그룹, th&td들로 구성된 결과값을 가지는 결과행(tr)을 묶을 때 사용
            * tfoot은 tbody위에 위치해도 항상 테이블의 마지막 단에 위치
            * 근데 이제 유효성 검사하면 오류 뜸
    * `tr`(block) : 행
    * `td`(block) : 열
        * 열(td)은 항상 행(tr) 안에 존재
    * `th` : 제목 열
        * 제목 - 내용 순서로 배치하기 위해 제목(th)이 먼저 시작, 내용(td)이 다음 순서로 배치
        * th, td는 형제관계
        * th, td는 tr(행) 안에서만 존재
```
<table>
    <tfoot>
        <tr>
            <td></td>
            <td></td>
        </tr>
    </tfoot>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>
```

### `colspan`, `rowspan`
* th, td에 사용하는 속성
* `colspan` : 같은 가로 행(tr)에 배치된 2개 이상의 열(th, td)을 합칠 때 사용
* `rowspan` : 서로 다른 가로행(tr)에 배치된 2개 이상의 열(th, td)을 합칠 때 사용
* colspan과 rowspan 값은 합쳐지는 총 열의 개수를 입력
* 
    1. 합치고 싶은 가로 방향, 세로방향 열 또는 행 2개 이상 정하기 (갯수 제한 없음)
    2. 위에서 정한 태그 확인
    3. 위 태그 중 먼저 시작한 태그 속성으로 colspan="합치는 칸의 갯수", rowspan="합치는 칸의 갯수"
    4. 합쳐지는 첫 번째를 제외한 나머지 태그는 주석으로 가리기
```
<table>
    <tr>
        <td colspan="2"></td>
        <!--<td></td>-->
    </tr>
</table>
```
* scope : 행과 열 범위 지정
    * 제목열(th)에 사용하는 속성
    * 각 제목과 내용으로 복잡하게 얽혀있는 표의 이해를 돕기 위해 연관 범위를 지정해주는 속성
    * 읽는 방향에 따라 수직(col) 수평(row)로 값을 작성
```
<table>
    <tbody>
        <tr>
            <th scope="col">Name</th>
            <th scope="col">HEX</th>
        </tr>
        <tr>
            <th scope="row">Teal</th>
            <td>#51F6F6</td>
        </tr>
        <tr>
            <th scope="row">Goldenrod</th>
            <td>#F6BC57</td>
        </tr>
    </tbody>
</table>
```

### 수열 선택자
* **`:nth-child(n)`**
    * css에서 요소를 규칙적으로 선택하고자 할 때 사용
    * 특정 부모의 배치된 형제 순서에 따라 대상을 선택
    * 반복 패턴을 따라 자식이 2개 이상 있을 때 n번 째 자식이란  개념으로 선택
    * 의미가 없는 요소에 이름을 붙이지 않고 관계와 순서로 대상을 파악해서 선택자를 만드는 방법
    * 첫째와 막내는 `:first-child`, `:last-child`
```
<div class="box">
  <h1>h1</h1>
  <p>selector1</p><!--적용대상-->
  <p>selector2</p>
  <p>selector3</p>
</div>

.box p:nth-child(2) { background-color:yellow; }
```

* **`nth-of-type`**
    - **형제 그룹 사이에서 자신과 동일한 요소만을 보고 해당 요소 순서에 따라 대상을 선택**
    - 전체 형제 중 같은 태그 종류 중 n번째
    - 첫째와 막내는 `:first-of-type`, `:last-of-type`
```
<div class="box">
  <h1>h1</h1>
  <p>selector1</p><!--적용대상-->
  <p>selector2</p>
  <p>selector3</p>
</div>

.box p:nth-of-type(1) { background-color:yellow; }
```

* **`:nth-child(An)`**
    * A 반복 간격(주기)
    * `:nth-child(3n)` : 3간격으로 형제 요소 선택 (3의 배수) -> 3 6 9 12 번째 요소 선택

* **`:nth-child(An+B)`**
    * A 반복 간격 (주기)
    * B 시작 위치 (기준)
    * `:nth-child(3n+1)` : 3n+1 1번부터 시작해서 3의 배수 -> 1 4 7 10 13 번째 요소 선택

* **`nth-child(odd)`, `nth-child(even)`**
    * odd 홀수, even 짝수 번째 요소 선택


-----
* **overflow** : 요소내의 컨텐츠가 너무 커서 요소내에 모두 보여주기 힘들 때 그것을 어떻게 보여줄지를 지정
    *  `overflow: hidden;`
        * 넘친 컨텐츠는 잘려지고 보이지 않음
    * `overflow: scroll;`
        * 넘친 컨텐츠는 잘리고, 스크롤바가 생겨서 스크롤해서 볼 수 있음
        * 가로/세로 스크롤바가 모두 생김
    * `overflow: auto;`
        * 넘칠경우 스크롤바가 자동으로 생김
        * 가로/세로 필요한 부분에만 생김
    *  `overflow-x`, `overflow-y`
        * 가로, 세로 overflow 를 각각 제어


 -----


## 2025-04-21 CSS(4)
### background 배경 속성
* **background-image:url**
    * 배경이미지는 배경색상보다 우선순위로 높게 처리
```

background-image:url(상대경로)
background-image:url(절대경로)

/*배경이미지 2개 이상 연결하기*/
background-image:url(경로), url(경로)

```

* **background-repeat**
    * 기본 값은 repeat(반복)으로 주로 사용하는 값은 no-repeat 이며 결과형태에 따라 반복 종류가 정해짐
```

background-repeat:repeat; /*반복*/
background-repeat:no-repeat; /*반복안함*/
background-repeat:repeat-x; /*x축 반복*/
background-repeat:repeat-y; /*y축 반복*/

/*배경이미지가 2장 이상이상일 경우 개별속성*/
background-repeat:repeat-x, repeat;

```

* **background-position**
    * 기본 위치는 왼쪽 상단 값으로 위치(left right top bottom center), 값(0%~100%, px)등을 사용
```

background-position:x축 y축;
background-position:left top;
background-position:right bottom;
background-position:center;
background-position:center top;
background-position:50% 30%;
background-position:50%;
background-position:100px 0;
background-position:100px;

/*배경이미지가 2장 이상이상일 경우 개별속성*/
background-position:left top, center bottom;

```

* **background-size**
    * - 배경이미지 연결 시 원본 크기가 기본으로 노출
    - 배경이미지 삽입 위치와 크기에 따른 값을 설정해야할 때 (아래) 값을 사용
        * contain : 요소 안에 배경 이미지가 전부 나타나도록 가로, 세로 크기 조정
        * cover : 배경 이미지로 요소의 크기를 모두 덮어 씌우는 형태
```

background-size:contain; /*이미지를 잘리지 않는 선에서 크게 설정*/
background-size:100%; /*이미지의 가로 너비100% 설정*/
background-size:cover; /*이미지의 가로세로비를 비교하여 빈공간이 생기지 않도록 크게 설정*/
background-size:1400px; /*강제 크기 입력(가로 세로 동시입력)*/
background-size:1400px 200px;  /*강제 크기 입력(가로 세로 개별 입력, auto 가능)*/

/*배경이미지가 2장 이상이상일 경우 개별속성*/
background-size:100%, cover;

```

* **background-attachment**
   - 스크롤 이동 시 배경 이미지가 같이 움직일 지 고정될지 설정
```

background-attachment:fixed; /*고정*/
background-attachment:scroll; /*스크롤*/

/*배경이미지가 2장 이상이상일 경우 개별속성*/
background-attachment:scroll, fixed;

```


* **배경 통합 속성 `background: color url() repeat attachment position`**
    * 색상-이미지-반복-고정-위치 순서로 작성
    * 필요에 따라 원하는 값만 골라서 작성 가능
    * 사이즈는 포지션 뒤에 ` / cover` 와 같은 사이즈 값 붙임
```

background:red url(..) repeat fixed left top;
background:url(...) scroll right bottom;
background:red center;

```


-----


## 2025-04-23 css(5)
### memo
* 모바일~태블릿까지 반응하는 반응형 웹이 아닌 pc에만 적응하는 웹을 제작하는 경우는 너비값을 pc의 표준값인 1920px에 맞춰서 피그마와 포토샵 디자인
* 디자인 후 css 진행 시 1920px를 입력하지 않고 입력하는 선택자 요소의 특징이 블록인지 인라인인지 구분
* 블록이라면 너비가 기본 100% 설정이기 때문에 pc의 w100% 채우므로 따로 너비값을 입력하지 않음 (높이 또한 마찬가지, 피그마의 hug기본값 내용에 맞추기와 뜻이 같음)
* 부모 선택자에서 상속시킨 속성이 자식, 자손에 들어있지 않을 경우 그대로 상속
* 자식, 자손에 동일한 속성이 있다면 상속 무시, 자신에게 들어있는 속성값만 인식

### **레이아웃 위치 정렬 기법**
* inline block
* float : 블록, 인라인 요소를 좌(left), 우 (right) 사용하는 위치 속성 (html4부터 존재한 속성)
    * 좌-우 배치하고 싶은 요소가 형제인 경우에 사용
    * 형제가 3개 이상인 경우 1->2 옆으로 두고 3을 내리고 싶은 경우 : 형제 3에게 `clear:both`를 선언하여 이전 형제의 float 정렬 제거
    * 형제 3개 이상인 경우 나란히 두고 싶은 경우(태그가 다를 때) : 1번에 `clear:both`
    * 오른쪽으로 보내고 싶은 형제 요소가 2개 이상인 경우
        * 2개 묶어서 그룹으로 처리하고 `float:right` 한 번만 작성
        * **`float:right`는 2번 이상 사용하면 역순이 되므로 반드시 한 번만 작성**
    * float를 적용하는 형제의 부모 높이가 max-content(기본값)이라면 -> 자식 요소에 float가 들어갈 경우 부모의 높이가 0으로 사라질 수 있음
        * 해결1 : 부모 높이(px) 입력 (디자인 높이가 고정된 경우만 주의해서 사용)
        * 해결2 : float로 인해 부유된 자식들의 영역을 재인식하는 css 속성 입력하여 오류 제거 : `overflow: hidden;`
```
/* 사각형 나열======================= */
#wrap main .ir_wrap .bg .contents {
    width: 1280px; height: 250px;
    margin: 0 auto;
    padding: 0 80px;

    /* float 오류 제거 - 하였으나 실패했으므로 높이값 설정*/
    /* overflow: hidden; */

    /* 플렉스 css - 같은 간격으로 정렬 */
    display:flex; 
    flex-wrap:wrap;
    justify-content:space-between
}

/* 레이아웃 위치 정렬 기법 */
/* inline block - float - flex - grid - position -> til 메모*/
#wrap main .ir_wrap .bg .contents a {
    /* float 정렬 - 나란히 일직선으로 정렬 */
    float: left;

    width: 260px; height: 250px;
    text-align: left;
}
```
* **flex** : 수평 수직 1차원 레이아웃으로 메인축과 교차축을 고려하여 다양한 레이아웃을 만들 수 있음
* flexible layout은 항상 container(부모)와 item(자식)으로 구분해서 이용 -> `display:flex`부모 대상에 display 명령어로 레이아웃이 flex라는 선언부터 시작
    * flex-direction : container에 적용하는 속성으로 container안의 item의 메인축 방향을 설정
        * flex-direction:row - 왼쪽->오른쪽 수평축 (기본값)
        * flex-direction:row-reverse - 오른쪽->왼쪽
        * flex-direction:column	- 위->아래 수직축 변경
        * flex-direction:column-reverse - 아래->위
    * flex-wrap : container에 적용하는 속성으로 container 내부 items 줄바꿈처리를 설정
        * flex-wrap:wrap - 기본값(자동 줄바꿈) ex) 1 2 3
        * flex-wrap:wrap-reverse - 행 기준 역방향으로 자동 줄바꿈 처리
        * flex-wrap:nowrap - 줄바꿈하지 않음(한 줄 처리) 가변너비에 따라 자동으로 % 크기 변경
    * flex-flow : container에 적용하는 속성으로 flex-direction과 flex-wrap을 묶음으로 처리
        * flex-direction:column + flex-wrap:nowrap 일 경우(아래)
        * flex-flow:column nowrap 이라고 작성 가능
    * justify-content : container에 적용하는 속성으로 메인축의 정렬방법을 설정
        * justify-content:flex-start	items의 시작점 container의 시작점으로 정렬
        * justify-content:flex-end	items의 시작점 container의 끝점으로 정렬
        * justify-content:center	items을 메인축 기준 container에서 가운데 정렬
        * justify-content:space-between	items을 container의 start, end 양끝 items을 배치하고 나머지는 고르게 정렬
        * justify-content:space-around	items을 container안에서 균등한 여백을 포함하여 정렬
    * align-content : container에 적용하는 속성으로 교차축의 아이템이 2줄 이상일 경우 정렬 방법
        * flex-wrap:wrap 적용한 상태여야 함
        * align-content:stretch	기본값(교차축 기준으로 아이템 늘리기)
        * align-content:flex-start : container의 start지점 기준 item 정렬
        * align-content:flex-end : container의 end 지점 기준 item 정렬
        * align-content:center : container의 가운데 위치 기준 item 정렬
        * align-content:space-between : container의 start, end 에 양쪽 끝 맞추고 나머지 item 균등하게 정렬
        align-content:space-around : container에서 모든 item 균등하게 정렬
    * align-items : container에 적용하는 속성으로 교차축의 아이템이 1줄 일 경우 정렬 방법
        * flex-wrap:nowrap 적용한 상태여야 함
        * align-items:stretch : (기본값) 교차축 방향 시작지점에 맞춰서 정렬(start와 거의 차이 없음)
        * align-items:flex-start : 교차축 기준 container의 시작지점에 맞춰서 정렬(왼쪽 / 위)
        * align-items:flex-end : 교차축 기준 container의 종료지점에 맞춰서 정렬(오른쪽/아래)
        * align-items:center : 교차축 기준 container의 가운데지점에 맞춰서 정렬(수직중앙, 수평중앙)
        * align-items:baseline : 교차축 기준 container의 시작지점에 맞춰서 정렬(왼쪽 / 위)
    * align-self : item에 적용하는 속성으로 container에 적용하는 align-items보다 우선순위가 높음
        * flex box의 교차축을 정렬
        * align-self:flex-start : 교차축 기준 container의 start 시작 위치(top or left)
        * align-self:flex-end : 교차축 기준 container의 end 종료 위치(bottom or right)
        * align-self:center : 교차축 기준 container의 center 중심 위치(center, middle)
        * align-self:baseline : 교차축 기준 container의 baseline 위치(내용 크기에 따라 다름(기본은 start동일))
        * grid
    * order : item에 적용하는 속성으로 아이템의 정렬 순서 설정
        * order:-1 - ex) 예시 숫자 중 가장 작은 수로 첫번째 정렬된다.
        * order:0 - ex) 예시 숫자 중 두번째 큰 수로 두번째 정렬된다.
        * order:1 - ex) 예시 숫자 중 가장 큰 수로 세번째 정렬된다.
    * flex : item에 적용하는 속성으로 증가/감소/기본의 묶음 속성
        * 주의사항) basis값은 설정 안할 시 기본값 auto가 아닌 숫자 0 으로 인식
        * flex:1 0 auto : grow(1) shrink(0) basis(auto)
        * flex:1 1 200px : grow(1) shrink(1) basis(200px)
        * flex:1 2 : grow(1) shrink(2) basis(0)
        * flex:2 100px : grow(2) shrink(x) basis(100px)
        * flex:1 : grow(1) shrink(x) basis(0) -> 가장 많이 씀
        * flex:1 auto : grow(1) shrink(x) basis(auto)
        * flex:auto : grow(x) shrink(x) basis(auto)
        * flex:100px : grow(x) shrink(x) basis(100px)
* position

### `box-shadow`
* box-shodow:x값 y값 blur값 색상 : `box-shadow: 0 0 30px rgba(0, 0, 0, 0.2);`

### 요소 사이를 같은 간격으로 정렬
```

display:flex; 
flex-wrap:wrap;
justify-content:space-between

```


 -----


## 2025-04-24 CSS(6)
### 상태 선택자 : `:hover`
* 주로 a, button, input 등에 사용하는 선택자
* 사용자가 마우스 올렸을 때 상태에 따라 스타일 적용
```

<a href="#">link</a>
<button type="button">button</button>

a:hover {background-color:yellow;}
button:hover {background-color:pink;}

```
```

#wrap main .ir_wrap .bg .contents a:hover {
    /* a에 마우스 올렸을 때 디자인 */
    background-color: #fff;
    border: 1px solid #36B4E5;
    /* box-shodow:x값 y값 blur값 색상 */
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.2);
}
```


### 속성 선택자
* html 요소 중 주로 form 관련 요소에 사용하는 선택자
* 속성 기준으로 스타일 적용
* 대괄호 안에 속성명 속성값 등 기준으로 요소 선택
    * 선택자[속성] : input[type]  속성 존재 시 선택
    - 선택자[속성=값] : input[type="text"]속성의 값이 모두 일치할 때 선택합니다.
    - 선택자[속성^=값] : input[type^="te"]속성의 값이 이것으로 시작할 때 선택합니다.
    - 선택자[속성$=값] : input[type$="xt"] 속성의 값이 이것으로 끝날 때 선택합니다.
    - 선택자[속성*=값] : input[type*="text"] 속성의 값에 이것이 포함되었을 때 선택합니다.
```
<input type="text">

input[type=text] {background-color:yellow;}
input[type^=t] {background-color:yellow;}
input[type$=xt] {background-color:yellow;}
input[type*=ex] {background-color:yellow;}

```


### 탭 형태 css
```

/* sign in 클릭했을 때 */
#wrap section .tap_title {
    margin-bottom: 50px;
    overflow: hidden;
}
#wrap section .tap_title a {
    width: 50%; /* height: 50px; */
    margin: 0 auto 0 auto;
    float: left;
    text-align: center;

    text-transform: uppercase;
    padding: 20px 0 0 0;
}

/* 비활성화 a의 자식 span */
#wrap section .tap_title a span {
    display: inline-block;
    font-weight: 300;
    font-size: ;
    padding: 5px 0;
}
/* 활성화된 a의 자식 span */
#wrap section .tap_title .active span {
    border-bottom: 2px solid #1ed760;
}

```

### form 태그 속성 : 양식에 따라 달라짐
* `valu`
    * 입력 양식일 때 - 사용자가 입력한 값 (속성 작성x)
        * 초기값을 작성하는 경우 : 쇼핑몰의 주문 수량 (기본값 1)
    * 선택 양식일 때 - 사용자가 선택해서 서버에 전송되는 값
* `name`
    * 입력 양식일 때 - 사용자가 선택해서 서버에 전송되는 값
    * 선택 양식일 때 - 1개, 또는 2개 이상의 선택 양식을 묶어주는 그룹

### form 속성에 사용자 정의값 이름 작성할 경우 주의사항
* name, value, id, class 등 속성으 ㅣ이름을 작성할 때는 **중복명칭_개별멍칭**을 섞어서 작성
* 중복명칭에서 주로 사용하는 단어 : `admin`, `user`
* 개별명칭은 요소의 특징에 따라 달라짐 (ex: `male, id, btn, pw`등)
* 중복명칭 설정 시 작성 방향도 동일하게


### 스크롤 CSS
```

#wrap section .join_law::-webkit-scrollbar {
    appearance: none; <!-- 스크롤 영역 안 보이게 -->
    width: 20px;}

#wrap section .join_law::-webkit-scrollbar-thumb {
    background-color: #e2e2e2;
    border-radius: 10px;
    background-clip: padding-box;
    border: 5px solid transparent;
    width: 10px;
}

#wrap section .join_law::-webkit-scrollbar-button{}

```

-----


## 2025-04-28 css(7)
### calc() - css 함수
* css에서 길이, 비율, 수치 등을 계산할 때 사용하는 함수
* 단위 같거나 다른 숫자 자동으로 계산 : `width:calc(350px - 59px);`
    * 셈(빼기, 곱하기, 더하기 등) 기호 앞뒤로 스페이스 있어야 함
### before , after
* **`::after`** : 요소의 자식 기준 마지막위치에 내용을 추가
```
.box li:first-child::after { 
  content:'위치 추가';
  background-color:yellow;
  display:block;
}
```
```
<ol class="box">
  <li>list
  	<!--after삽입위치-->
  </li>
  <li>list</li>
  <li>list</li>
</ol>
```
* **`::before`** : 요소의 자식 기준 시작위치에 새로운 내용을 추가
```
.box li:last-child::before { 
  content:'위치 추가';
  background-color:yellow;
  display:block;
}
<ol class="box">
  <li>list</li>
  <li>list</li>
  <li>
    <!--before삽입위치-->
    list
  </li>
</ol>
```
```
/* 가상의 형제 만들기 */
#wrap section #join_frm .member_info .birth_wrap span::after {
    content: '/';
    display: inline-block;
    font-size: 0.75rem;
}
#wrap section #join_frm .member_info .birth_wrap span:last-of-type::after {
    display: none;
}
```
* **직선 등을 가상 선택자로 만들 때는 background color를 사용해서 면으로 디자인해야 함**
```
#wrap header nav .sub_menu li:nth-child(1)::after {
    content: '<!-- 내용은 비워둠 -->';
    <!-- 크기 조절해야 하기 때문에 인라인 블록 -->
    display: inline-block;
    margin: 0 0 0 30px;
    <!-- 크기 조정과 컬러 선택 -->
    width: 1px; height: 12px;
    background-color: #000;
}
```


-----


## 2025-04-30 css(8)
### position : 위치속성
* 모든 position 관련 속성은 relative, absolute, fixed, sticky, static(기본값)중 1개를 필수로 작성하여 위치 기준 설정
*  다음 left, right, top, bottom 속성을 사용하여 원하는 위치로 대상을 이동
* **`position:relative`**
    * 원래 위치를 기준으로 움직임
    * absolute의 기준으로 부모 위치를 잡을 때도 사용
```
selector {
  position:relative;
  left:0; top:0;
}
```
* **`position:absolute`**
    * 부모 위치를 기준으로 상대적으로 위치를 움직임
    * 부모 기준은 가장 가까운 부모 기준 position 값을 인식(모든 position 가능)
        * 부모 중 별도의 position 속성이 없다면 body를 기준으로 위치 설정되므로 부모 중 원하는 기준 대상에 반드시 position 속성 작3성
```
selector {
  position:absolute;
  left:0; top:0;
}
```
* **`position:fixed`**
* 페이지 스크롤길이와 관계없이 웹브라우저 위치에 고정
* 팝업 요소에 주로 사용
* body를 기준으로 위치가 정해짐
```
selector {
  position:fixed;
  right:0; bottom:0;
}
```
* **`position:sticky`**
* 뷰포트(viewport) 기준 설정한 위치 값에 따라 끈적하게 붙은 모습을 유지
* left, right, top, bottom 방향에 따라 뷰포트의 x축과 y축으로 위치를 인식
    * sticky의 부모가 스크롤되는 뷰포트 영역에 보이는 동안  sticky가 적용
* sticky의 부모가 뷰포트 영역에서 벗어나면 sticky 기능도 종료
* webkit- CSS 접두어를 사용해야 -> https://caniuse.com/
* header의 nav요소를 상단에 붙일 경우 주로 사용
```
selector {
  position:sticky;
  top:50px;
}
```


-----


## 2025-05-07 css(9)
### **`transition`** : 스타일이 변할 때 애니메이션 효과를 부여하는 속성
* 기존 css 속성 중 어느 속성에게 효과를 부여할지, 지속시간, 속도, 딜레이 시간 등을 설정
* css 상태 선택자 (:hover), 자바스크립트 타이머 함수, 이벤트와 함께 많이 활용

* **`transition : 속성, 속성, 속성`** : 2개 이상 속성 작성 가능
* **트랜지션 속성**
* **`transition : 애니메이션적용속성 지속시간 타이밍 딜레이속도`** 
    * **transition-property** (필수, 기본값 all) : 애니메이션 적용 대상 
    * **transition-duration** (필수, 기본값 1s) : 애니메이션 지속 시간
    * **transition-timing-function** (기본값 ease) : 애니메이션 함수, 타이밍 설정
        * linear : 일정속도 움직임
        * ease (slow->fast->slow) 천천히 시작되고 중간에 빨라지고 다시 느려지면서 끝
        * ease-in : 천천히 시작
        * ease-out : 천천히 끝
        * ease-in-out : 천천히 시작되어 천천히 끝
        * cubic-bezier(n,n,n,n) 정의한 큐빅 베지어 함수에 따라 진행 (개발자도구로 간단히 설정가능)
    * **transition-delay** (기본값 0) : 애니메이션 시작 전 딜레이 시간


### **``transfrom`** : 요소에 회전, 크기, 기울기, 이동 등의 효과 부여
* 자체 애니메이션 기능을 가지고 있지 않기 때문에 즉시 변경을 원하지 않을 땐 별도의 트랜지션 속성 필요
* 모든 트랜스폼 적용 대상은 중심축 센터를 기준 위치로 사용하여 속성 적용
* 두 가지 이상 속성 값을 묶어서 작성 가능
* 속성 중 rotate+translate의 경우 속성값에 따라 애니메이션 진행 결과가 다르게 적용될 수 있음
* 속성과 속성 사이는 공백으로 구분하며 세미콜론은 마지막에만 입력
* `transform-origin:` : 기준 위치 지정 (트랜지션과 같은 선택자, 기준 선택자)
```
transform:scale(1) rotate(20deg)
transform:translate(20px, 0) rotate(30deg) scale(2)
```
* **트랜스폼 속성**
* **scale** : 요소의 크기를 X, Y축으로 확대 또는 축소합니다. (0 또는 양수 값 입력)
    * scale(n), scaleX(n), scaleY(n)
    * 별도의 단위 입력 없이 배율 기준으로 숫자를 입력
    * transform-origin 미 설정 시 center 기준으로 크기가 설정
* **rotate(deg)** : 요소를 deg 단위 값 만큼 회전(양수, 음수 값 가능)
    * transform-origin 미 설정 시 center 기준으로 설정
* **skew** : 입력한 값에 따라 기울기, 비틀기
    * skew(deg), skewX(deg), skewY(deg)
* **translate** : 요소의 위치를 X, Y 축으로 이동 (px, %, em 단위를 사용가능)
    *  translate(x, y), translateX(n), translateY(n)

-----
## 2025-05-08 css(10)
### 