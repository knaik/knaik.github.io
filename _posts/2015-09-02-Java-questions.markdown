---
layout: post
title:  "CS 112 Questions"
date:   2015-09-02 14:40:00
categories: CS112
---
#Question about pass by value

{% highlight java %}
public class Test{
	public static void main(String args[]){
		int a = 1;
		int b = 2;
		int x = 0;
		
		System.out.println("original");
		System.out.println(a + "a");
		System.out.println(b + "b");
		
			
		System.out.println("swap method 1");
		swap(a, b);	
		System.out.println(a + "a");
		System.out.println(b + "b");
		
		System.out.println("swap method 2");
		int temp2 = a;
		a = b;
		b = temp2;		
		
		System.out.println(a + "a");
		System.out.println(b + "b");
	}

	public static void swap(int c, int d){
		int temp2 = c;
		c = d;
		d = temp2;		
	}	
}
{% endhighlight %}
'original
1a
2b
swap method 1
1a
2b
swap method 2
2a
1b'