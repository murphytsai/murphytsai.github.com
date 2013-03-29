---
layout: post
title: "Objective-C Category"
date: 2013-03-29 10:25
comments: true
categories: 
---
Objective-C 和其他語言如 Java , C++特性上其中一個最大的不同就是 Category.
這樣的想法是來自於 Smalltalk 這個程式語言.


在 Objective-C 裡允許你添增新的 method，即使你手頭上沒有原先類別的程式碼。
Category 的定義和 Class 類似，但是它不能修改 Class 中的實例變數，即使是它的父類別也不行。
要注意的是 Category 的介面和實作都是 Optional的。


另一個須注意的是 宣告在 Category 中的 method 名稱若是與原本 Class 中的 method 有相同(衝突)，
那麼 Category 中的 method 將會優先被使用而取代原先的。


若有兩個 Category 中的 method 重覆了呢？那一個會被使用是沒有定義的(自求多福) !


{% codeblock lang:objc %}
//example : 在 NSObject 中新增 Category

@interface NSObject(MyAddedCategory)
-(void) addedMethod;
@end


@implementation NSObject(MyAddedCategory)
-(void) addedMethod
{
	NSLog(@"This new added method for extending NSObject function.");
}
@end

{% endcodeblock %}
