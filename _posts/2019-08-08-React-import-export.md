---
layout: post
title: "ECMASciprt 2015에서 정의된 import 사용법 및 정리"
author: "leaveittogod0123"
comments: true
tags:
- React
- ES2015
---

### 환경: mac OS Mojave 10.14, Webstorm

# ECMASciprt 2015에서 정의된 import 사용법 및 정리

## import와 export

js로 프로그래밍을 하다보면 js코드를 재사용하기, 코드 고치는 부분 적게 만들려고 등등 장점 때문에

js파일을 나눠서 프로그래밍을 합니다. 그러면 다른 js파일에서 코드를 가져다 쓸 일이 많은데 그때 사용하는게

이런 방법으로 프로그래밍을 하는 것을 전문용어로 module이라고 하죠. 

이러한 module기법을 쓸때 사용하는 키워드 export, import는 ECMAScript 2015에서 새로 정의한 구문입니다.

사용법은 다음과 같습니다.

```javascript
A.js 
function a(){
    
}
export const a; // 이 대상이 클래스가 될 수도, 객체가 될 수도, 변수가 될 수도 있겠죠.

///

B.js

import {a} from './B.js'

a();

```

다른파일에서 A.js 파일에 a함수를 사용할 수 있게 export를 하고
import {a} from '가져올파일 경로';

export 하는 방법이 크게 두 가지로 나뉩니다.

이름을 정해서 보내기

그냥 보내기

```javascript
// my-module.js
function cube(x) {
  return x * x * x;
}
const foo = Math.PI + Math.SQRT2;
var graph = {
    options: {
        color:'white',
        thickness:'2px'
    },
    draw: function() {
        console.log('From graph draw function');
    }
}
export { cube, foo, graph };
```
이렇게 내보낼 이름을 적어서 export하면
import 하는쪽에서도 똑같이 받아야되요.
{ 변수 } <- Destructuring Assignment라 하는데 이 또한 ECMAScript에서 나왔습니다.
```javascript
// other.js
import { cube, foo, graph } from 'my-module';
graph.options = {
    color:'blue',
    thickness:'3px'
}; 
graph.draw(); // my-module.js 에 있는 함수, 값, 객체를 쓸 수 있어요.
console.log(cube(3)); // 27
console.log(foo);    // 4.555806215962888
```

또 다른 방법인 그냥 내보내기
```javascript
// my-module.js
export default function cube(x) {
  return x * x * x;
}
```
단, export default는 한번만 쓸 수 있습니다.

```javascript
// other.js
import cube from './my-module.js';
console.log(cube(3)); // 27
```

기존 NodeJs에서 제공하는 CommnoJS와 동일한 목적을 가진 구문입니다.
ES2015에서 정의된 import export가 React에서는 CommnoJS인 require와 export.module과
혼용이 됩니다. babel이 import 문을 require로 바꿔주기 때문인데요.
엄밀히 말하면 ES2015 module과 CommonJS는 다릅니다.

어떻게 다른지는 이후에 post 예정입니다.