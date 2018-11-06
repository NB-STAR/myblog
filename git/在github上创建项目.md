### 安装git

- brew install git

### 创建ssh key、配置git

```
config --global user.name "odyssey"
config --global user.email "com.mark.fake@gmail.com"
```
ssh-keygen -t rsa -C "com.mark.fake@gmail.com"

- 终端查看.ssh/id_rsa.pub文件

`cat ~/.ssh/id_rsa.pub`

- 链接验证

`ssh -T git@github.com `

- 终端输出结果
```shell
The authenticity of host 'github.com (192.30.253.113)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
Hi NB-STAR! You've successfully authenticated, but GitHub does not provide shell access.
```
说明已经链接成功。

### 提交本地项目到GitHub

- 第一种：在git上创建后clone到本地

在github中创建一个项目，创建成功后，复制项目的地址。使用命令：`git clone 地址`

进入项目的目录，然后输入：

```shell
//文件添加到仓库（.代表提交所有文件）
git add .
//把文件提交到仓库
git commit -m "First Commit"
//上传到github
git push
```


- 第二种：本地创建后推送到github

_前提：在github上手动创建仓库。_

在本地按照如下的命令进行

```shell
mkdir myblog  
#如果是已存在的工程项目，则直接cd到项目根目录下，不需要新建。
cd myblog
#初始化本地仓库
git init 
#添加要push到远程仓库的文件或文件夹
git add xxx
#commit
git commit -am ‘first commit’
#建立远程仓库
git remote add origin https://github.com/xxx/myblog.git 
#将本地仓库push到远程仓库
git push -u origin master 
```


