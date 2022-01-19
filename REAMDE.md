# vmvare esxi 7.0u2 装macOs和android文档

## Mac Os系统安装

**VMware esxi不支持macOS和Mac OS X，需要解锁**

- 解锁工具
  - [esxi-unlocker-master.zip](esxi-unlocker-master.zip)
  - vmvare esxi 开启ssh
  - scp esxi-unlocker-master.zip到 vmvare esxi 中
     - scp root@ip:/path
  - ssh 登录到vmvare esxi中
     - ssh工具登录
     - 执行sh esxi-install.sh
     - reboot

- macOS ISO镜像 懒人版即可
  - boot启动
  - 磁盘工具 抺掉磁盘 相当于分区
  - 安装镜像
  - ...

- 屏幕共享
  - 开启 设置密码
  - windows利用vnc软件登录[http://www.tightvnc.com/download.php](http://www.tightvnc.com/download.php)
  

## Android 系统

- android ISO镜像
  - boot 启动
  - 分区
  - 安装镜像
  - ...


- 开启ui界面启动
    - 进入控制台执行
        - mkdir /mnt/sda
        - mount /dev/block/sda1 /mnt/sda
        - vi /mnt/sda/grub/menu.lst
            - quiet -> nomodeset xforcevesa

- 调试
   - 连接
        - adb connect ip:5555
   - 操作
        - 利用adb进行一系操作
        - adb install 安装apk或xapk
        - adb push 上传文件到android
        - adb pull 拉取文件到本地


