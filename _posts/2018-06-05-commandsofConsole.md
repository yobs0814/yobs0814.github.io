---
layout: post
title: " 자주 사용하는 콘솔 명령어 정리"
author: "yobs0814"
tags:
- mac
- console
---

# 목표: 콘솔을 이용해보자
## 환경: mac OS High Sierra 10.13.4

각 OS에서 터미널을 실행한다.
터미널이 실행된 화면을 보면
YOSEPHui-MacBook-Pro:firstProject yosephnoh$ 라는 글자는 프롬프트 라고 부른다.
사용자로부터 명령을 입력 받는 역할을 담당한다. 프롬프트에 적혀있는 단어들의 의미는 다음과 같다.

~~~
사용자ID@컴퓨터명:현재디렉토리$
~~~

현재 디렉토리명에 물결(~)표시가 있는데 이는 관례적으로 리눅스에서 사용자의 홈 디렉토리를 나타낸다.
마지막으로 $표시도 의미가 있다. $는 현재 사용하고 있는 계정의 권한이 일반 사용자임을 나타낸다. 일반 사용자 외에 최고 권한
사용자도 있는데 이를 root라고 부른다. root계정을 사용하면 #표시로 바뀌게 된다. 사용자 권한에 관한 이야기는 추후에
검색을 통해 살펴보도록하자.


terminal 을 종료하는 방법은
~~~
$ exit
~~~
특수기호 ($) 뒤쪽에 있는 글자만 키보드로 입력하면 된다.

지금까지 콘솔창을 사용하기 위한 기본 설명을 진행했다.

파일이동
<center>명령어</center>|<center>설명</center>|<center>예제</center>
:---|:---:|---:
**pwd** | <center>디렉토리 이동</center> | /Users/사용자명/Documents/IOSLab/firstProject
**cd ..** | <center>현재 디렉토리의 상위 디렉토리로 이동</center> | /Users/사용자명/Downloads/IOSLab
**cd ~** | <center>사용자의 홈 디렉토리로 이동 </center> | /Users/사용자명
