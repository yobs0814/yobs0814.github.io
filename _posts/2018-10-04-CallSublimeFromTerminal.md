---
layout: post
title: "Sublime Text 서브라임 텍스트를 터미널에서 실행하기"
author: "leaveittogod0123"
tags:
- SublimeText
- Terminal
---

# 목표: sublime 을 터미널에서 실행하기
### 환경: mac OS High Sierra 10.13.4, Submlime text3

[참조](https://beomi.github.io/2017/07/04/Call-Sublime-from-Terminal/)
위 블로그에 정말 자세히 나와있는데, 따라해도 잘 안되서 구글링을 더 해본결과

### sublime Text 설치 확인
터미널을 키고 아래 명령어를 입력해서 설치 확인해봅니다.
~~~
# SublimeText3 의 경우
open /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl
~~~

서브라임 텍스트 프로그램이 실행된다면

다시 터미널에 아래 코드를 입력해줍니다.

[code]
~~~
rm /usr/local/bin/subl;
sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl;
~~~
