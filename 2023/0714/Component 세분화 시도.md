# 230714
## simple-diary 화면 구성
### Component 세분화
</br>

> 기존 Main.jsx 코드
``` javascript
function Main() {
    return (
        <div className="page">
            <div className="simpleDiary">
                Simple Diary
            </div>

            <div className="contentWrap">
                <button className="mainButton"> 로그인 </button>
                <button className="mainButton"> 회원가입 </button>
            </div>
        </div>
    )
}
```

로그인, 회원가입 버튼을 누르면 메인 타이틀인 `SimpleDiary`를 제외한 아래 부분만 바뀌도록 하기 위해 **세분화** 필요
</br>

> Page.jsx 
``` javascript
const Page = (props) => {
    return (
        <div className="page">
            {props.title}
            {props.button}
        </div>
    )
}
```
</br>

> Title.jsx
``` javascript
const Title = () => {
    return (
        <div className="simpleDiary">
            Simple Diary
        </div>
    )
}
```
</br>

> MainButton.jsx
``` javascript
const MainButton = () => {
    return (
        <div className="contentWrap">
            <button className="mainButton"> 로그인 </button>
            <button className="mainButton"> 로그인 </button>
        </div>
    )
}
```
</br>

> 최종 Main.jsx
``` javascript
function Main() {
    return (
        <Page title={<Title />} button={<MainButton />} />
    )
}
```
props에 title, button에 Component를 넣어서 전달