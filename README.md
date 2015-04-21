# iOS-Resource-Integration


## Objective-C
### 基本语法
- [十分钟让你明白Objective-C的语法（和Java、C++的对比）](http://blog.csdn.net/totogo2010/article/details/7632384) 
- [Objective-C语法快速参考](http://www.cocoachina.com/b/?p=122) 简单的介绍，语法快速入门。
- [维基百科Objective-C](http://zh.wikipedia.org/wiki/Objective-C) 推荐阅读，维基百科对于Objective-C较为详细的介绍。
- [苹果官方Objective-C开发说明文档](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html)  官方权威。

## Swift
- [The Swift Programming Language 中文版](http://numbbbbb.gitbooks.io/-the-swift-programming-language-/content/)

## 布局
iOS中进行界面布局有三种方式：代码手写UI、使用InterfaceBuilder进行xib布局、storyboard。

代码手写UI，完全通过手写代码布局,灵活性强,代码可重用，但开发效率低，而且必须到运行时才能知道布局效果。

xib，使用InterfaceBuilder可视化界面布局，所见即所得，开发效率高，但灵活性差。

storyboard，由多个xib以及导航关系合成，可看做是一组xib，以及xib之间的转换方式的集合。故事版清晰地展示出界面中的逻辑和层次结构。也是Apple对开发者的建议和未来的方向。
- [代码手写UI，xib和StoryBoard间的博弈](http://onevcat.com/2013/12/code-vs-xib-vs-storyboard/)

## UIKit

## 布局自适应
### Auto Layout、Size Classes
iOS6新增的Auto Layout和iOS8新增的Size Classes。
- [为iPhone 6设计自适应布局](http://www.cocoachina.com/ios/20141020/9978.html)
- [iOS 开发实践之 Auto Layout](http://xuexuefeng.com/autolayout/)
- [iOS8 Xcode6中Size Classes简单使用教程](http://www.swiftmi.com/topic/105.html)
- [Auto Layout官方文档](https://developer.apple.com/library/ios/recipes/xcode_help-IB_auto_layout/_index.html#//apple_ref/doc/uid/TP40014226)
- [Size Classes官方文档](https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/_index.html#//apple_ref/doc/uid/TP40014436)

### NSLayoutConstraint
通过代码创建约束实现Auto Layout，Apple难用的NSLayoutConstraint工厂。
- [学习AutoLayout（NSLayoutConstraint）](http://www.jianshu.com/p/ebb8570ad70f)
- [iOS在代码中使用Autolayout](http://gaoxiaosong.xsweby.com/2014/04/07/ios-code-autolayout.html)

### Visual Format Language
同样也是通过代码创建约束，Visual Format Language基于字符串，不利于编译器检查，可读性差。
- [使用Auto Layout中的VFL(Visual format language)](http://www.cnblogs.com/wupei/p/4150626.html)
- [在UIScrollView中使用Auto Layout中的VFL](http://www.cnblogs.com/wupei/p/4428164.html)
- [Visual Format Language官方文档](https://developer.apple.com/library/mac/documentation/UserExperience/Conceptual/AutolayoutPG/VisualFormatLanguage/VisualFormatLanguage.html#//apple_ref/doc/uid/TP40010853-CH3-SW1)

### Masonry
轻量级的布局框架，简洁的链式语法，可读性高。
- [github](https://github.com/SnapKit/Masonry)
- [Masonry介绍与使用实践(快速上手Autolayout) ](http://adad184.com/2014/09/28/use-masonry-to-quick-solve-autolayout/)

### Cartography
利用Swift丰富的操作符重载特性，声明Auto Layout。
- [github](https://github.com/robb/Cartography)

### FLKAutoLayout
一个干净的原生API包装框架。
- [github](https://github.com/floriankugler/FLKAutoLayout)

## 关于图片
### Asset Catalog
Asset Catalog用来管理任意图片（包括app icon、启动图片）如@1x，@2x，@3x图片,使用的时候使用Asset名字。还可以可视化处理图片进行拉伸。
- [Asset Catalog官方文档](https://developer.apple.com/library/ios/recipes/xcode_help-image_catalog-1.0/Recipe.html)

还可以通过使用向量图(PDFs)加入到asset catalogs，Xcode可以自动地根据它们生成位图。
- [USING VECTOR IMAGES IN XCODE 6](http://martiancraft.com/blog/2014/09/vector-images-xcode6/)

关于@1x，@2x，@3x：iOS中图片通过@1x，@2x，@3x为不同分辨率的设备统一为一个尺寸所作的标记
- [切图常说的@1X@2X@3X是什么意思？-知乎](http://www.zhihu.com/question/26195746)

## 设计规范、流程
- [iPhone、iPad app设计规范](http://www.ui001.com/chicun/)
- [iOS APP设计一稿支持iPhone5/iPhone6/Plus设计流程](http://www.ui001.com/article/visual/ios-app-she-ji-yi-gao-zhi-chi-iphone5-iphone6-plus-she-ji-liu-cheng.html)

## 数据存储

## 网络通信
### AFNetworking
- [github](https://github.com/AFNetworking/AFNetworking)

## Json

## 事件通知
### 委托(Delegate)
Apple中经常用的委托执行回调。
- [iOS视图控制器之间delegate传值教程](http://mojijs.com/2014/10/160124/index.html)
- [IOS 委托代理（delegate）实现页面传值](http://www.androiddev.net/lvesli_delegate/)

### Callback blocks (回调代码块)
block也可以实现回调，实现过程比委托回调更简洁。
- [Objective-C中的Block回调模式](http://www.cnblogs.com/ludashi/p/3922911.html)

### NSNotificationCenter
一种类似广播的消息通知机制。观察者只需要向消息中心注册，当有地方发出这个消息的时候，通知中心会发送给注册这个消息的对象。
- [iOS的消息传递机制—NSNotificationCenter](http://segmentfault.com/a/1190000000610302)
- [NSNotificationCenter](https://developer.apple.com/library/ios/documentation/Cocoa/Reference/Foundation/Classes/NSNotificationCenter_Class/index.html#//apple_ref/doc/uid/TP40003701) 官方文档

### Key-Value Observing (KVO，键值编码)
KVO源于设计模式中的观察者模式，简单的说就是：指定的被观察的对象的属性被修改后，KVO就会自动通知相应的观察者。
- [Objective-C之KVC、KVO](http://www.cnblogs.com/kenshincui/p/3871178.html)
- [详解键值观察（KVO）及其实现机理](http://www.cppblog.com/kesalin/archive/2012/11/17/kvo.html)
- [Registering for Key-Value Observing](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/KeyValueObserving/Articles/KVOBasics.html#//apple_ref/doc/uid/20002252-BAJEAIEE) 官方文档

## 多线程

## Core Graphics、Quartz 2D
Core Graphics框架是一组用于绘制2D图形的API，使用CPU进行计算。

Quartz 2D是Core Graphics的一部分，基于C的API。
- [Drawing iOS 7 2D Graphics with Core Graphics](http://www.techotopia.com/index.php/Drawing_iOS_7_2D_Graphics_with_Core_Graphics) Core Graphics、Quartz 2D简介。
- [An iOS 7 Graphics Tutorial using Core Graphics and Core Image
](http://www.techotopia.com/index.php/An_iOS_7_Graphics_Tutorial_using_Core_Graphics_and_Core_Image) Graphics、Quartz 2D绘图API示例。
- [Core Graphics Tutorial for iOS](http://www.raywenderlich.com/tag/core-graphics) Core Graphics使用实例。
- [Quartz 2D Programming Guide](https://developer.apple.com/library/ios/documentation/GraphicsImaging/Conceptual/drawingwithquartz2d/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007533-SW1) Quartz 2D官方文档


## Core Animation

## 国际化
- [iOS应用国际化教程](http://www.cocoachina.com/industry/20140526/8554.html)

## 推送

## Xcode

## 工具、插件

## 第三方平台

