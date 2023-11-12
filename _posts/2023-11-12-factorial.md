---
layout: post
title:  "팩토리얼을 구해보자!"
subtitle: 코딩의 시작
author: pjb8051
date:   2023-11-12 17:52:13 +0900
categories: code
tags: PJB C/C++
sidebar: []
---

세번째 시간이다

그 전에 Hello World<sup id="a1">[1](#footnote1)</sup>를 출력하고 피보나치 수열<sup id="a1">[2](#footnote1)</sup>을 구하는 코드를 공부해보았다
그래서 이번에는 팩토리얼을 구해보려고 한다.

# 팩토리얼이란?
그 수보다 작거나 같은 모든 양의 정수의 곱이다
n이 하나의 자연수일 때, 1에서 n까지의 모든 자연수의 곱을 팩토리얼이라고 한다

그럼 위에서 팩토리얼에 대해서 알아보았으니 코드를 보며 어떻게 구하는지 알아보자

```C
#include <stdio.h>
#include <stdlib.h>
int main() {

	int n;
	scanf_s("%d", &n);
	int sum = 1;

	for (int i = n; i > 0; i--)
	{
		sum *= i;
	}

	printf("%d\r\n", sum);
	
	return 0;
}
```
팩토리얼을 구하는 간단한 예제코드이다.
4!은 4x3x2x1 = 24이다
![factorial](/assets/images/factorial.png)

`4`를 입력하였을 때, `24`가 나오는 모습이 보인다!

다음번엔 뭘 공부해볼까?

# 참고
><b id="footnote1">1</b> [Hello World][Hello-World]

[Hello-World]: https://pjb8051.github.io/code/2023/11/05/Hello-World.html

><b id="footnote1">2</b> [Fibonacci][fibo]

[fibo]: https://pjb8051.github.io/code/2023/11/05/fibonacci.html