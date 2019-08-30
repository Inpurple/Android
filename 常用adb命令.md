ADB常用的几个命令
1. 查看设备

adb devices

查看当前连接的设备, 连接到计算机的android设备或者模拟器将会列出显示

2. 安装软件

adb install [-r] [-s] <file>

将指定的apk文件安装到设备上.

－r  强制安装（在某些情况下可以已有些应用程序在运行或不可写，可加上此参数强制安装）

－s  将apk文件安装在SD-Card

3. 卸载软件

adb uninstall [-k] <软件名>

如果加 -k 参数,为卸载软件但是保留配置和缓存文件.

4. 从电脑上发送文件到设备

adb push <本地路径> <远程路径>

用push命令可以把本机电脑上的文件或者文件夹复制到设备(手机)

例：传送文件到手机中,如:

adb push recovery.img /sdcard/recovery.img

将本地目录中的 recovery.img文件传送手机的 SD卡中并取同样的文件名

5. 从设备上下载文件到电脑

adb pull <远程路径> <本地路径>

用pull命令可以把设备(手机)上的文件或者文件夹复制到本机电脑

6. 显示帮助信息

adb help

显示帮助信息

7. 显示ADB命令版本号

<b>adb version</b>

8. 启动计算机adb 服务进程

adb start-server

也可以直接使用adb devices命令时自动开启

9. 关闭计算机adb 服务进程

adb kill-server

可以关闭adb服务进程

10. 重启设备

adb reboot [bootloader|recovery]

adb reboot-bootloader

重启有三种方式

1）直接重启设备回到使用界面adb reboot即可；

2）重启设备到bootloader引导模式：adb reboot-bootloader或adb reboot bootloader

3）重启到recovery刷机模式：adb reboot recovery

11. 返回设备状态

adb get-state

返回设备状态，有三种结果：关机，引导模式，设备在线

12. 返回设备序列号

adb get-serialno

13.查看wifi密码：cat 空格/data/misc/wifi/*.conf

　　
