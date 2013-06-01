---
layout: post
title: "Middleman网站新设计"
description: ""
category: 
tags: []
---
{% include JB/setup %}
==========================================
Middleman是一个使用各种快捷方式和工具在当下Web开发环境下的静态网站发生器。  
<div align="center"><img src="http://media.tumblr.com/tumblr_m76dvhusKv1qafhdm.jpg"/></div>  
######Middleman有一个官方的扩展以支持博客，文章和标记。
<!--break-->
######它的使用方法非常简单，首先确保你已经安装了ruby环境，详见:<http://ruby-china.org/wiki/install_ruby_guide/>，middleman的安装请输入：  
<pre>gem install middleman</pre>  
安装过程中会添加一个新的命令到你的enviroment中，有3个非常有用的功能：  
<pre><ul><li>middleman init</li><li>middleman server</li><li>middleman build</li></ul></pre>  
新建一个Middleman网站---middleman 初始化:  
<pre>middleman init my_new_project</pre>  
每一个新的项目，为您创建一个基本的web开发骨架。这自动的层次结构的文件夹和文件，您可以使用在所有项目的建设。一个全新的项目将包含一个源文件夹(source)和一个config.rb文件。源文件夹，在那里你会建立自己的网站。骨架项目包含JavaScript，CSS和images文件夹，但你可以改变这些以符合您自己的个人喜好。  
Middleman允许使用Bundle Gemfile锁定你的gem依赖。当创建一个新的项目，Middleman将产生的Gemfile指定你使用的是同一版本的Middleman。  
config.ru文件描述网站如何被一个机架功能(Rack-enabled)的Web服务器加载。此文件提供一个方便用户部署他们的Middleman网站到一个基于机架的主机，如Heroku。要在你的项目中包括一个的样板config.ru文件，添加`--rack`外部链接到初始化命令: 
<pre>middleman init my_new_project --rack</pre>  
在本地测试，使用：  
<pre>bundle exec middleman server</pre>  
它和下面这个命令是一样的：  
<pre>bundle exec middleman</pre>
当然如果你熟悉rails框架的话，你也可以这样做：  
<pre>bundle install</pre>  
<pre>middleman</pre>  
打开浏览器，在地址栏中输入`http://localhost:4567/`，这样你就可以在本地Web服务器上看到它的样子了。  

Middleman-blog作为middleman一个扩展，可以帮助你迅速的建立一个属于你的静态博客。要安装使用它，只要在你的Gemfile中添加：  
<pre>gem "middleman-blog"</pre>  
如果你不想用到`bundle`命令，你也可以通过手动在命令行输入：  
<pre>gem install middleman-blog</pre>  
除此之外，如果你想在之前建立的项目里加入Middleman-blog，那么你可以这样做：  
<pre>middleman init PROJECT_NAME --template=blog</pre>  
当你已经完成上述步骤之后，你可能就想创建一篇新的文章，当然你可以手动添加，Middleman提供了一种快捷方式，下面这条命令可以供你使用：  
<pre>middleman article TITLE</pre>
这跟jekyll中使用的`rake post title=""`是比较类似的。
如果你已经完成了上面的所有步骤，那么恭喜你，你已经完成了一个属于你的简单静态博客网站的创建。继续探索吧，你会得到更多的乐趣。  
Want more Info,you may just refer to:<http://middlemanapp.com/blogging/>
  
