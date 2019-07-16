# Remote-Reposity
### *github远程仓库的使用

### 一.创建一个仓库：

#### 1.Reposity---new--输入仓库名称（此处我输入的是Remote-Reposity）与描述信息

#### 2.在桌面建立与仓库同名的文件夹，该文件夹中含有相关文件，进入该文件夹，右键--> Git Bash Here  ,启动窗口

#### 3.检测远程仓库与本地仓库是否有建立连接：输入 git remote -v，如果没有东西显示，则表示没有建立连接。

#### 4.添加连接：

#### git remote add origin https://github.com/EvanismYu/Remote-Reposity.git (此处的EvanismYu是我的用户名)

#### 5.再次输入git remote -v，回车，此时就能发现有连接了

#### 6.将仓库中的文件推送到远程，输入git push origin master,回车，此时回到GitHub中的仓库，就能发现已经成功了

### *将GitHub中的文件克隆到本地：

### git clone https://github.com/EvanismYu/Remote-Reposity.git

### *在本地修改文件之后

#### 1. 添加文件查看状态

实时的查看工作状态

```shell
git status
```

可见,此时git发现有一个新文件,但并没有把此文件纳入管理.

如果文件修改了与版本库不一样,会提示,要不用commit提交更新版本

或者用版本库中的代码覆盖工作区

```shell
git checkout -- 文件名
```



#### 2. 将文件提交暂存区

```shell
git add index.html
```

可以通过下面命令将提交暂存区的文件删除

```shell
git rm --cached README.md
```



#### 3. 将暂存区的代码提交版本库

```shell
git commit -m "备注信息"
```



尝试修改文件,查询状态重新操作2,3,4步



#### 4.快速将修改后的代码提交版本库

这种简写的方式只针对修改文件

```shell
git commit -a -m "备注信息"
```

也可以如下写法

```js
git commit -am "备注信息"
```

### 远程操作

##### 1 查看远程仓库的名字

```shell
git remote
```



##### 2 查看远程仓库的关联

```shell
git remote -v
```



##### 3 代码推送远程

```shell
git push origin master
```



##### 在这里介绍一下HTTPS和SSH:
#####  HTTPS:（全称：Hyper Text Transfer Protocol over Secure Socket Layer 或 Hypertext Transfer Protocol Secure，超文本传输安全协议），是以安全为目标的HTTP通道，简单讲是HTTP的安全版。

##### SSH: Secure Shell 的缩写，由 IETF 的网络小组（Network Working Group）所制定；SSH 为建立在应用层基础上的安全协议。SSH 是目前较可靠，专为远程登录会话和其他网络服务提供安全性的协议。利用 SSH 协议可以有效防止远程管理过程中的信息泄露问题。