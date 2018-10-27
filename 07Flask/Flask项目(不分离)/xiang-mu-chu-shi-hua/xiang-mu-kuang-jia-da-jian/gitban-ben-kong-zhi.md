# 使用 GIT 管理源代码

## 本地提交

- 初始化 git

```
$ cd [项目目录]
$ git init
```

- 配置当前项目git提交信息(可省略此步，如不配置则使用全局配置)

```bash
git config user.name XXX
git config user.email XXX@xxx.com
```

- 添加忽略文件

```bash
$ touch .gitignore
```

- 设置忽略文件内容(后续根据需要再添加)

```bash
.idea
*.py[cod]
```

- 添加所有文件到暂存区

```bash
$ git add .
```

- 提交到本地仓库并填写注释

```bash
$ git commit -m'第一次提交'
```

- 让 Pycharm 管理当前项目的 git

![](/assets/将git注册到Settings中.png)


## 远程提交

使用码云 https://gitee.com/ 作为在线 git 源代码仓库，免费注册账号

- 在码云上创建项目：

![](/assets/码云创建项目.png)

- 创建完成之后，将已有项目上传到码云：

![](/assets/将已有项目上传到码云.png)


###  上传项目到码云
#### 方式1：使用命令行的形式将项目上传到码云

```bash
$ cd 项目根目录
$ git remote add origin 仓库地址
$ git push -u origin master
```

#### 方式2：使用Pycharm将项目上传到码云

- 拷贝地址

![](/assets/码云项目地址.png)

- 添加远程地址

![](/assets/添加远程地址1.png)

- 输入远程地址

![](/assets/输入远程地址.png)

- 输入码云的账号和密码并点击`OK`

![](/assets/输入码云的账号和密码.png)

- 选择菜单中的 `VCS` -> `Git` -> `Push`

![](/assets/使用Pycharm将项目Push到远程.png)

- Push 成功之后 Pycharm 弹出的提示

![](/assets/push_successful.png)

> 去码云上刷新当前项目查看Push结果



## 回滚代码

- 回滚到上一版本

```bash
$ git reset --hard HEAD~1
```

- 查看所有提交版本记录

```
$ git reflog
```

- 回到指定版本

```bash
$ git reset --hard 提交id
```




