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

예시

```jsx
function Header(props) {
  console.log(props);
  return (
    <header>
      <h1>
        <a href="/">{props.title}</a>
      </h1>
    </header>
  )
  
  <Header title = "React"></Header>
  ```
