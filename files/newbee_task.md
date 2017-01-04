# Newbee Task

## 任务一：我们的目标是 IP

在 Linux 和 macOS 环境下，显示或配置网络设备（网络接口卡）的命令是 `ifconfig`（Windows 下是 `ipconfig`），当我们在 Command 模式下，输入这样一段命令后，会显示以下内容：
（以 macOS Sierra 系统，item2 环境为例）

```shell
# Desgard_Duan @ MacBook-Pro in ~/Desktop/HackSwjtu on git:master x [22:52:22] C:1
$ ifconfig
lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAST> mtu 16384
	options=1203<RXCSUM,TXCSUM,TXSTATUS,SW_TIMESTAMP>
	inet 127.0.0.1 netmask 0xff000000
	inet6 ::1 prefixlen 128
	inet6 fe80::1%lo0 prefixlen 64 scopeid 0x1
	nd6 options=201<PERFORMNUD,DAD>
gif0: flags=8010<POINTOPOINT,MULTICAST> mtu 1280
stf0: flags=0<> mtu 1280
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether ac:bc:32:8e:47:1f
	inet6 fe00::18f7:6e8e:6bac:cc1b%en0 prefixlen 64 secured scopeid 0x5
	inet 192.168.0.5 netmask 0xffffff00 broadcast 192.168.0.255
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: active
en1: flags=963<UP,BROADCAST,SMART,RUNNING,PROMISC,SIMPLEX> mtu 1500
	options=60<TSO4,TSO6>
	ether 00:00:00:00:c0:a0
	media: autoselect <full-duplex>
	status: inactive
en2: flags=963<UP,BROADCAST,SMART,RUNNING,PROMISC,SIMPLEX> mtu 1500
	options=60<TSO4,TSO6>
	ether 4a:00:02:cb:c0:a1
	media: autoselect <full-duplex>
	status: inactive
bridge0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=63<RXCSUM,TXCSUM,TSO4,TSO6>
	ether 4a:00:02:cb:c0:a0
	Configuration:
		id 0:0:0:0:0:0 priority 0 hellotime 0 fwddelay 0
		maxage 0 holdcnt 0 proto stp maxaddr 100 timeout 1200
		root id 0:0:0:0:0:0 priority 0 ifcost 0 port 0
		ipfilter disabled flags 0x2
	member: en1 flags=3<LEARNING,DISCOVER>
	        ifmaxaddr 0 port 6 priority 0 path cost 0
	member: en2 flags=3<LEARNING,DISCOVER>
	        ifmaxaddr 0 port 7 priority 0 path cost 0
	nd6 options=201<PERFORMNUD,DAD>
	media: <unknown type>
	status: inactive
p2p0: flags=8843<UP,BROADCAST,RUNNING,SIMPLEX,MULTICAST> mtu 2304
	ether 0e:bc:32:8e:47:10
	media: autoselect
	status: inactive
awdl0: flags=8943<UP,BROADCAST,RUNNING,PROMISC,SIMPLEX,MULTICAST> mtu 1484
	ether d1:1f:1c:47:a8:43
	inet6 fe80::d01f:1cff:fe27:a843%awdl0 prefixlen 64 scopeid 0xa
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: active
utun0: flags=8051<UP,POINTOPOINT,RUNNING,MULTICAST> mtu 2000
	inet6 fe80::9a5:b4f4:f8bc:1519%utun0 prefixlen 64 scopeid 0xb
	nd6 options=201<PERFORMNUD,DAD>
utun1: flags=8051<UP,POINTOPOINT,RUNNING,MULTICAST> mtu 1380
	inet6 fe80::33e9:2a0:2b35:b367%utun1 prefixlen 64 scopeid 0xc
	nd6 options=201<PERFORMNUD,DAD>
utun2: flags=8051<UP,POINTOPOINT,RUNNING,MULTICAST> mtu 1380
	inet6 fe80::ed1b:a994:2b95:3f9%utun2 prefixlen 64 scopeid 0xd
	nd6 options=201<PERFORMNUD,DAD>
```

在这之中我们可以获取到当前的 IP 地址、网关号以及子网掩码。但是在种场景下，我们想只让计算机显示这几个量，即格式为 `XXX.XXX.XXX.XXX` 的字符串，已知 XXX 的范围是 0-255，我们应该怎样做才能从这一大段命令反馈中只显示我们需要的信息呢？

## 任务二：密码有时候看不见真的好烦

有时候为了避免在录入密码时候出错，我们总是想把网页中密码输入变成明文。所以请完成这一目的。我们推崇嵌入 js 脚本，当然你封装成了 Browser 插件会加分的。

（结果如下图所示，下图是更改的教务网登录页）

![](img/newbee_task-1.png)