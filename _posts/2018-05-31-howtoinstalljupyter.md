---
layout: post
title: "텐서플로우를 주피터 노트북에서 실행"
author: "yobs0814"
tags:
- jupyternotebook
- tensorflow
- anaconda
---

# 목표: 텐서플로우를 주피터 노트북에서 실행
### 환경: Mac OS macOS High Sierra 10.13.4

결국 주피터노트북하고 파이썬3는
아나콘다로 설치함..
3.6버전을 인터넷으로 다운로드 받아서 설치함.

아나콘다 3.6 버전을 가지고
파이썬3.6 버전 설치했고, 3.5버전이 커버된다고 사이트에 써있음..

터미널에서 아나콘다 설치
~~~
$ conda install -c anaconda jupyter
~~~

참고: https://anaconda.org/anaconda/jupyter

텐서플로우 설치 ( 아나콘다 3.6 설치했다는 가정하에)
~~~
$ conda create -n tensor flow python=3.6
~~~

텐서플로우 실행 준비
~~~
$ source activate tensorflow
~~~
프롬프트가 (tensorflow)로 변함

~~~
(tensorflow)$ condo install -c conda-forge tensorflow
~~~
그럼 설치된다. 설치후

텐서플로 환경 비활성화
~~~
$ source deactivate
~~~

이제 설치가 다 되었으니, 텐서플로우를 실행하려면 텐서플로 환경 활성
~~~
$ source activate tensorflow
~~~

주피터 노트북 설치 (기존 Jupiter notebook 제거할 필요없음)
~~~
(tensorflow)$ conda install jupyter
~~~

이제 주피터를 실행해서 tensorflow 사용하고싶으면 먼저 활성화 시키고
Jupyter 실행하면 된다.

주피터노트북으로 텐서플로 실행
~~~
$ source activate tensorflow
$ (tensorflow)$ jupyter notebook
~~~


종료하는 법
주피터 파일에서 file - close and halt 클릭

터미널에서 Ctrl + c 해서 종료해야된다.


참고: http://pinkwink.kr/992
