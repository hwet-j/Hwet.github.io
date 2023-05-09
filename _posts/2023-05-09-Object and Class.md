---
layout: post
title:  "객체, 클래스, 인스턴스"
date:   2023-05-09 03:30:13 +0800
categories: Java
tags: Object Class 
comments: 1
---
### 클래스 <br>
○ 개념
	- 객체를 만들어 내가 위한 설계도 혹은 틀
	- 연관되어 있는 변수와 메서드의 집합
### 객체
○ 개념
	- 소프트웨어 세계에 구현할 대상
	- 클래스에 선언된 모양 그대로 생성된 실체
○ 특징
	-'클래스의 인스턴스'라고도 부른다.
	-객체는 모든 인스턴스를 대표하는 포괄적인 의미를 갖는다.
	- oop관점에서 클래스의 타입으로 선언되었을 때 '객체'라고 부른다.

<pre>
<code>
class OverloadingExample{
		void cat(){
			System.out.println("매개변수 없음");
    	}
    	void cat(int a){
			// System.out.println("매개변수 하나");
			System.out.printf("현재 %d마리의 고양이가 있습니다.\n", %d);
			// > 동일한 메소드지만 
    	}
    	void cat(String b){
			//System.out.println("매개변수 하나");
			System.out.printf("고양이가 있는 곳은 %s입니다.\n", %s);
    	}
	}
	// => main메소드에서 호출 가정 한다면
	OverloadingExample ole = new OverloadingExample(); // 
	ole.cat(); 		// => 매개변수 없음 출력
	ole.cat(4);		// => 현재 4마리의 고양이가 있습니다. 출력
	ole.cat("동물병원"); // => 고양이가 있는 곳은 동물병원입니다. 출력
{% endhighlight %}

