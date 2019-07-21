---
layout: post
title: " Mac에서 jekyll serve 실행시 오류 해결"
author: "leaveittogod0123"
comments: true
tags:
- jekyll
---

### 환경: mac OS Mojave 10.14, CLion

#### 문제 발생
지킬블로그를 로컬에서 실행하기 위해서  

구글링을 통해 지킬 블로그 디렉토리에서 터미널로 jekyll serve 라는 명령어를 통해 로컬 실행이 가능하다는 것을 알게 되었다.

jekyll serve 실행시  

jekyll serve error because extensions are not built 불라불라하는 에러가 발생했다.

[구글링을 통해 찾은 이슈 해결법](https://github.com/jekyll/jekyll/issues/7317) 그런데 해결이 안됐다.

일단 bundle update도 되지 않았다. stackoverflow등 검색결과

[Cannot install Jekyll on MacOS Mojave #7274](https://github.com/jekyll/jekyll/issues/7274) 에서 본 것 처럼

xcode-select --install 도 안됐다. 혹시 몰라 xcode도 업데이트했다.

그래도 해결이 안됐다.

ruby 업데이트해야된다라는 결론을 지음.


구글에서 루비 업데이트로 검색하면 [루비 사이트](https://www.ruby-lang.org/ko/documentation/installation/)가 나온다.

근데 하라는데로 해도 되질 않았다.

#### 문제해결

ruby mojave 키워드로 검색하니 [새로운 ruby 사이트](https://gorails.com/setup/osx/10.14-mojave)가 있었다.

사이트에 나온대로  

installing homebrew, installing Ruby를 따라서 했음.

일단 루비가 2.3.8 -> 2.6.3 으로 업데이트 되었다.

이제 다시 

$bundle update

$gem install jekyll

$bundle exec jekyll serve를 하면

크롬으로 localhost:4000 접속하면 로컬에서 지키블로그가 올라간것을 볼 수 있음.