
# Basics of Daily Git Operation

## 1. Rules of git comment

- Step 1: Find issue number from issue tab
- Step 2: Add "[#51]" to the head of comment
- Step 3: Use simple brief desciption of submission

*Note: see below for example.*

> commit b42cee176eb4a7592c29d2c04fcee09b11e6be18 (HEAD -> main, origin/main, origin/HEAD)
>
> Author: Daniel Li <lida_mail@163.com>
>
> Date:   Fri Dec 23 14:17:57 2022 +0800
> 
>    [#51] Add wireless get/post RESTful API

## 2. GitHub SSH Clone project to local


SSH cloning project needs to configure SSH key, and SSH key needs to be configured on GitHub

SSH clone must be the owner or administrator of the item to be cloned, and SSH key must be added first, otherwise it cannot be cloned.

In SSH push, you do not need to enter the user name. If the password is set when configuring the SSH key, you need to enter the password. Otherwise, you do not need to enter the password directly.

### GitHub configuration local SSH key

**1、User setting key, mailbox**

You need to run the command to configure the local user name and mailbox. This can be real or fake.

>View Configuration
>
>git config --list
>
>View current status 
>
>git status 
>
>Configure key user name
>
>git config --global user.name "docker"
>
>Configure key mailbox
>
>git config --global user.email  "xxx@yeah.net"


**2、GitHub SSH Key configuration**

Check if it exists SSH Key

>cd ~/.ssh 
>
>ls

See if there is an id_ Rsa and id_ The rsa.pub file, if it exists, indicates that there is already an SSH key. If not, create a new SSH key.

**3、Create a new SSH key**

>$ ssh-keygen -t rsa -C “content neirong”
>
>-t ：密钥的类型
>
>-C : 用于识别密钥的注释
>
>-C 一般大家都写的是Email邮箱

然后会在 .ssh 目录生产两个文件：id_rsa和id_rsa.pub

id_rsa 文件是私有密钥，id_rsa.pub是公开密钥。

**4、获取ssh key公钥内容（id_rsa.pub）**

打开.ssh目录下的id_rsa.pub文件，复制里面的内容，或者直接执行命令查看

>cat ~/.ssh/id_rsa.pub

执行命令后，会出现公钥的大串字符，复制字符，然后在GitHub上配置密钥

**5、复制ssh key到github**

1、登陆到自己的gitbub,点击右上角用户头像的倒立小三角形。选择 settings

2、在左边点击SSH and GPG keys

3、点击右边的New SSH key 把复制的公钥文件复制到key选项框

[配置GitHub密钥](https://blog.csdn.net/qq_20663639/article/details/126284892)


**6、验证是否设置成功**

现在验证一下用手中的私有密钥与GitHub进行认证和通信

>ssh -T git@github.com


>The authenticity of host 'github.com (xx.xx.xx.xx)' can't be established.
>
>RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
>
>This key is not known by any other names
>
>Are you sure you want to continue connecting (yes/no/[fingerprint])? yes (这里输入yes)
>
>出现以下说明成功通信：
>
>Hi xxx! You've successfully authenticated, but GitHub does not provide shell access.


**7、git clone克隆GitHub项目到本地**


>git clone git@github.com:lida2003/SnapAirUnitTest.git

克隆GitHub上的项目到本地后，就可以对本地文件做编辑了

[获取GitHub项目SSH链接地址](https://blog.csdn.net/qq_20663639/article/details/126284892)


## 2.git提交步骤

[git提交步骤](https://blog.csdn.net/weixin_44933530/article/details/126149801)

1、同步远程仓库代码：git pull

提交代码第1步：git pull 同步远程仓库代码到本地

git add / git commit代码之前首先git pull，需先从服务器上面拉取代码，以防覆盖别人代码；如果有冲突，先备份自己的代码，git checkout下远程库里最新的的代码，将自己的代码合并进去，然后再提交代码

出现Already up-to-date代表本地代码已经更新到和远程仓库一致了。

第2步：查看当前状态：git status

提交代码第2步：git status 查看当前状态

当你忘记修改了哪些文件的时候可以使用 git status 来查看当前状态，红色的字体显示的就是你修改的文件。

第3步：提交代码到本地git缓存区：git add

提交代码第3步：git add . 或者 git add xxx

命令：git add 文件名1 文件名2 …

第4步：推送代码到本地git库：git commit

提交代码第4步：git commit -m “提交代码” 推送修改到本地git库中

命令：git commit 文件名 -m “提交代码备注”

第5步：提交本地代码到远程仓库：git push

提交代码第5步：git push <远程主机名> <远程分支名> 把当前提交到git本地仓库的代码推送到远程主机的某个远程分之上。

命令：git push

## 3.查看提交日志 git log

>git log

查看所有的提交记录

>git log -n 1

查看最近一条提交记录
