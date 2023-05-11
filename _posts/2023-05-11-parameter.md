---
layout: post
title:  "매개변수의 개수를 모르는 경우"
date:   2023-05-11 15:00
categories: Java
tags: parameter
---

<h4>매개변수의 개수를 모르는 경우</h4>
<p>메서드의 매개변수는 이미 정해져있는 것이 일반적이지만, 메서드를 선언할 때 매개변수의 개수를 알 수 없는 경우가 존재할 수 있다. </p>
<p>숫자의 합을 구하는 메서드를 선언하고자하는데 몇 개의 매개변수가 입력될지 알 수 없는 상황을 가정해보자.</p>

``` java
public class Computer {
	int sum1(int[] values) {
		int sum = 0;
		for (int i=0; i<values.length; i++) {
			sum += values[i];
		}
		return sum;
	}
	
	int sum2(int ... values) {
		int sum = 0;
		for (int i=0; i<values.length; i++) {
			sum += values[i];
		}
		return sum;
	}
}
```

1. 매개변수를 배열 타입으로 선언
	- sum1을 확인하면 배열 타입으로 선언한 것을 확인할 수 있다. 하지만, 배열로 선언하게 되면 메소드를 호출할 때마다 배열을 선언해줘야 하는 불편함이 존재한다. (Ex. System.out.println(com.sum1(new int[]{1,2,3,5,6,7})); )
2. 매개변수 입력란에 타입과 변수명 사이에 ... 를 입력하여 선언
	- ... 을활용하여 선언해주면 메소드 호출할 때 넘겨준 값의 수에 따라 자동으로 배열이 생성되고 매개값으로 사용된다. (Ex. System.out.println(com.sum2(1,2,3,5,6,7)); )
	


