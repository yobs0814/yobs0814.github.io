---
layout: post
title: "자바스크립트 콜백이란?"
author: "leaveittogod0123"
comments: true
tags:
- 자바스크립트
- callback
---

### 환경: mac OS Mojave 10.14, Webstorm

### 자바스크립트 초보자들에게 콜백이란?

### call / back

### 정리해보면 콜백함수는 제어권을 넘겨주는거에요. 누구한테요? 맡기는 대상한테

오지게 추상적인건 코드로 봐야됍니다.

```js
setInterval( function() {
    console.log('1초마다 실행됌');
},1000);

//setInterval( 함수,  ms) : 함수를 ms초 마다 호출해줘요.
// 1초마다 함수(); 이런식으로요 동작합니다.

function(){
    console.log('1초마다 실행됌');
}
// 위와 같은 익명함수를 setInterval() 이란 함수에게 전달한거죠. 그리고 setInterval() 이란 함수가 호출해줘요.toString()
// 전달된 익명함수가 콜백함수에요.콜백함수는 함수인데, 정의만 해놓고, 다른 함수의 인자로 쓰여요.
// 그럼 다른 함수가 콜백함수를 실행시켜요.
// 콜백함수는 함수다. 다만 제어권(호출)이 다른 함수에게 있다.
```

이번엔 비동기 처리를 callback으로 하는 예제를 봅시다.

비동기는 코드를 눈에 보이는대로 위에서 아래로 쭈루룩 수행하는게 아니고, 상대적으로 시간이 오래 걸리는 작업은 다른 곳에 놔둬요.
그리고 작업이 완료되면 다른곳에서 가져와서 이어서 실행해요.

동기는 코드를 눈에 보이는대로 위에서 아래로 쭈루룩 수행해요.

```html
[생활코딩fetch](https://opentutorials.org/course/3281/20562)
<!-- 생활 코딩 fetch예제-->
<!doctype html>
<html>
  <body>
    <article>
 
    </article>
    <input type="button" value="fetch" onclick="
      fetch('html').then(function(response){
        response.text().then(function(text){
          document.querySelector('article').innerHTML = text;
        })
      })
    ">
  </body>
</html>
```


then이 뭐냐 하시는 분은 간단히 말하자면.  
fetch는 인자로 url을 받아서 url에 get요청 보내는 함수에요.  

then은 요청이 오면 실행되는 함수라고 보시면 됩니다. 인자로는 요청의 결과가 들어와요.  

네트워크 요청은 간단하지 않아요. 그냥 CPU가 코드를(명령어를) 실행하는 수준이 아니죠. 

코드를 수행하는 것과는 상대적으로 시간이 많이 걸리는 일이라서 일단 요청 보내고,  

html 클릭 이벤트처럼.. 발생하면 동작하는 것처럼, 요청에 대한 응답이 오면

랜카드로 응답이 오면 랜카드가 인터럽트를 날리고 cpu가 랜카드의 데이터를 받아서 처리해요.
즉 시간이 오래 걸리죠.

잡소리를 추가하자면 네트워크는 OSI 7layer등을 타고 전달되죠? 그건 추상적으로 그렇다는 것이고,  
내부적으로는 우리가 건드릴 일이 없죠. protocol이 다 구현되어있으니... 아무튼  
![OSI7player](http://2.bp.blogspot.com/-yLCv4kSsrWw/TkUl25f7pRI/AAAAAAAAHo0/nwcnaRvFLgk/s1600/d0078067_4a666aa73c6c7.gif)

fetch('url').then( 이 부분을 보시면 )
함수가 정의되었어요. 함수의 제어권을 then()이란 메서드에 전달한거죠?

혹시나 콜백함수에서 this를 쓰고싶으면 '자바스크립트 this 바인딩' 검색을 해보세요.  
[poiemaweb](https://poiemaweb.com/js-this) 이 사이트에 나온 내용들을 찾아보시면 됩니다.  
일단은 자바스크립트에서 함수내부에서 this는 전역객체입니다.  

## 결론: 콜백함수는 함수이다! 다른 함수의 인자로 전달되고 다른 함수가 실행합니다!

