# css

## css란
- Cascading Style Sheets

### 구조
- 선택자(태그)와 속성명 속성값으로 이루어짐
-  선택자{속성명:속성값}

### 적용법
- 인라인 스타일 - Inline Style Sheet
  - 태그안에 style을 적용
  - ' ; '을 이용하여 여러 style 적용가능
  - 현업에서는 잘 사용하지 않음
- 인터널 스타일 - Internal Style Sheet
  - head태그안에 style태그를 사용하여 style규칙을 선언한다. 
  - 현업에서는 잘 사용하지 않음
- 외부 스타일 - External Style Sheet
  - 외부에 css파일을 생성한다.
  - style태그없이 style 바로 규칙을 정한다.
  - head태그 안에 링크태그 선언 ex(link rel="stylesheet" href="./style.css")

## 선택자

### 기본선택자
- 전체 선택자 (*)
  - 브라우저 가지고 있는 기본 style을 초기화 할 떄 사용
- Type 선택자 (타입이름)
  - 태그의 style 설정
- Class 선택자 (.)
  - class의 style을 설정 (class명에 스타일형식을 암시하게 만드는게 좋다)
- ID 선택자ㅍ(#)
  - id의 style을 설정
  - id는 고유해야 한다. 
- 속성 선택자(태그[속성], [속성])
  - 태그에 속성이 있으면 style적용
  - 사용방법
    - 속성이 존재하는 요소
      - h2[class] { ~ }
      - [target] { ~ }
    - 속성 값과 일치하는 요소
      - h2[class = ' 속성값 ' ] { ~ }
    - 속성 값을 포함하는 요소
      - a[href *= ' 속성값 ' ] { ~} 
    - 속성 값으로 시작하는 요소
      - h2[class^=' 속성값 ']{} 
    - 속성 값으로 끝나는 요소
      - a[href$=" 속성값 "]{}
    - 속성에 단어를 포함하는 요소 
      - h2[class~=' 단어 '] {}
  
### 그룹선택자
선택자를 쉼표(,)로 구분해 여러 선택자를 나열함.

같은 스타일을 여러 선택자에 한꺼번에 정의할 수 있다.

## 결합자
### 자손 결합자
자손 (공백) 결합자는 첫 번째 요소의 자손인 태그를 선택합니다.

- 문법
    
    `A B` A선택자의 하위에 있는 B선택자를 모두 선택함.   

### 자식 결합자
자식`>` 결합자는 첫 번째 요소의 바로 아래 자식인 태그를 선택합니다.

- 문법
    
    `A > B`
    
### 일반 형제 결합자
일반 형제`~` 결합자는 형제, 즉 첫 번째 요소를 **뒤따르면서** 같은 부모를 공유하는 두 번째 요소를 선택합니다.

- 문법
    
    `A ~ B`

### 인접 형제 결합자
인접 형제`+` 결합자는 형제, 즉 첫 번째 요소의 **바로 뒤에** 위치하면서 같은 부모를 공유하는 두 번째 요소를 선택합니다.

- 문법
    
    `A + B`

## 글꼴

### 글꼴 관련 속성 
- `font-family` - 글꼴 종류를 지정합니다.
    
    기본값 : 웹브라우저 기본 글꼴
    
- `font-size` - 글자 크기를 지정합니다.
- `font-style` - 글자를 이텔릭체로 표시할지 지정합니다.
- `font-weight` - 글자 굵기를 지정합니다.
- `font-variant` - 소문자를 작은 대문자로 바꾸는 속성

### 웹 폰트
사용자의 컴퓨터에 설치된 폰트와 상관 없이 **온라인의 특정 서버에 위치한 폰트 파일**을 다운로드하여 화면에 표시해주는 **웹 전용 폰트**입니다.
구글 웹 폰트 사이트에 방문하여 `<link>` 또는 `@import` 문을 사용하여 웹 폰트를 적용할 수 있다.

### 단위 em, rem
- `px` : 픽셀 단위
- `rem` : 루트 요소의 글꼴 크기
- `em` : 요소의 글꼴 크기
- `vw` : viewport 너비의 1%
- `vh` : viewport 높이의 1%

## 글자 색상
글자 색상은 `color` 속성으로 지정하며 색상 값으로는 `16진수 값` `rgb 값` `hsl 값` `색상 이름`이 사용된다.
### `RGB/RGBA` 표기법
RGB 색상 모델은 빨강, 초록, 파랑을 통해 특정 색을 표현합니다. **선택사항으로 색의 투명도**를 알파 채널로 표현할 수 있습니다. 함수형 표기법(`rgb()`, `rgba()`)으로 표현할 수 있습니다.
- 예시
    rgb(0,0,0), rgba(0,0,0,0)
    
### `16진수` 표기법
RGB 색상 모델은 빨강, 초록, 파랑을 통해 특정 색을 표현합니다. 선택사항으로 색의 투명도를 알파 채널로 표현할 수 있습니다. # 뒤의 16진수 표기법으로 표현할 수 있습니다.
- 예시
    #ff0000, #ff00ff, #808000 등 16진수
    
## 그 외 글자 관련 속성
- `text-align` 
    블록 요소(block element), 테이블 셀 박스(table-cell box)안에서 글자를 가로 정렬 하는 데 사용합니다.
    값 으로는 `left`, `right`, `center`키워드가 올 수 있습니다.
- `line-height`
    줄 간격을 설정합니다.
- `letter-spacing`
       글자 사이의 간격
## Box Model
모든 HTML 요소는 웹 페이지에서 일정 공간을 차지하게 됩니다. 그리고 이러한 공간을 CSS에서는 박스 모델(Box Model)로 정의하고 있습니다.

HTML 요소의 박스 모델은 Content, Padding, Border, Margin으로 구성되어 있습니다.
 ![image](https://user-images.githubusercontent.com/100742454/199740700-3fa0e642-099a-4cd5-8be3-f8fbd70ab59a.png)
 
 ### Content
- `width` - Content 영역은 `width` 값을 이용하여 가로 너비를 지정할 수 있습니다.
- `height` - Content 영역은 `height` 값을 이용하여 세로 너비를 지정할 수 있습니다.

### Padding
- `padding` - `padding` 값을 조절하여 안쪽 여백을 지정할 수 있습니다.
- `padding-{direction}` - `padding-top` `padding-left` `padding-right` `padding-bottom` 속성을 사용하여 각각 지정할 수도 있습니다.
    
### Border
- `border` - `border` 속성을 사용하여 테두리를 설정할 수 있습니다.

### Margin
- `margin` - `margin` 속성을 사용하여 바깥쪽 여백을 지정할 수 있습니다.
- `margin-{direction}` -  `margin-top` `margin-left` `margin-right` `margin-bottom` 속성을 사용하여 각각 지정할 수도 있습니다.

### Box Sizing
Box Sizing 속성은 HTML요소의 너비와 높이를 **계산하는 방법**을 지정합니다.
CSS 박스 모델에서 지정한 너비(width)와 높이(height)는 HTML 요소의 Content크기에 적용됩니다. 요소에 테두리(Border)나 안쪽 여백(Padding)이 있으면 너비와 높이에 더해서 화면에 그립니다. 따라서 크기를 설정할 때 원하는 크기를 얻으려면 테두리나 안쪽 여백을 고려해야 합니다.
이때 `box-sizing` 속성을 사용해 이 방식을 변경할 수 있습니다.
- `box-sizing` 값
    - `content-box` - 기본 CSS 박스 크기 결정법 입니다. 요소의 너비를 100px로 설정하면 콘텐츠 영역이 100px 너비를 가지고, 테두리와 안쪽 여백은 이에 더해집니다.
    - `border-box` - 테두리와 안쪽 여백도 요소의 크기(width, height)로 고려합니다. 너비를 100px로 설정하고 테두리와 안쪽 여백을 추가하면, 콘텐츠 영역이 줄어들어 총 너비 100px을 유지합니다. 대부분의 경우 이 편이 크기를 조절할 때 쉽습니다.
  
  ### 테두리 Border

CSS `border` `border-width` `border-style` `border-color` 속성으로 요소의 테두리를 설정합니다.

- `border-style`
    - 어떤 형태의 테두리 스타일을 지정할지 나타냅니다.
    - 4개 방향의 값을 한꺼번에 지정할 때는 방향 순서를 지켜야 합니다. top → right → bottom → left
    - 테두리 스타일 종류 [MDN](https://developer.mozilla.org/ko/docs/Web/CSS/border-style)

- `border-width`
    - 테두리 두께를 지정합니다.
    - 값으로 `<크기>` 또는 키워드 `thin` `medium` `thick` 가 올 수 있습니다.

- `border-color`
    - 테두리 색상을 지정합니다.

- `border`
    - 단축 속성으로서 다음의 하위 속성을 포함합니다. `border-width` `border-style` `border-color`
    - 즉, 테두리 두께, 스타일, 색상을 한꺼번에 표기할 수 있습니다.
    - `border-top` `border-right` `border-left` `border-bottom` 을 사용하여 스타일을 각각 지정할 수 있습니다.

- `border-radius`
    - 테두리 꼭짓점을 둥글게 만듭니다.

### 바깥 여백 Margin
- `margin` 속성은 HTML 요소의 바깥 여백을 지정합니다.
- `margin-top` `margin-bottom` `margin-left` `margin-right` 속성을 사용하여 각각 지정할 수도 있습니다.
   
### 마진 중첩
HTML 요소를 세로로 배치할 경우 `margin`과 `margin`이 만날 때 `margin` 값이 큰 쪽으로 겹쳐지는 것. 요소를 가로로 배치할 경우에는 상관없지만 세로로 배치할 경우에는 값이 큰 `margin`만 적용 된다.

### 안쪽 여백 Padding
- `padding` 속성은 HTML 요소의 안쪽 여백을 지정합니다.
- `padding-top` `padding-bottom` `padding-left` `padding-right` 속성을 사용하여 각각 지정할 수도 있습니다.

## display 속성
`display` 속성은 HTML 요소를 어떻게 표시할지를 결정합니다.
HTML 요소마다 기본적으로 갖고 있는 display 속성 값이 다른데요.
이 기본값이 `display: block` 이면 Block Level Element 이며, `display: inline` 일 경우 Inline Level Element 입니다.
그리고 display 속성은 주로 4가지 속성 값이 쓰입니다.

### `none`
요소를 보이지 않게 설정합니다. `visibility` 속성을 `hidden`으로 설정한 것과 달리, 영역도 차지하지 않습니다.

### `block`
기본적으로 가로 영역을 모두 채우며, block 요소 다음에 등장하는 태그는 줄바꿈이 된 것처럼 보입니다. 문서에서 문단을 표시할 때 주로 사용합니다.
`width`, `height` 속성을 지정 할 수 있습니다.
`div` `p`  `h1~h6` 태그 등이 이에 해당됩니다.

### `inline`
컨텐츠만큼 영역을 차지합니다. 
block 과 달리 줄 바꿈이 되지 않고, `width`와 `height`를 지정 할 수 없습니다.
word 같은 문서에서 볼드, 이탤릭, 색상, 밑줄 등 글자나 문장에 효과를 주기 위해 존재하는 단위라고 할 수 있습니다.

### `inline-block`
block과 inline의 중간 형태로 요소는 inline인데 내부는 block처럼 표시함
inline 처럼 컨텐츠 만큼 영역을 차지하여 가로로 배치되지만
block 처럼 내부 속성인 width, height 등과 같은 값을 변경할 수 있습니다. 

# CSS Float

### float 속성
`float` 의 사전적인 의미는 '뜨다"라는 뜻입니다.
만약 HTML 요소에 float이 적용되면 HTML 요소는 원래의 흐름에서 벗어나 둥둥 떠다니듯 배치가 됩니다.
그리하여 인접한 텍스트 또는 인라인 요소가 그 주위를 자연스럽게 감싸게 합니다. 
자주 사용하는 `float` 속성 값은
- `none` - 기본값으로 요소를 띄우지 않음
- `left` - 왼쪽에 띄움
- `right` - 오른쪽에 띄움
- `inherit` - 부모 요소로부터 상속함
- `initial` - 기본값으로 설정함
-
### clear 속성
clear는 취소하다 라는 뜻으로 `float: left;` 혹은 `float: right;` 값을 취소합니다.
- `clear: none;` - 기봇값
- `clear: left;` - 왼쪽을 취소
- `clear: right;` - 오른쪽을 취소
- `clear: both;` - 왼쪽 오른쪽 둘다 취소

# CSS Position

## position 속성
`position` 속성은 HTML 요소를 배치하는 방법을 지정합니다.
- `static` (기본값)
    static은 요소가 HTML 문서에서 일반적인 흐름을 따라 배치가 되게하며, 기본값이다.
- `relative`
    `static`과 마찬가지로 요소가 문서의 일반적인 흐름에 따라 배치되게 합니다. static과 차이점은 요소가 자신의 `static` 위치에서 `top` `right` `bottom` `left`와 같은 속성에 의한 상대적인 위치에 배치된다는 점입니다.
- `absolute`
    `absolute`는 요소가 문서의 일반적인 흐름을 따르지 않게한다. `absolute`는 **position: static 속성을 가지고 있지 않은 부모를 기준**으로 움직입니다. 만약 부모 중에 포지션이 relative, absolute, fixed인 태그가 없다면 가장 위의 태그(body)가 기준이 됩니다.
- `fixed`
    `fixed` 역시 `absolute`와 마찬가지로 요소가 문서의 일반적인 흐름에서 제거됩니다. 대신, 스크린의 뷰포트(viewport)를 기준으로 한 위치에 배치됩니다. 즉, 스크롤되어도 움직이지 않는 고정된 자리를 갖게 됩니다.
- `sticky`
    `sticky`는 요소가 HTML 문서안에서 `static`과 같이 일반적인 흐름에 따라가다가 스크롤 위치가 임계점에 이르면 `fixed`와 같이 박스를 화면에 고정할 수 있는 속성입니다.
    - top속성을 적용해야 스크롤 임계점에서 고정이됨.
    - left, right, bottom 속성을 사용할 수 없음.
    - 
### 위치 속성
position 속성이 배치하는 방법이라면 top left bottom right 속성은 요소를 원하는 곳으로 최종적으로 위치 시키는 속성이다. 이 속성은 `position: static;` 에서는 적용되지 않는다.
- `top`
- `left`
- `bottom`
- `right`


출처:[짐코딩 HTML&CSS](https://gymcoding.notion.site/HTML-CSS-706749085a29449bb066957e56686365)
