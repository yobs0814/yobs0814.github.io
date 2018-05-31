---
layout: post
title: "Example Content"
author: "yobs0814"
---

# 목표: 텐서플로우를 주피터 노트북에서 실행
### 환경: Mac OS macOS High Sierra 10.13.4

결국 주피터노트북하고 파이썬3는
아나콘다로 설치함..
3.6버전을 인터넷으로 다운로드 받아서 설치함.

아나콘다 3.6 버전을 가지고
파이썬3.6 버전 설치했고, 3.5버전도 된다고 함

터미널에서
Conda install -c anaconda jupyter로 설치
참고: https://anaconda.org/anaconda/jupyter

텐서플로우 설치 ( 아나콘다 3.6 설치했다는 가정하에)
Conda create -n tensor flow python=3.6

source activate tensorflow 실행하면
프롬프트가 (tensor flow)로 변함

(tensorflow)$ condo install -c conda-forge tensorflow 실행

그럼 설치된다. 설치후

Source deactivate 실행

이제 텐서플로우를 실행하려면
source activate tensorflow 로 활성화 하면됨
이렇게 하면 환경설정까지 모두 다시 되어야해서

(tensorflow)$ condo install jupyter 실행 (기존 Jupiter notebook 지울 필요없음)

이제 주피터를 실행해서 tensorflow 사용하고싶으면 먼저 활성화 시키고
Jupyter 실행하면 된다.


주피터노트북으로 텐서플로 시작하는 방법
source activate tensorflow
Jupyter notebook


종료하는 법
주피터 파일에서 file - close and halt 클릭

터미널에서 Ctrl + c 해서 종료해야된다.
실행후
source deactivate





참고: http://pinkwink.kr/992
