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
```
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

```
//文件添加到仓库（.代表提交所有文件）
git add .
//把文件提交到仓库
git commit -m "First Commit"
//上传到github
git push
```


- 第二种：本地创建后推送到github



