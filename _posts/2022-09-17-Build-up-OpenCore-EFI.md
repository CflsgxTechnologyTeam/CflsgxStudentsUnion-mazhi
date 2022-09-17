---
title: 转载:黑苹果指南
tags: 转载 黑苹果 折腾
img: /images/2022-09-17/images.png
date: 2022-09-17
categories: 黑苹果
layout: post
author: CharlesSu
describe: 这是一篇适合黑苹果毫无了解的小白。本文转载已经原作者[@CharlesSu]()同意，如二次转载请联系作者并标明出处。文章封面来源于网络。  
---

# 黑苹果指南
问问题请做一个有素质的人！

此文章投稿了不止一个平台，且每个平台的排版方式不同

所以此文章使用的是直角引号。

需要耐心！需要耐心！需要耐心！需要耐心！

## 前言

### 壹、这是一篇适合对黑苹果毫无了解的小白

```
适用于：你已经买到电脑，想装黑苹果
```

若你准备买一台可以装黑苹果设备

参考 [笔记本](https://github.com/daliansky/Hackintosh) [台式机](https://macx.top/18202.html)

### 贰、在开始前，你至少需要确保：

```
会进bios 

会至少一点点英语

有手、耐心

此文章用的是传统安装法，需要一个U盘
```

### 叁、文章会用到的简写

1.搜索 **XXX+中文(括号内是英文，在谷歌搜)**

2.笔记本和电脑统称电脑，如有特殊说明（笔记本有电池、触控板啥的），请按照特殊说明的来办

3.已经默认你会搭梯子、会使用GitHub(不接受此类问题)

4.~~像这种被划了线的句子,小白可以不用看~~

## 一、思考

```
·想想你装黑苹果来干嘛？

·愿不愿意一遍一遍的重启排错？

·愿不愿意仔仔细细的阅读一些英文的？甚至读不懂的俄语？

·能不能接受不稳定？

·需要大量时间，大量精力？
```

## 二、明确自己的配置

**Why?**

~~黑果的大概启动原理是：修改config和DSDT来启动OS X~~

```
当然这么说，显然不适合小白。
```

对于小白来说，你需要做的就是去搜一下 「机型+EFI」 即可

## 有现成的EFI

国内买的就去国内平台（包括但不限于bilibili、百度、各种论坛）

国外买的去Google 「型号+Hackintosh」

你的电脑如果找不到或者太冷门，且也想装黑苹果。就需要自己配EFI

## 无

如果没有，就要按照下面的内容来自行配置EFI

使用 **鲁大师、aida64、百度搜** 等，一定要准确的知道自己的配置，例如图一

# 三:配置EFI

```
这是一个 ！大点！
请结合多方信息，
不要只看我的这篇、也不要局限于国内互联网。
```

## 壹、你至少需要知道

```
1.黑苹果不怎么挑U，但太老、太偏、AMD，就节约时间不考虑了。上网本（奔腾、赛扬就直接pass不得行）

2.Intel的集显(HD+一些数字)、AMD的独立显卡大多都可驱动，这个请搜索 显卡型号+黑苹果”

3.网卡能驱动上的很少，能驱动的也有各种特殊方法。
具体情况请自行搜索，本文不展开

4.声卡同理，请自行搜索
```

##  贰、下载工作

### Part1: 必须下载（无论你是什么电脑，当然苹果电脑除外）
最好以我提供的名字为准，也可以随便取名字，你找到就行

~~这里的文件[参考](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#must-haves)部分软件请记住他的别称（打在括号里的）~~

```
请将你下载好的文件放在一起，软件请安装。请确保所有的东西你都能找到！
```

1.编辑plist配置的[plist编辑器](https://github.com/corpnewt/ProperTree) 或者[OpenCoreCFG](https://mackie100projects.altervista.org/opencore-configurator/)

2.必备，下载release[最简EFI](https://github.com/acidanthera/OpenCorePkg/releases)

3.[SSDT](https://github.com/corpnewt/SSDTTime)

4.diskgeunis(区分工具)百度去下

5.[Lilu](https://github.com/acidanthera/Lilu/releases)

6.[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases)

7.[WhateverGreen !部分AMD的集显不能装！](https://github.com/acidanthera/WhateverGreen/releases)

8.[AICP编辑工具](https://acpica.org/downloads/binary-tools)

9.[写盘工具](https://github.com/balena-io/etcher/releases/download/v1.7.9/balenaEtcher-Setup-1.7.9.exe)

10.[黑果小兵](https://blog.daliansky.net/)这里下载一个镜像，可以私聊我给你发一个

11.[排错1](https://shuiyunxc.gitee.io/2020/04/06/Faults/index/) [排错2](https://apple.sqlsec.com/10-%E6%8E%92%E9%94%99/)

    这里面是常见的黑苹果会遇到的问题，遇到问题了来这看看
### 这里是笔记本的附加部分，台式机请跳过

```
因为有电池、键盘鼠标等，笔记本用户大多都需要补充这些驱动。

当然凡事无绝对，你无法确保有些吃饱没事干，搞特殊，

这一部分适用于大部分用户，如果这一部分按照广普的教程不行，请百度搜索
```

#### 所有笔记本用户

1.SMCProcessor.kext

2.SMCSuperIO.kext

3.SMCLightSensor.kext

4.SMCBatteryManager.kext

5.SMCDellSensors.kext(仅限dell用户)

##### AMD用户需要额外补充的驱动

1.[AMDProcesser](https://github.com/trulyspinach/SMCAMDProcessor)

2.[AMDRadeonGPU](https://github.com/aluveitie/RadeonSensor)

### Part2：显卡

#### Intel核显 （也就是整个电脑没有显卡）

直接用这个[OC工具箱](https://www.123pan.com/s/rd39-MkpOd)特别省事

#### Nvdia ~~仅支持到10.13.6~~

[参考](https://www.bilibili.com/video/BV1wr4y1r78X?spm_id_from=333.337.search-card.all.click&vd_source=b2ed1387674e77df3a3f4f6acfe5a846)
这个部分争议较大，且这个技术比较新，又加上我没有Nvdia的显卡无法测试

所以英伟达用户请自行测试

#### AMD显卡（独显，如果你是vega8这类集显，要么等，要么C++逆向）

```
AMD显卡要么就是免驱，要么就是仿冒ID这一步AMD用户可以大喊一声：AMD YES
如果你是vega8的用户，且你刚好会C++，接触过逆向工程。欢迎联系我
```

### Part3: 声卡

声卡部分，由于不同品牌的网卡有不同的驱动方式

有些事注入ID就好，有些需要单独加驱动，有些又无法驱动

在此我帮你搜到了全网的大部分声卡驱动，剩下的你自己测试
[声卡](https://radcliffe.vercel.app/post/hei-ping-guo-sheng-qia-qu-dong/)

### Part4:网卡

网卡部分intel的看Intel

其他部分，把你的网卡型号在这里面搜索一下

有你的网卡，你就去对应搜索“型号+黑苹果

[Intel](https://zhuanlan.zhihu.com/p/299695036)
[其他网卡](https://zhuanlan.zhihu.com/p/339648390)

    现在，所有的下载工作应该都做完了，你可以稍事休息一下
    
    辛苦了，但真正的硬菜马上就来了。少喝酒，多吃菜

# 叁、配置EFI
请按照这个顺序或者你自己不会弄错的顺序来。

请将下载好的文件解压、安装。如果你看到 XXX.kext这种文件夹，就证明她已经是最简了

请将下载好的文件分好类。
## 一、地基
    将「最简EFI」解压到你找到地方
    
    删除Tools文件夹下的所有东西

    把Drivers文件下删得只剩 OpenRuntime.efi 「！仔细理解这句话！」
！把[这个](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)放在Drivers里面

## 二、AICP
~~这一步的目的是让系统可以控制硬件，软件控制硬件
[参考](https://www.bilibili.com/read/cv10117507/)~~

1.打开 __**SSDT**__  打开里的 __**SSDTTime.bat**__

2.以「4，3，2」的顺序「顺序不能错」会生成3个文件

3.现在我们需要处理下 **SSDT-RTC0.dsl** 

没有自动生成就[下载](https://github.com/acidanthera/OpenCorePkg/tree/master/Docs/AcpiSamples/Source/SSDT-RTC0.dsl)

用文本编辑器之类的打开它，用尽你毕生所学找到
    
    External (_SB_.PCI0.LPCB, DeviceObj)

    Scope (_SB.PCI0.LPCB)

修改成

    External (_SB_.PCI0.LPC, DeviceObj)

    Scope (_SB.PCI0.LPC)

4.处理 **SSDT-PMC**
没有就[下载](https://github.com/acidanthera/OpenCorePkg/tree/master/Docs/AcpiSamples/Source/SSDT-PMC.dsl)

    External (_SB_.PCI0.LPCB, DeviceObj)
    
    Scope (_SB.PCI0.LPCB)
 修改为

    ternal (_SB_.PCI0.LPC, DeviceObj) 

    Scope (_SB.PCI0.LPC) 
 5.编译
 用这个指令

    acpihelp.exe -o 文件名字
**把「文件名字」 依次换成 刚刚变出来的5个文件**
最后你需要确保 你可以看到5个以XXX.aml结尾的文件。

    现在，请新建一个文件夹，把文件放入，命名为「ACPI」替换在「最简EFI』文件夹里

## 三：配置OpenCoreCFG
[请看](https://post.smzdm.com/p/aqm8nxvx/)，这个部分这个作者写的好，请看他

以后会考虑自己写

## 四：驱动
将你刚才下载的各种驱动 XXX.kext 新建一个文件夹放在一起。然后命名为kexts

## 五：组装
将 **kexts文件夹** **ACPI** 放在「最简EFI里」

这个时候你的「最简EFI」里会有 图1.1[![xS2aDI.png](https://s1.ax1x.com/2022/09/17/xS2aDI.png)](https://imgse.com/i/xS2aDI) 1.2[![xS2hV0.png](https://s1.ax1x.com/2022/09/17/xS2hV0.png)](https://imgse.com/i/xS2hV0)

将你的「最简EFI」重命名为EFI
 
    休息下吧，看到这里
    
    辛苦啦
    
    这一步之后，就要正式开始安装了
# 肆、开始安装
## 一、写盘
用「写盘工具」将你下载映像写入U盘

~~如果你卡在Vailting 这个地方 跳过就好~~

对于小白：当你同时看到绿色的进度条和Skip这个单词时
直接点 **skip**

## 二、进入BIOS
### 以你的毕生所学，进入bios并且关闭
    没有的不管

    Fast Boot
    Secure Boot
    Serial/COM Port
    Parallel Port
    VT-d 
    CSM
    Thunderbolt（有些没有驱动）
    Intel SGX
    Intel Platform Trust
    CFG Lock(可以的话)
### 打开
    VT-x
    Above 4G decoding
    Hyper-Threading
    Execute Disable Bit
    EHCI/XHCI Hand-off
    OS type: other 
    UEFI Mode
    DVMT Pre-Allocated: 64MB
    SATA Mode: AHCI
## 三、Boot up
    从你的U盘启动

## 四、安装
请将安装程序调成你熟悉的语言，最好不要登陆Apple ID

如果你是在安装Catalina(10.15.x)之前的系统，请[参考](https://www.applex.net/threads/macos-mojave.93508/)

## 五、善后
现在，不出意外，你应该在系统里面了，

有部分网卡、声卡需要别的操作的，请按照对应的教程进行

# 伍、尾言
文章写得很赶，有些东西自己也不太会。希望大家有耐心慢慢搞。

苹果发布M1型片后，就不知道黑苹果还能活多久。且行且珍惜

如果你是vega8用户，又刚好会C++写驱动，可以带你去找找国外的进度

感谢那些曾经为黑苹果默默做出贡献的开发者！

此致

转载请注明出处，可以二创。

如果你在安装时遇到问题，可在飞机号：[@CharlesSu](https://t.me/Mistry_Rain)

所有的操作均来自互联网，遇到问题请你自己负责！

文章已授权 [Gloridust](https://gloridust.xyz/) [Rene](https://rene.wang/)发布


* * *
本文转载已经原作者[@CharlesSu](t.me/Mistry_Rain)同意，如二次转载请联系作者并标明出处。  
文章封面来源于网络。  
