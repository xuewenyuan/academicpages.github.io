---
title: 'TexLive + Atom,教你配置炫酷的LaTex编译环境'
date: 2016-10-20
permalink: /posts/TexLive+Atom
tags:
  - LaTex
  - 环境配置
---

**原创，转载请标明引用出处。**

## TexLive + Atom

[LaTex](https://en.wikipedia.org/wiki/LaTeX)排版系统是科研工作者写作的标配，[TexLive](https://en.wikipedia.org/wiki/TeX_Live)就是一款用于LaTex编译的发行版软件，包含了LaTex的主要程序，以及各种宏包和字体。选择TexLive还有两个主要的原因就是它自带Beamer(用LaTex做slides最常用的包，大咖们那些好看的幻灯片可不是用PPT做的哦)，省去了你额外配置Beamer的麻烦，另外TexLive长期支持更新。  

[Atom](https://atom.io/)是GitHub推出的一个跨平台文本编辑器，支持几乎所有的语言，并且还可以通过安装“功能包”的方式来扩展编辑器的功能(语法高亮、自动补全、编译预览、配色方案...)。作为计算机专业的学生，你可能经常使用多门语言，但是完全没有必要为所有的平台都配置一套专有的编辑环境，那会使我们的电脑变得拥挤不堪，Atom就帮我们解决了这个问题，而且极易上手使用。

## 环境配置

### 软件下载

首先从如下地址分别下载TexLive和Atom。  
**[TexLive][1]**    
**[Atom][2]**  
[1]:https://pan.baidu.com/s/1eSuS71w#list/path=%2F  
[2]:https://github-cloud.s3.amazonaws.com/releases/3228505/156b3c88-9484-11e6-89ac-4b9033378650.exe?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAISTNZFOVBIJMK3TQ%2F20161020%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20161020T132923Z&X-Amz-Expires=300&X-Amz-Signature=4dc7e17c2f72eba11614243cfbb5c9b599f3fe977ecad8d155d758c29b6c324d&X-Amz-SignedHeaders=host&actor_id=7368805&response-content-disposition=attachment%3B%20filename%3DAtomSetup.exe&response-content-type=application%2Foctet-stream

### 安装  

Atom的安装非常简单，下面说一下TexLive的安装。  

1. 解压下载的镜像文件，双击文件“install-tl-advanced”  
![](http://ww1.sinaimg.cn/large/535663c3gw1f8z2rjx015j20mr0fkdjk.jpg)  
2. 在如下窗口中点击“continue”  
![](http://ww2.sinaimg.cn/large/535663c3gw1f8z2sw5jjjj208r04caag.jpg)  
3. 如下的安装选项窗口中，最后两项点击"切换"，选择"否"，然后开始安装，经过漫长的等待之后，安装就结束了。  
![](http://ww4.sinaimg.cn/large/535663c3gw1f8z2x2agd5j20fc0egq5j.jpg)  


### Atom的配置

通过TexLive的安装，电脑的LaTex环境就已经配好了，想要在Atom上使用，我们还需要安装几个Packages。  
首先，在Atom的File菜单栏中点开Settings，选择Install选项卡，在搜索栏分别搜索以下几个Packages，并安装：  
* 语言高亮：language-latex  
* 编译：latex
* PDF预览：pdf-view
* 击键效果：activate-power-mode（可选）

![](http://ww3.sinaimg.cn/large/535663c3gw1f8z3miaprrj20u30dmdiq.jpg)

之后我们在File中新建文件，并在Atom编辑器的右下角选择LaTex语言，输入以下内容：

```
% small.tex
\documentclass{beamer}%声明文档类型
\usetheme{default}%使用默认主题
\begin{document}

\begin{frame}{A sample slide}

A displayed formula:

\[
\int_{-\infty}^\infty e^{-x^2} \, dx = \sqrt{\pi}
\]

An itemized list:

\begin{itemize}
\item itemized item 1
\item itemized item 2
\item itemized item 3
\end{itemize}

\begin{theorem}
In a right triangle, the square of hypotenuse equals
the sum of squares of two other sides.
\end{theorem}

\end{frame}

\end{document}
```

输入完成后，新建一个测试文件夹，将文件保存在该路径下，在菜单栏中选择"Packages->LaTex->Build",则会生成如下所示的一张slides(文档类型为beamer)，下面就可以愉快的使用LaTex写论文了！：）

![](http://ww1.sinaimg.cn/large/535663c3gw1f8z3njkzhfj20nq0hsmyc.jpg)

![](http://ww3.sinaimg.cn/large/535663c3gw1f8z3rfhwqig20e607m4qq.gif)

Ps:在Setting中还可以下载大量Atom的主题！

---------------------------------------------------
**如有任何相关问题欢迎评论或者邮件讨论<15120452@bjtu.edu.cn>**
------
