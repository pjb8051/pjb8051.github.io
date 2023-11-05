---
layout: post
title:  "피보나치 수열"
subtitle: 코딩의 시작
author: pjb8051
date:   2023-11-05 15:15:13 +0900
categories: code
tags: PJB C/C++
sidebar: []
---

저번 시간에는 코딩 첫 시작의 국룰인 Hello World<sup id="a1">[1](#footnote1)</sup>를 출력하였다. 오늘은 내가 대학 강의에서 Hello World 다음으로 배웠던 피보나치 수열을 구하는 코드를 알아보자

먼저 피보나치 수열에 대해서 알아보자
```
피보나치 수열은 첫째항과 둘째항이 0과 1로 고정이고 그 뒤의 모든 항은 바로 앞 두 항의 합인 수열이다.
예를 들어, 0, 1, 1, 2, 3, 5 ''' 이런 식으로 증가하는 수열이다
```
식으로 나타내면
<br>
![](/assets/images/fibo.png)
<br>

피보나치 수열을 알아보았으니 코드를 짜서 콘솔 창에서 제대로 구현이 되는지 알아보겟다

```C
#include <stdio.h>
#include <stdlib.h>

int main() {

	int n;

	scanf_s("%d", &n);
	
	int arr[101] = { 0 };
	int len = sizeof(arr) / sizeof(arr[0]);

	arr[0] = 0;
	arr[1] = 1;

	for (int i = 2; i < len; i++)
	{
		arr[i] = arr[i - 2] + arr[i - 1];
		
	}

	printf("%d\r\n", arr[n]);
	
	return 0;
}
```
위 코드는 입력을 100까지로 제한하는 코드이다.
만약, 10을 입력하면 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55으로
`55`가 출력되어야 한다

결과를 보자
<br>
![](/assets/images/fibo-result.png)

`55`가 잘 검출된다!

다음에는 뭘 공부할지 고민하고 포스팅해야겠다

# 참고
><b id="footnote1">1</b> [Hello World][Hello-World]

[Hello-World]: https://pjb8051.github.io/code/2023/11/05/Hello-World.html