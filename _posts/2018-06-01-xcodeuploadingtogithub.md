---
layout: post
title: "ios xcode에서 github에 소스 올리기"
author: "yobs0814"
---

목표: xcode로 github소스올리기
버전 : xcode 9.3.1

xcode new project를 만드는 과정에서 경로지정하는 탭에서


![img1](./img/2018-06-02-1.39.55.png)
이 부분을 체크합니다.

새 폴더를 만들면 활성화 됩니다.



깃헙 리파지토리 만들기

왼쪽에 보이는 네이게이션 영역에서

네비게이션 영역의 source control navigator에서 해당 프로젝트 우측클릭
![img2](./img/2018-06-02-1.40.10.png)

create <프로젝트이름> remote on github...

그러면 깃헙 계정에 리파지토리 만들어집니다.

깃헙 계정 설정은

![img3](./img/2018-06-02-1-40-19.png)


Preferences..  클릭후 Account탭에서 github 계정 넣고, Clone using HTTP...

ssh key는 자동으로 만들어주는 버튼을 클릭합니다.



나머지는 다른 IDE와 비슷한 방식이므로 생략합니다.



참조: https://www.youtube.com/watch?v=cVBECn2j-iQ
