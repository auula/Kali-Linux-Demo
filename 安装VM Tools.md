<p align="center">
  <a  href="https://wpa.qq.com/msgrd?v=3&uin=2420498526&site=qq&menu=yes" target="_blank" >
   <img alt="codin"  height="200" width="200"src="https://q.qlogo.cn/headimg_dl?dst_uin=2420498526&spec=640&img_type=jpg" >
  </a>
</p>

安装VM Tools（传统版）
===========
>by：codin
>2018年5月6日16:11:59

安装命令:
---------
>1.挂载VM tools.iso

```
shell#: tar zxvf VMwareTools.tar.gz
shell#: ./VMware-install.pl
```
>一路yes！执行命令完成之后重启虚拟机

我安装时执行截图(传统方式)
--------------
![](https://github.com/coding1618/Kali-Linux-Demo/blob/master/img/2018-05-06_173349.png?raw=true'VMtools安装')


安装Open-VM-tools
=================
>传统的vmtools已经被抛弃，VMware Workstation自带的vmware-tools安装后仍然不能相互复制文件，现在建议使用Open-VM-tools。

修改源
------
```shell
vi /etc/apt/sources.list
#中科大更新源
deb http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
deb-src http://mirrors.ustc.edu.cn/kali/ kali-rolling main contrib non-free

#阿里云更新源
deb http://mirrors.aliyun.com/kali kali-rolling main non-free contrib 
deb-src http://mirrors.aliyun.com/kali kali-rolling main non-free contrib 
deb http://mirrors.aliyun.com/kali-security kali-rolling main contrib non-free

注意文件中的“kaili-rolling”

apt-get install open-vm-tools-desktop fuse

```
按提示安装后重启即可。
---------------------

>PS：可以通过系统编辑器来编辑源配置文件
![](https://github.com/coding1618/Kali-Linux-Demo/blob/master/img/2018-05-06_182132.png?raw=true'kali更新源')


安装成功后效果预览
------------------
![](https://github.com/coding1618/Kali-Linux-Demo/blob/master/img/2018-05-06_185130.png?raw=true'kalilinux')
