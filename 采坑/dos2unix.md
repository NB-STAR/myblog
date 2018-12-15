因为工作需要，经常需要写dockerfile和docker-compose文件，写完以后往往会传到公司的gitlab上，需要用的时候拉下来。

但是，经常会遇到本来可以正常up起来的docker-compose文件重新pull下来以后就没法用了。

巨佬教了我一个方法：使用dos2unix，把pull下来的文件转一下格式。

命令很简单，eg：`dos2unix Dockerfile`