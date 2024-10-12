# 小娱C5路由器OpenWrt固件Lean
>简要说明

## 硬件信息
* 架构。
* CPU。
* 内存。
## 基础包
* a
* b
## 主题
* bootstrap
* [Argon](https://github.com/jerrykuku/luci-theme-argon)
## 插件
* [luci-app-zerotier](https://github.com/coolsnowwolf/lede/tree/master/package/lean/luci-app-zerotier)
* [luci-app-jd-dailybonus](https://github.com/jerrykuku/luci-app-jd-dailybonus)
## 拓展功能
* IpV6支持
## 默认配置
* 登录地址和账号密码
* 内网
## 编译说明
* 编译方法。
* 编译时间。
* 编译版本。
自动编译，分基础版和加强版。基础版包含基础软件，加强版在基础版的基础上，添加了xxx等软件。


## 常见问题说明Q&A

### 如何更新固件?

### 2021年6月发生了什么，导致必须清楚配置升级？

### 如何手动安装或更新插件包?

### 如何取消默认编译进固件的插件？

### 编译openwrt时取消预选的软件包?





**说明：** 采用GitHub actions自动编译，每周一拉取[Lean大的源码仓库](https://github.com/coolsnowwolf/lede)更新。编译配置中取消了部分默认预选插件，添加了部分插件包括ipv6支持需要的插件。配置详见[这里](https://github.com/qughij/openwrt-xiaoyu_xy-c5/blob/master/.github/workflows/build.yml)



## 关于ipv6

现在基本上手机网络和宽带都能获得ipv6地址了，所以还是要用起来。

况且，DDNS可以解析ipv6，实现外网访问路由器或其它服务（openvpn可以通过tcp-ipv6实现连接到家庭网络）

但注意的是，在外使用时，一定要先确认自己的手机网络获得了ipv6地址，不然是访问不了基于ipv6的服务的。


## 关于编译时取消预选插件

默认设置在/openwrt/include目录下面的target.mk中，参考知乎文章[编译openwrt时取消预选的软件包](https://zhuanlan.zhihu.com/p/70656867)
