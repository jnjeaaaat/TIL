# 230711
## simple-diary 화면 구성
### CSS Button 부드러운 마우스 오버 효과 만들기
</br>

> react 파일

``` react
{/*button 생성*/}

<button className="mainButton"> 로그인 </button>
<button className="mainButton"> 회원가입 </button>
```
</br>

> css 파일

``` css
.mainButton {
  ...
  /*개인 설정*/
  ...
  transition: all 0.4s; /* transition으로 부드러운 효과 */
}
```
</br>

> focus, hover

``` css
.mainButton:focus {
  /* border-radius 설정을 했을 때 테두리를 벗어나 버튼표시 되는것을 방지 */
  outline: none; 
}
```

``` css
/* hover는 마우스를 올렸을 때 변화 */
.mainButton:hover {
  background: white;
  color: pink;
}
```
</br>

> 시연영상
<p align="center">
  <img src="https://github.com/youjyeon/ourFuture/assets/47658862/1472212b-a000-4e63-b771-4489d487fd6a">
</p>

