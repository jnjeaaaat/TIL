# 230720
## simple-diary 화면 구성
### Button누르면 페이지 이동
</br>

> import navigate
``` javascript
import {useNavigate} from "react-router-dom";
```
터미널에서 `npm install react-router-dom` 명령어로 react-router-dom 설치  
Routes, Route, useNavigate를 사용할 수 있다.
</br></br>

> Routing.jsx
``` javascript
import {BrowserRouter, Route, Routes} from "react-router-dom";

function Routing() {

    return (
        <BrowserRouter>
            <Routes>
                {/* path에 따른 Component 설정 */}
                <Route path='/' element={<Main />} />
                <Route path='/app/users/log-in' element={<SignIn />}/>
            </Routes>

        </BrowserRouter>
    )
}

export default Routing;
```
반드시 `<Routes>` 안에 `<Route>`들을 넣어줘야 한다.
</br></br>

> 버튼에 useNavigate 설정
``` javascript
import {useNavigate} from "react-router-dom";

const MainButton = () => {
    const movePage = useNavigate();

    const moveSignInPage = () => {
        movePage('/app/users/log-in');
    }
    return (
        <div className="contentWrap">
            <button className="mainButton" onClick={moveSignInPage}> 로그인 </button>
            <button className="mainButton"> 회원가입 </button>
        </div>
    )
}

export default MainButton;
```
로그인 버튼에 `onClick`으로 `moveSignInPage` 함수를 넣는다.  
`moveSignInPage`함수의 역할은 /app/users/log-in 으로 페이지 이동을 시켜주는 것  

-> Routing에서 path='/app/users/log-in' 인 컴포넌트는 SignIn.jsx
</br></br>

> 시연영상
<p align="center">
  <img src="https://github.com/jnjeaaaat/TIL/assets/47658862/2a248bd1-63e0-4f56-af2f-5c86138de715">
</p>
