# iOS-Resource-Integration


## Objective-C

### 基本语法
- [十分钟让你明白Objective-C的语法（和Java、C++的对比）](http://blog.csdn.net/totogo2010/article/details/7632384) 
- [Objective-C语法快速参考](http://www.cocoachina.com/b/?p=122) 简单的介绍，语法快速入门。
- [维基百科Objective-C](http://zh.wikipedia.org/wiki/Objective-C) 推荐阅读，维基百科对于Objective-C较为详细的介绍。
- [苹果官方Objective-C开发说明文档](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html)  官方权威。

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

## 多线程

## CoreGraphic

## Core Animation

## 国际化
- [iOS应用国际化教程](http://www.cocoachina.com/industry/20140526/8554.html)

## 推送

## Xcode

## 工具、插件

## 第三方平台

