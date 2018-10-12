> **在配置uWSGI与Django的过程中，通过查询[uWSGI官方文档](https://uwsgi-docs.readthedocs.io/en/latest/tutorials/Django_and_nginx.html)照葫芦画瓢，但有一处笔误导致我这个菜鸡踩坑:**
![](img/201810121300.PNG)

>重启nginx提示:<br>
>*[emerg] open() "/etc/nginx/sites-enabled/mysite_nginx.conf" failed (2: No such file or directory) in /etc/nginx/nginx*<br>

>原来这里官方文档写错了，导致链接了不存在的文件。

> **在这里建立的软连接应该为：**
>`sudo ln -s ~/etc/nginx/sites-available/mysite_nginx.conf /etc/nginx/sites-enabled/`
