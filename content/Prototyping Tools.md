+++
weight = 1
title = "Prototyping Tools"
date = "2012-04-06"
+++

刚好借着项目需求分享一些我用过的制作交互原型的工具，使用这些工具可以快速的将想法呈现出来并且快速验证。

做Prototype的工具大致分成两个阵营，一个阵营是制作早期原型，用于快速验证逻辑和迭代，另一个阵营是制作高保真的动态原型，可以输出非常逼近于原生应用的动态Demo。这两个阵营的产品都有Web App和Native App可以选择，有非常简单易学，上手容易的，也有非常复杂并且需要编程基础的，这些都可以基于项目的情况进行选择。我下面介绍一些现在评价和口碑都不错的Prototyping产品。
<!--more-->

## [invision](http://www.invisionapp.com/)

InVision应该是属于制作早期原型的产品，功能非常强大，可以作为原型制作到交流沟通的一个统一平台，几乎可以解决所有的需求。
InVision的流程也比较简单，主要是基于图片上Hotspot的跳转，只需要将设计好的界面图片导入到他的Project里面，在每个界面上画出可点击的Hotspot区域，然后指定这个热点跳转到的页面即可，但是无法做出转场的动画效果。其实这个模式有点类似在Keynote里面做超链接跳转的方式。同时InVision引入了协作模式，可以多人共同编辑和添加焦点评论，所以也可以将InVision当做Design Review的工具使用，最后也可以将做好的原型可以生成链接发给别人。
InVision支持Dropbox同步设计图，只要将所有的界面图放到Dropbox中就可以自动同步到指定的Project里面，这个功能十分方便。最近它们还推出了直接无缝支持Sketch的重磅功能，可以自动将Sketch中的Artboard转换为Screen（在InVision中每个上传的界面图都叫做一个Screen），这个功能实在是极大的方便了使用Sketch的设计师（所以还有什么理由不用Sketch呢？）。现在唯一的问题是InVision在国内的访问速度有点慢，最好还是科学上网之后使用。

## [marvel](http://marvelapp.com/)

Marvel属于比较简单容易上手的工具，使用模式和InVision也比较类似，都是基于Hotspot跳转来做原型。同时也支持Dropbox和Sketch，不过Marvel的新版增加了很实用的转场动画，可以比较方便的设置两个界面的转换效果，基本上都是现在移动产品上比较常用的一些转场动画。Marvel也支持在移动端进行调试和预览。个人感觉Marvel中比较实用的一个功能是可以制作页面的滚动，同时可以设置不滚动的区域，也就是说如果我们做的界面是带有StatusBar的一个长界面，那么在Marvel中可以设置Statusbar的区域始终在最顶端，但是内容区域可以滚动，这个小功能是Marvel比较出彩的一个特性。

## [pixate](http://www.pixate.com/)

Pixate是一个前一段时间开始流行的Web App（其实它也有mac版的，但只是套了一个外壳，内核其实还是webview），pixate其实就像是一个进阶版的keynote，主要用来给设计好的界面图加上交互和动画使其串联成一个可以交互的流程，pixate里面内置的互动行为和动画还是比较丰富的，可以做出逼近于原生应用的效果，可以即时预览，上手相对也比较简单，但缺点就是只能使用它们内置的行为和动画，没有办法自己定义，其实还是有些不灵活，而且pixate在浏览器中运行的效率不是很理想，访问速度也有点慢，但关键的是这家伙真心不便宜。

*更新: Pixate现在已经被Google收购*

## [Origami](https://facebook.github.io/origami/)

Origami绝对是这个领域的大杀器，但是想要用它的话也要费一番功夫。首先Origami是构建在Apple的[Quartz Composer](https://en.wikipedia.org/wiki/Quartz_Composer)（简称QC）的基础上的，而QC又依赖于apple的开发工具Xcode，所以要想尝试origami的话需要安装这一整套的软件包。Origami是Facebook基于QC开发的增强型Node集合，QC是一个基于节点来进行可视化逻辑开发的工具，每个节点可以理解为一个功能，节点拥有input和output端口用来接收或者输出数据，关于工作原理这里就不详细展开了。其实Origami就是将QC原有的节点进行了一些增强，并且加入了一些专门用于原型设计的节点。在origami里面可以实现几乎100%还原度的交互效果，著名的Facebook Paper就是通过origami和QC设计的。Origami的学习曲线比较陡峭，关键是要理解基于节点的可视化编程方式。想要详细了解可以看一下知乎的[这篇讨论](http://www.zhihu.com/question/20956344)。

与Origami和QC类似的还有被Google收购了的[Form](http://www.relativewave.com/form/)，但是这个之前试用过以后感觉执行速度实在是不佳。

## [Framer](http://framerjs.com/)

另外还有一个工具就是Framer，这个是基于[Coffeescript](http://coffeescript.org/)的原型开发工具，相当于提供了一套JS的交互框架，所有的交互效果都需要通过写代码来完成，同样也支持从Photoshop和Sketch里倒入设计图。但问题是国内会Coding的设计师实在是不多啊。


我们以后在设计产品的过程中会经常使用原型设计工具，目前比较推荐的是用InVision来进行早期的原型验证，后期配合Origami来做一些局部交互效果，如果是开发ios app的话origami可以直接生成xcode工程的可用代码，对于开发来说也可以比较省力。
