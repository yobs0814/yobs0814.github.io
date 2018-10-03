---
layout: post
title: " 분할정복 알고리즘 :: 가장 가까운 두 점 찾기 문제"
author: "yobs0814"
tags:
- 분할정복
- 알고리즘
---

# 목표: 분할정복 알고리즘을 적용하여 가장 가까운 두 점 찾기 문제 해결하기
## 환경: mac OS High Sierra 10.13.4

가장 가까운 두 점을 찾는 간단한 방법은 '모든 경우를 다 점검해 보는 것'입니다. 즉, 모든 점 사이의 거리를 구해보는 것입니다. 
만약 점의 개수가 n개라면 O(nC2) = O(n(n-1)/2) = O((n^2-n)/2) = O(n^2)
시간복잡도 n^2을 보면 성능이 나쁘지 않다고 볼 수 있습니다. 하지만, 분할 정복 알고리즘을 사용하면 이보다 더 빨리 '가장 가까운 두 점'을 찾을 수 있습니다.

//분할 정복 알고리즘의 의사코드
//points 점들의 배열(단, x 좌표로 오름차순 정렬되어있음)
~~~
closetPairRecursive(points){
	if( 점들의 개수 <= 3){
		result <- 모든 경우에 대해 최소 거리를 계산
	}

	가운데 점을 기준으로 points를 points_L과 points_R로 분할

	dL = closestPairRecursive( points_L)
	dR = closestPairRecursive( points_R)
	dC = 중간 영역의 점들에서 가장 가까운 거리 구하기

	result = min(dL, dR, dC)

	return result
}
~~~