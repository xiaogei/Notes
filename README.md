# Notes
学习笔记

首先感谢lean大的源代码：https://github.com/coolsnowwolf/lede

这里记录些，完全小白在编译openwrt的过程中学到的知识

先是整个的流程复述一遍

一开始，我给自己电脑装了VirtualBox，但是安装好Ubuntu系统后，发现无法获取IP，所以我把虚拟机换成了VMware，OK!成功解决。
系统我是按照lean大的要求，用了sever版的Ubuntu 14.04.6 LTS 64

接下来，就按照lean大写的内容，一条一条复制进去，切记！如果有的浏览器自带自动翻译页面的，记得关闭，不然会出现错误。

还有就是记得装python 3.5，sudo apt-get install python3.5， 不然会出错

文件夹回退 cd ../

查看文件夹 ls

返回 z 或 ctrl+c

删除文件夹 rm -rf lede/

如果要编译别的软件进去，那就再下载好源代码后

cd lede/package/lean/  

git clone https://github.com/jerrykuku/lua-maxminddb.git  #git lua-maxminddb 依赖

git clone https://github.com/jerrykuku/luci-app-vssr.git

cd ../

cd ../

./scripts/feeds update -a

./scripts/feeds install -a

make menuconfig

make -j1 V=s

大概就这样吧，记录下，免得我忘记了。
