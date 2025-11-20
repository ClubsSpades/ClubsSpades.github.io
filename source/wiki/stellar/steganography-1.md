---
wiki: hexo-stellar 
title: 隐写相关（一）
tags: [MISC,Stegano]
excerpt: 遇到新的/不记得的就更新
---

## NTFS隐写
> NTFS文件系统时windows NT内核系列操作系统支持的、专门为网络和磁盘配额的，文件加密等管理安全特性设计的磁盘格式。NTFS比FAT文件系统更加稳定，更能也更为强大。

NTFS数据流文件也被称为 Alternate data streams，简称ADS，是NTFS文件系统的一个特性之一，允许单独的数据流文件存在，同时也允许文件附着多个数据流，除了主文件流之外还允许许多非主文件流寄生在主文件流中，使用资源派生的方式来维持与文件的相关信息，并且这些寄生的数据流文件我们使用资源管理器无法看到。

{% icon solar:planet-bold-duotone %} 交换数据流介绍:
Windows NTFS文件系统的交换数据流（Alternate Data Steams, ADS）可以追溯到Windows NT3.1，为了满足Windows系统和苹果HFS（Hierachical File System） 系统的交互需求诞生了交换数据流。NTFS使用的交换数据流来存储文件的相关元数据，包括安全信息、原作者以及其他元数据。
对于隐藏文件，Windows NTFS中的交换数据流事一种简单并且隐蔽的方式。
{% box %}
dir /r  #即可查看当前目录是否有ntfs隐写的文件
{% endbox %}

然后用工具**ntfsstreamseditor.exe**打开所在文件夹,即可导出隐藏的文件