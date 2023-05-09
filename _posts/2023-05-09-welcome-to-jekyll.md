---
layout: post
title:  "오버로딩과 오버라이딩"
date:   2023-05-23 01:30:13 +0800
categories: Java
tags: Array 
comments: 1
---
<오버로딩>
	오버로딩은 같은 이름의 함수(메소드)를 여러개 정의하고, 매개변수의 타입과 개수를 다르게 하여 
	다양한 호출에 응답할 수 있게 된다. 

{% highlight java %}
class OverloadingExample{
		void cat(){
			System.out.println("매개변수 없음");
    	}
    	void cat(int a){
			# System.out.println("매개변수 하나");
			System.out.printf("현재 %d마리의 고양이가 있습니다.\n", %d);
			// > 동일한 메소드지만 
    	}
    	void cat(String b){
			//System.out.println("매개변수 하나");
			System.out.printf("고양이가 있는 곳은 %s입니다.\n", %s);
    	}
	}
	#=> main메소드에서 호출 가정 한다면
	OverloadingExample ole = new OverloadingExample(); // 
	ole.cat(); // => 호출시 생성한 객체의 변수명으로 가능하며 점(".")을 사용하여 클래스내 메소드를 불러올수 있다.
	ole.cat(4);		// => 현재 4마리의 고양이가 있습니다. 가 출력됨
	ole.cat("강남동물병원"); // => 고양이가 있는 곳은 강남동물병원입니다. 가 출력됨
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/