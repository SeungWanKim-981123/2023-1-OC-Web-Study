# 5주차 과제 HTML 및 CSS Properties 개인 공부

1. HTML

   - HTML 기본 문법

     - HTML의 주요 추가 사항 모음.
       - 멀티미디어, 그래픽, 하드웨어 통제와 같은 추가 익스텐션 기능 없이도 구현이 가능해졌음
       - Semantic Tags : 의미론적인 태그를 프로그래머가 자율적으로 설정함으로써 가독성이 좋은 HTML 문서의 작성이 가능해졌음.
       - CSS3 : HTML 뿐만 아니라 CSS도 버전이 변화되며 이를 완벽하게 지원 가능하게 되었음.
     - HTML5의 구조
       - HTML은 doctype이 html이라고 기술된 바를 통해 정의되며 head와 body태그로 이루어진다고 할 수 있다.
       - head 태그는 일종의 브라우저 엔진이 크롤링을 할 때 도움을 주는 data들이 모여있는 요소이며, 외부 파일의 참조(css 같은 것)나 메타 데이터의 설정이 위치한다.
       - body 태그는 사람의 눈에 가시적으로 보이는 요소들이 위치한다.
     - HTML의 기본 문법

       - 요소(element)
         - 요소는 대부분의 열림 태그<>와 닫힘 태그</>로 이루어진다.
         - 태그는 딱히 대소문자의 구별은 없으나 소문자를 쓰는 것이 일반적이다.**(convention)**
         - 요소는 중첩될 수 있음, 다른 프로그래밍 언어처럼 부모 - 자식 간의 관계가 존재하는 것임.
         - content를 가질 수 없고, 속성만 가질 수 있는 특수한 태그들이 존재한다.<br/> 예시: br,hr,img,input,link,meta
       - 속성(attribute)

         - 속성은 열림 태그에 위치해야하며, 이름과 등호(=), 그리고 값(value)를 통해 구현된다.
         - global 속성 : 모든 html 요소가 공통으로 가질 수 있는 속성을 의미하며, **id class style title** 등이 이의 예시이다.

       - 주석(comment): 개발자가 html 문서 자체를 읽을 때에 도움을 주기 위해서 표기하는 내용임.

   - Semantic element & Browser Engine
     - **Semantic Web**<br/>
       오늘 날의 인터넷은 브라우저 엔진을 통해 검색된다. 우리가 만든 웹 페이지가 브라우저 엔진에 노출되지 않으면, 별다른 의미가 없고 단지 우리의 로컬
       컴퓨터 내부에 위치하는 것이라고 할 수 있다. 위에서 살펴 보았듯, HTML 문서에는 head 부분이 존재한다. meta 태그에 위치한 content들은 브라우저 엔진에 의해서 그 의미를 가진다. 이를 의미론적 요소(Semantic element)라고 한다. 이러한 방식을 통하지 않고 HTML 문서를 작성한다면, 즉 box를 작성해도 단지 div와 같은 태그를 통해 작성하면 브라우저 엔진은 이를 매우 평범한 요소로만 인식할 것이다. 하지만 HTML5에서 지원하는 header, footer,nav, section과 같은 태그를 통해 box를 표현한다면 이는 브라우저 엔진에게 있어서 매우 큰 의미로 다가올 것이고 우리의 웹사이트는 알고리즘의 수혜를 보다 더 많이 받게될 것이다!
   - 기본적(Fundamental) 태그들
     1. 문서 정의 태그 : 위에서 언급한 바와 같이 html 파일의 최상단에 위치하며 !doctype이라는 형식으로 지정한다.
     2. html 태그 : head와 body를 감싸는 태그
     3. head 태그
        - title 태그 : 문서의 제목을 명시
        - style 태그 : html 문서를 꾸밀 스타일 태그들이 위치한다. 여기에 직접 작성해도 되지만, 외부에 css 파일을 작성하고 이를 끌어와도 됨.
        - link 태그 : 외부에서 작성한 css 파일을 끌고 오는 태그이다. link 태그의 속성 값으로 rel(관계)="stylesheet"를 설정해주면 적용.
        - script 태그 : 여기에 위치한 javascript 코드는 **client-side-javscript**를 의미한다. 하지만 link와 비슷한 개념으로 src 속성을 통해서 외부에서 작성한 javascript 파일을 로드할 수 있다.
        - meta 태그 : 브라우저 엔진의 crawling에 도움을 주는 속성에 해당.</br> 메타 태그의 content 속성을 이용하면 검색엔진에게 제공할 keyword를 명시할 수 있다. </br>
          예시 : `<meta name = "keywords" content="HTML,CSS,XML,XHTML,Javascipt">`
     4. body 태그 : 대부분의 구성 요소가 본 태그에 위치. 자세한 설명은 추후 기술.
   - 텍스트(**Text**) 관련 태그
     1. **제목 태그(h1~h6)** : semantic적인 설계 구조를 고려해서 제목이 아닌 것에는 사용하지 않는 것이 바람직함.
     2. 글자 형태 태그 : b(bold체), strong(bold와 동일한 기능이지만, semantic의 관점에서 더욱 발전된 태그임),i(기울임꼴), em(i와 같은 기능을 보이지만 이 역시 semantic 구조에 있어서 더 발전된 형태), small(작은 글자로 표현해줌),del(삭제 표시),ins(inserted),sub&super(아래 & 위에 쓰인 text)
     3. 본문 태그 - p : 단락 - br : 개행 - nbsp : html에서는 공백이 얼마나 문서에 작성되던 상관 없이 1개로 취급하므로 여러개의 공백을 표현하고 싶을 때는 nbsp를 사용 - pre : 형식화된 text를 의미. 태그 내에 작성된 content 그대로를 브라우저에게 표시해준다. - hr : 수평줄 삽입 - q : 인용문을 의미. text를 큰따옴표로 감싼다.

