
# 远程开机_网络唤醒设置方法 (WOL, Wake on Lan)

## 使用方法：有线接入到极路由的电脑切换到休眠状态，在极路由安装WOL插件，然后极路由手机APP上唤醒电脑。

## 操作系统中配置网卡

在设备驱动管理器中，找到 网络适配器 ，在第一个驱动 右键 -> 属性

![网卡属性]（https://beyondthe.top/img/wangka1.png）

在 高级 菜单中的属性找到 唤醒魔包 (Wake on Magic Packet) Wake on pattern match 设置为 启用

![开启唤醒]（https://beyondthe.top/img/wangka2.png）

在 电源管理 中 勾选 允许此设备唤醒计算机

![电源管理]（https://beyondthe.top/img/wangka3.png）

## 测试看是否成功，不成功的话还要重启到电脑BIOS中的ACHI，PCIE等设置中找到Wake on Lan等设置。

![PCIE设备唤醒]（https://beyondthe.top/img/bios1.png）

![ACHI设备唤醒]（https://beyondthe.top/img/bios2.jepg）

[更多方法](https://blog.csdn.net/liuyukuan/app/article/details/53439118)

[linux远程开机](https://www.cnblogs.com/klb561/p/8679329.html)
