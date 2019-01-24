直接在ubuntu16中使用 `apt install pyhon-pip`

出现了这样几条警告

```shell
Do you want to continue? [Y/n] y
perl: warning: Setting locale failed.
perl: warning: Please check that your locale settings:
	LANGUAGE = "en_US:",
	LC_ALL = (unset),
	LC_CTYPE = "zh_CN.UTF-8",
	LANG = "en_US.UTF-8"
```

没有管，继续安装，貌似也没有什么问题，用 `pip install docker-compose`

问题来了，报了这个错误

```shell
Traceback (most recent call last):
  File "/usr/bin/pip", line 11, in <module>
    sys.exit(main())
  File "/usr/lib/python2.7/dist-packages/pip/__init__.py", line 215, in main
    locale.setlocale(locale.LC_ALL, '')
  File "/usr/lib/python2.7/locale.py", line 581, in setlocale
    return _setlocale(category, locale)
locale.Error: unsupported locale setting
```

上网搜了一下，可能是pip安装的有问题，有两种方法解决，一种是修改python2.7的文件，还有一种是重新安装合适的pip版本。我选择第二种了，第一种我也试过，但是当时没保存网页，所以，不想再去找一遍了。

第二种方法是：

```shell
wget https://bootstrap.pypa.io/get-pip.py //下载pip安装脚本
python get-pip.py
```

再执行 `pip install docker-compose`，报错！ emmm

```shell
bash: /usr/bin/pip: No such file or directory
```

找一下pip装哪去了，`whereis pip`

```shell
pip: /usr/local/bin/pip /usr/local/bin/pip2.7
```

那就搞个软连接吧 `ln -s /usr/local/bin/pip /usr/bin/`

再次执行`pip install docker-compose`，ok了。

