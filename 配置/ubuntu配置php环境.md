##ubuntu 16.04 LTS下php环境配置

###安装apache2
`sudo apt-get install apache2`

安装完成之后使用service apache2 status查看apahce2的状态，使用service apache2 restart重启apache2。

###安装php7.0
`sudo apt-get install php7.0`

安装完成之后可以通过php -v测试环境是否配置正确，或者通过`sudo nano /var/www/html/testphp.php`命令创建`testphp.php`文件,浏览器输入[http://localhost/testphp.php](http://localhost/testphp.php)进行访问，如果访问正常，则表示php安装成功。

安装mysql
`sudo apt-get install mysql-server`

安装过程中记住自己设置的密码。使用`mysql -u root -p`命令，然后输入自己的密码进行数据库登录。

安装phpmyadmin

参考资料：https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-phpmyadmin-on-ubuntu-16-04

`sudo apt-get install phpmyadmin php-mbstring php-gettext`，安装的过程中选择apache2。

安装完成之后使用如下两个命令修改支持模块:

    sudo phpenmod mcrypt
    sudo phpenmod mbstring
    
修改完成之后`sudo systemctl restart apache2`重启apache2服务器。在浏览器输入[http://localhost/phpmyadmin/](http://localhost/phpmyadmin/)，进入熟悉的页面。一切OK。

phpstorm安装

官方下载地址：https://www.jetbrains.com/phpstorm/download/#section=linux-version

安装包下载完成之后，提取到你想要安装的位置，然后进入bin目录，输入./phpstorm.sh打开应用。

破解：在注册的时候选择License server填写http://idea.qinxi1992.cn/即可。如果不可用，就打开该页面，作者在页面中有最新破解server链接的说明。向作者致敬。