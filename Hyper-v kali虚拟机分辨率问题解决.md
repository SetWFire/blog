关键点：**虚拟机硬件设置中不要添加RemoteFX！！**
>在kali里面的`/etc/default/grub`中找到`GRUB_CMDLINE_LINUX_DEFAULT`,修改为：
>`GRUB_CMDLINE_LINUX_DEFAULT="quiet splash video=hyperv_fb:1920x1020"`（或者其它分辨率）
>运行`sudo update-grub`后重启即可。
>
>事实上，RemoteFX硬件的载入会导致hyperv_fb模块无法加载。原因不详，官方有个BUG报告，但最后的解决方案（安装udev）没有效果。
>看来Hyper还是为win设计的，Linux的支持并不全面。
