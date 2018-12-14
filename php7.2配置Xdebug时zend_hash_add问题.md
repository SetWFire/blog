在kali上面配置php的Xdebug扩展时，先安装

`apt-get install php-xdebug`

然后若在php7.2中配置xdebug，无论如何都会出现错误：

`undefined symbol: zend_hash_add in Unknown on line 0`

正确做法为在php7.3中配置，配置文件添加：

>zend_extension=xdebug<br>
>[xdebug]<br>
>;相关设置<br>
