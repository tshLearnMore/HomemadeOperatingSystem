# HomemadeOperatingSystem
1. 以前读书的时候学了很多计算机原理相关的书，有编译、操作系统、体系结构、算法等，但是从没想过自己写操作系统，一是觉得无从下手，二是觉得很难。自从看见30天自制操作系统后，发现并不是难么困难，所有就想实现一个
2. 根据30天自制操作系统这本书来编写

# 如何开发操作系统
1. 在windows(或其他)系统上编写源代码
2. 用C语言编译器编译源代码，生成机器语言文件
3. 对机器语言文件进行加工，生成软盘映像文件
4. 将映像文件写入磁盘，制作成含操作系统的启动盘

# 启动方式

## 1. 软盘或者U盘启动

## 2. QEMU启动

1. 新建一个目录（以helloos0为例），目录和z_tools平级，然后将z_new_w文件夹中!con_9x.bat和!con_nt.bat复制到helloos0中
2. 新建一个run.bat文件输入以下内容
```
copy helloos.img ..\z_tools\qemu\fdimage0.bin
..\z_tools\make.exe	-C ../z_tools/qemu
```
3. 新建一个install.bat，输入以下内容
```
..\z_tools\imgtol.com w a: helloos.img
```
4. 将projects\01_day\helloos0\helloos.img拷贝到helloos0目录中。
5. 进入helloos0目录，双击!cons_nt.bat后然后输入run即可
