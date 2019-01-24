想从github上下载单个文件，直接用了 `curl -O https://github.com/bozhu/NSA-ciphers/blob/master/simon.py`

打开一看，这是把整个网页保存下来了，那这个就不对了，从网上搜了以下，要点击项目右上角的raw，这样就是单纯的只有文件本身。使用 `curl -O https://raw.githubusercontent.com/bozhu/NSA-ciphers/master/simon.py`