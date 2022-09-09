# Markdown中快速插入图片

之前用markdown写作，传图片都是手动上传到imgur，然后再人工添加链接，感觉确实比较耗费时间。


## 受到大妈启发
> [@ZoomQuiet](https://github.com/OpenMindClub/Writer002/issues/88)  
>其实, 有相关浏览器插件,可以自动将图片上传 7niu 并生成 md 图片引用链接到正文中的  
>当然, 类似的教练们有利用 MAC 的内置便利工具完成自动化的
>
>[Mac OS 图床运用优化模式 - Microdust](
http://azeril.me/blog/How-To-Use-Image-Hosting-Quickly.html)  
>等等,很多....就不一一帮搜了.

Update 2016-04-01:  
谢谢 @jeromevc 的分享，发现上面大妈提到的插件，就是 [极简图床](http://yotuku.cn/) ，用起来也非常简单，也不会遇到在mac的terminal里挣扎的痛苦。

## 说干就干
参照插件作者的blog进行操作 [使用Dropzone和七牛云存储来优化博客图床](http://yansu.org/2015/01/10/use-dropzone-and-qiniu-to-store-blog-images.html)
不过无奈的是，最后一直都出错。  

## 解决ruby安装路径错误
参照作者的留言，初步判定应该是我的路径和作者不一样
> 因为我的ruby环境是brew装的，所以路径设置成了/usr/local/bin/ruby，你如果不是用的brew版ruby，需要重新设置一下。

可是真心不知道要在哪里设置啊。
再google一通搜索后，最后终于通过查找“七牛插件 mac”，
发现[这篇文章](http://www.waerfa.com/upload-pix-to-qiniu-by-dropzone)中有提到

> 但在实际操作中，你可能会像我一样遇到 Qiniu Ruby 库无法正常安装的情况，此时你需要确认一下系统 Ruby 的安装目录，有的时候她会安装在 /usr/bin/ 里，也有时候会在 /usr/local/bin/，此时你需要到 Dropzone Qiniu 插件 里的 Action.rb 里编辑一下注释段落最后一行里对 RubyPath 的路径，如下图，不然你在使用插件时会遇到以下类似的错误提示

![](http://7xsjcm.com1.z0.glb.clouddn.com/dropzone.png)
在实际操作的时候，就是在Dropzone右击Qiniu的图标，选择EditScript，在上方的注释部分添加上图所指的那一行文字就可以啦。

## 回顾
解决错误总是如此纠结，让我在google中和terminal中尝试来尝试去，搜索来搜索去，真的是觉得想放弃了。  
但是当最后用上这个服务的时候，顿时觉得好爽，节约了好多时间，一切都变得这样简单顺畅。  
顿时觉得这种简单无聊的工作就应该自动化啊！  
顿时觉得在geek的世界中，有很多解决问题的好方法啊！  
以后也要学着多多发掘，让生活更简单。

