---
title: 一次糟糕的更换博客主题记录
date: 2021-5-4 16:10:50
tags:
- 日常
- 博客
---
## 起因
一直想更换waline好久，但由于博客主题不支持waline，于是就拖了好久
今天，终于要换主题啦！~~然而还是没换成~~
挑了好久，终于选出了一个MengD<https://mengd.lete114.top/>

## 经过
我家网差到离谱，github网站登不上去，就想着下github desktop，下这个就废了我20分钟
github desktop好像没有中文？我就边摸索，边换主题
满怀希望滴上传了第一次push，一看，没变化(´இ皿இ｀)
到处找原因——原来是_config.yml里的theme 项没改。。。。。。。。
第二次上传上去，编译失败！！！
我又改了改，第三次上传——主页就是空白的！我甚至还去看了看vercel的output，index.html就是空的！！~~震惊我一百年~~
我于是就不抱希望了，准备换回原来的主题
也不知道是我脑子短路了还是怎么的，忘了把config里的theme项改一改就可以，还去网上找github回滚。。
终于，我想到了改一改config这个方法，博客也恢复了原样
看一下push记录![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1620116326000.PNG)

## 结果
~~我再也不敢换主题了~~（雾）