---

2. CSS

- CSS's basic grammar
  **For what?**</br>
  HTML5 이전에는 HTML 문서 내에서 어느 정도의 스타일링이 가능했지만, 본연의 기능에 충실함을 위해 CSS로 따로 구현
  1. Selector(선택자) </br> 적용하고자 하는 HTML 요소를 선택하는 데에 사용됨. 이와 같은 selector의 집합을 style sheet라고 함.
  2. Property(속성)</br> 요소에 적용시킬 내용을 의미함. 표준 속성을 따라야 하며, 사용자가 임의로 정할 수 없음.
  3. Value(값)</br> 속성에 대응하는 값으로 **키워드**나 **단위** 또는 **색상 표현 단위**로 이루어진다.
  4. HTML과 CSS의 연동
     - Link style : link 태그에 rel 속성값을 stylesheet로 적어주고 href 속성에 파일의 상대경로를 적어주는 방식이다.</br>`<link rel="stylesheet" href="css/style.css">`
     - Embedding style : 외부의 css 파일을 끌어와서 적용시켜주는 것이 아니라, style 태그 내부에 요소들에 대한 렌더링을 정의해주는 것임.
     - Inline style : 프로그래밍에서 인라인이란, 직접 코드를 날것으로 말하면 코드를 옮겨다가 직접 박아주는 것을 말한다. 이처럼 그냥 요소의 속성값 자체를 적용해 렌더링 해주는 방법이라고 할 수 있다.
  5. Reset.css : 브라우저가 **기본으로** 적용해주는 속성값 정도로 이해하면 좋다.
- Selector : HTML의 요소를 스타일 렌더링 해주기 위해서 필요한 기법이며 comma(,)를 통해 여러개를 동시에 지정해줄 수 있다.

  - \*(asterisk) : '전체'라는 의미로 문서 내의 모든 요소를 의미한다.
  - tag selector : 태그들을 통칭해서 묶음
  - ID selector(#): 특정 ID를 가지는 요소를 선택.
  - class selector(.): 특정 class 값을 가지는 요소'들'을 선택함. 단, 클래스는 하나의 요소에 여러 개가 위치할 수 있다(활용성이 높음).
  - Attribute selector({태그명}[속성명]) : 지정된 속성을 갖는 요소를 선택.</br> **속성 셀렉터는 정규표현식을 통해 여러 방식의 활용이 가능함!**
  - **복합 selector** : {태그1}{태그2}처럼 표기되면 태그1보다 한 단계 내부에 있는 자식 태그를 가진 요소를 선택함.
    - \> : 바로 밑단 level에 있는 요소를 선택.
    - 형제 셀렉터 : +를 쓰면 바로 뒤에 오는 하나를 선택, ~를 쓰면 뒤에 오는 전부를 선택함.
  -

- Properties
- Box Models
- Font & Text
- Elements & Location
- Elements Alignment
