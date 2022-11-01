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

### 결합자
