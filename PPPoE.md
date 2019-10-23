# 介绍

PPPoE是Point to Point Protocol over Ethernet的缩写，意思也就是以太网上的PPP，其中PPP是Point to Point Protocol（点到点协议）的字母缩写，故PPPoE也称PPP over Ethernet，即PPPoE协议。可以说PPPoE是将以太网和PPP协议相结合的协议，是在以太网中转播PPP帧信息的技术，它利用以太网将大量主机组成网络，通过一个远端接入设备连入因特网，并对接入的每一台主机实现控制、计费功能，PPPoE广泛应用在包括小区组网建设等一系列应用中，前些年流行的宽带接入方式ADSL 就使用了PPPoE协议。

PPPoE不仅有以太网的快速简便的特点，同时还有PPP的强大功能，任何能被PPP封装的协议都可以通过PPPoE传输，此外还有如下特点： 

1、PPPoE很容易检查到用户下线，可通过一个PPP会话的建立和释放对用户进行基于时长或流量的统计，计费方式灵活方便。 

2、PPPoE可以提供动态IP地址分配方式，用户无需任何配置，网管维护简单，无需添加设备就可解决IP地址短缺问题，同时根据分配的IP地址，可以很好地定位用户在本网内的活动。 

3、用户通过免费的PPPoE客户端软件(如EnterNet)，输入用户名和密码就可以上网，跟传统的拨号上网差不多，最大程度地延续了用户的习惯，从运营商的角度来看，PPPoE对其现存的网络结构进行变更也很小





# 搭建文章

## 基于Linux环境的PPPOE服务器搭建

<https://www.imooc.com/article/50559>



## ubuntu上搭建PPPOEServer

<https://blog.csdn.net/leiming32/article/details/50462838>



## Linux下搭建 PPPoE Server 问题总结

<https://blog.csdn.net/pdcxs007/article/details/44599885>