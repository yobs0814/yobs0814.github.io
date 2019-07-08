---
layout: post
title: "xCode에서 여러개의 main 메서드를 사용하기"
author: "leaveittogod0123"
tags:
- Xcode9
- c
---

# 목표: xCode에서 여러개의 main 메서드를 사용하기
### 환경: mac OS High Sierra 10.13.4, Xcode9.4

File -> New -> Target... 그리고 macOS탭에서 Application -> Command Line Tool
next -> Product name 입력후 -> finish

![img1](https://i.stack.imgur.com/O3SQ1.png)

실행할때는 navigator 위에있는 target scheme만 바꿔주면 된다.

![img1](https://i.stack.imgur.com/fEds5.png)

원래는 여러개의 타겟 접근은 앱에서 여러 코드를 공유할때 쓰이지만, 이런 상황에서도 사용된다.

다른 방법이 한개 더 있는데 참조한 사이트에 있음.

![img1](https://i.stack.imgur.com/Ilkhq.png)

[참조](https://stackoverflow.com/questions/40006218/xcode-multiple-main-methods).

---

그러면 target은 뭔가?

- workspace는 한개 또는 그 이상의 프로젝트를 가진다. 보통 이 프로젝트는 연관이 있음.
- project는 코드와 리소스 등등을 가진다.
- target은 각 프로젝트는 한개 이상의 targets을 갖는다.
  - 각각의 target은 프로젝트에 대한 빌드 세팅을 정의한다.
  - 각각의 target은 클래스들과 리소스들 그리고 사용자 정의 스크립트 등 빌드에 필요한 것들을 정의한다.
  - 여러개의 targets은 같은 프로젝트에서 다른 버전의 배포를 할때 사용된다.
    - 예를 들어, my project에 두개의 targets을 갖고 있다. 그리고  "normal"빌드와 "office"빌드는 각각 다른 기능을 추가하여 테스트해야하는데, targets를 바꿈으로써 손쉽게 테스트를 할 수 있음.
- scheme은 빌드, 테스트, 프로파일을 누를 때 일어난다.
  - 보통 target하나당 적어도 하나의 scheme을 갖는다.

target은 다른 내용을 더 봐야 이해가 될듯..
[참조](https://stackoverflow.com/questions/20637435/xcode-what-is-a-target-and-scheme-in-plain-language).
