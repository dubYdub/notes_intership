

![图片描述](C:\Users\29551\OneDrive\2020-Autumn\notes_intership\assets\5b67b3da0001548f06780584.png)



### Ubuntu版本号为16.04，内网IP地址为192.168.1.100，外网网关地址为172.20.10.1。内网网卡名称为enp2s0，外网网卡名称为enp0s29f7u7c4i2，外网为USB连接手机开热点的方式。





## Step1:  pppoe服务添加默认网关使之能访问外网 ：

> #### sudo route add default gw 172.20.10.1 dev enp0s29f7u7c4i2





## Step 2:转发pppoe上的数据到外网上: 192.168.1.0/24为实际的网卡的网络地址。

> #### sudo iptables -A POSTROUTING -t nat -s 192.168.1.0/24 -o enp2s0 -j MASQUERADE





## Step 3: 运行 PPPoE 服务器,电脑重启后需要重新运行此命令

> #### sudo pppoe-server -I enp2s0 -L 192.168.1.10 -R 192.168.1.19 -N 20，

- -I 参数为指定pppoe服务器所监听连接请求的网卡名称，可使用 ifconfig 命令查看。
- -L 参数PPPoE服务器的IP地址，此IP地址为PPPOE服务器的虚拟IP地址，与网卡enp2s0 地址无关
- -R 参数为当有客户连接到服务器上时，pppoe服务器分配给客户端的起始IP地址
- -N 参数为指定最多可以连接pppoe服务器的客户端数量



## 关闭PPPOE服务器

> ####  killall pppoe-server