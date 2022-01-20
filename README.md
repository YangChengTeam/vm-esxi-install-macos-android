# vmvare esxi 7.0u2 装macOs和android文档

## MacOs系统安装

**VMware esxi不支持macOS和Mac OS X，需要解锁**

- 解锁
  - 下载工具[esxi-unlocker-master.zip](esxi-unlocker-master.zip)
  - vmvare esxi 开启ssh
  - scp esxi-unlocker-master.zip到 vmvare esxi 中
     - scp root@ip:/path
  - ssh 登录到vmvare esxi中
     - ssh工具登录
     - 执行sh esxi-install.sh
     - reboot

- 安装
  - 下载macOS ISO镜像 懒人版即可
  - boot启动
  - 磁盘工具 抺掉磁盘 相当于分区
  - 根据界面操作
  - ...

- 屏幕控制
  - 开启 设置密码
  - windows利用vnc软件登录[http://www.tightvnc.com/download.php](http://www.tightvnc.com/download.php)
  - 或者[https://www.realvnc.com/en/connect/download/viewer/](https://www.realvnc.com/en/connect/download/viewer/)

## Android 系统安装

- 安装
  - 下载android镜像 
  - boot 启动
  - 分区
  - 根据界面操作
  - ...

- 启动方式修改
    - 进入控制台执行
        - mkdir /mnt/sda
        - mount /dev/block/sda1 /mnt/sda
        - vi /mnt/sda/grub/menu.lst
            - quiet -> nomodeset xforcevesa

- 屏幕控制
   - scrcpy
     - [https://github.com/Genymobile/scrcpy/releases](https://github.com/Genymobile/scrcpy/releases)
     - adb connect ip:5555

