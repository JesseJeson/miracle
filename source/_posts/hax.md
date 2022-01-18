---
title: hax的免费vps
date: 2022-1-3 11:53:00
tags:
- 白嫖
- 服务器
---
## 0.准备材料
telegram帐号，~~脑子和手~~QAQ
前排提示，这个服务器只有ipv6，但可以用[warp](https://blog.misaka.rest/202110/89.html)让他有ipv4.

## 1.注册帐号
(建议先加入telegram群，点击官网那个Join our Telegram Group 就行)
打开<https://hax.co.id/register/>，根据要求去telegram私聊机器人(@HaxTG_bot)，发送/getid，![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641182448000.png)，然后把得到的id输入，点击submit。然后机器人就回发过一个验证码来(图一)。把验证码填入第一个文本框，在第二个文本框输入密码(图二)，点击submit，帐号就注册好了。

![图一](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641182821000.png)
![图二](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641182839000.png)

## 2.白嫖vps
<https://hax.co.id/login/>登录帐号，ID就是getid获取的，password是自己设定的。验证码加载可能较慢，如有需要可挂梯子。

![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641183050000.png)
点击这里的Create VPS
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641183267000.png)
如图所示。DataCenter是选择vps地区的，后文介绍区别，Operating System是选择系统，根据个人喜好吧。Password是ssh连接服务器时的密码。VPS  purpose 是目的，随便选。最后把五个复选框点上，验证验证码，点击Create VPS就行啦QwQ。

### 补充DataCenter
eu1-10是德国服务器，没什么特殊的(500m内存应该是4g硬盘)。eumid1也是德国服务器，但是是1g内存10g硬盘(如果列表没有就是抢没了，共120台，常年满人)，这些都是kvm区。
eu openvz用满一个月可以升级内存到1gb，看图![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641183741000.jpg)
ID1(印尼的机器，国际宽带很小，不建议)，US-LA，US-NYC(美国的)，是LXC区，配置和kvm区差不多。

## 3.连接vps
去<https://www.test-ipv6.com/>看一下，如果有ipv6好说。直接ssh连接就好。如果显示没有ipv6(~~例如我~~)，就可以用官方的[ipv6-ipv4](https://hax.co.id/ipv6-to-ipv4/)，把ipv6转发到ipv4。
看图就行
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1641186001000.png)

## 4.用途
这样配置的vps最常见的用途就是搭建vpn，但你也可以搭建web服务器，mc服务器等(可以去看看小岚dalao的[博文](https://blog.ltya.top/richang/330.html))。QwQ