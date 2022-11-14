# React

## 수정
`npm star`t명령어로 파일을 만들면 `src`->`index.js`파일은 입구 파일이다.
`index.js`파일안의 명령대로 실행

## 배포
`npm run build`를 통해 실행하고 `npx serve -s 파일명`을 통해서 접근

## 컴포넌트 만들기
컴포넌트 : 사용자정의 태그라하며 대문자로 정의한다. <br>
장점 
  - 컴포넌트를 수정함으로써 모든 코드의 내용을 수정할 수있다
  - 컴포넌트를 공유하기 좋다
  - 크기를 줄일 수 있다.

예시<br>

```jsx
function Header(){
  return <header>
      <h1><a href="/">WEB</a></h1>
      </header>
}
```

## PROP
속성과 비슷한 역활을 하여 각 컴포넌트들에 특정 값을 줄 수 있다.<br>
예시

```jsx
function Header(props) {
  return (
    <header>
      <h1>
        <a href="/">{props.title}</a>
      </h1>
    </header>
  )
  
  <Header title = "React"></Header>
  ```
  
  ## 이벤트
  사용자와 상호작용을 말한다.
  예시
  ```jsx
  function Header(props) {
  return (
    <header>
      <h1>
        <a href="/" onClick={(event)=>{
          event.preventDefault();
          props.onChangeMode();
        }}>{props.title}</a>
      </h1>
    </header>
  );
  
  <Header title="React" onChangeMode={()=>{
        alert('Header');
      }}></Header>
```

## state
컴포넌트 내부에서 사용하는 값이다
`import {useState} from 'react';`를 이용하여 사용한다.


![image](https://user-images.githubusercontent.com/100742454/201532093-5d675db4-7977-4c6c-b44e-a0270f77efd4.png)
선언
```jsx
const [mode, setMode] = useState('welcome')
```
use stated의 첫번째 인자는 초기값이고 배열을 리턴한다.
0번째 인덱스는 값을 1번째 인덱스는 값을 변경하는 함수를 준다.


출처:[생활코딩](https://www.youtube.com/c/%EC%83%9D%ED%99%9C%EC%BD%94%EB%94%A91)
  
