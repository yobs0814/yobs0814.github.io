---
layout: post
title: "swift4, xcode9 에서 외부라이브러리 연동하기"
author: yobs0814
tags:
- Xcode9
- FSCalendar
---

# 목표: xcode9에 FSCalendar 연동하기
### 환경: mac OS High Sierra 10.13.4, Xcode9.4

[추가하려는 외부라이브러리](https://github.com/WenchaoD/FSCalendar)
[cocoapods사용법](http://zeddios.tistory.com/25)

cocoapods 사용법에 대해서는 위의 참조에 너무 친절하게 나와있음.
외부 라이브러리를 관리하는 프로그램인데요. 맥은 루비가 기본으로 설치되어있기 때문에
루비를 이용해 설치하고 사용합니다.

다만 문제가 있었는데 추가하려는 외부라이브러리 'FSCalendar' Readme에 나온대로 읽고 그대로 따라했는데

## 문제: no such module 'FSCalender'

역시나 그냥 되는건 없죠. 이 문제가 발생했지요. 구글링을 다해봐도 저한테 해당되는 방법이 아니었는데,
xcode 초보라 몰랐던 내용인것 같은데,

##해결: xcode 메뉴바 -> Product -> Scheme -> FSCalendar -> Run(command + R)

문제해결됐네요.
