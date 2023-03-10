# Git初始教程

## 1.Git是什么

摘取菜鸟教程的一段话*Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。*

*Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。*

*Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。*

简单来说Git就是一种开源的分布式版本控制系统，可以协调控制各个分支间的差异

***注意：本教程只教命令行的Git教程如果你想看关于Git GUI的教程请查看[Git可视化极简易教程 — Git GUI使用方法 | 菜鸟教程 (runoob.com)](https://www.runoob.com/w3cnote/git-gui-window.html)本教程不对GUI负责或者你可以补充本教程缺失的内容***

### 1.1为什么要使用Git

Git是一种快捷的拉取和推送远程仓库的一种选择，你也可以使用其他的拉取和推送的软件,但是我还是推介你使用Git因为他足够便捷和已经在大部分IDE中拥有其快捷的提交和推送。


接下来将介绍怎么[初始化Git](#初始化)和使用Git如果已经知道这些知识那么请跳转到[克隆远程仓库和拉取和推送](#克隆远程仓库和拉取和推送)

## 2.本地仓库

### 2.1安装Git

Git是需要在本地进行安装的安装的官网为:
> [Git (git-scm.com)](https://git-scm.com/)

详细的安装选项可以参考这篇文章：[(26条消息) Git 详细安装教程（详解 Git 安装过程的每一个步骤）_mukes的博客-CSDN博客_git安装](https://blog.csdn.net/mukes/article/details/115693833)这篇文章可以辅助你知道怎么在安装中选择应该的选项。

### 2.2注册本地的账号和邮箱

使用Git之前都需要创建自己的账号和邮箱以此来知道是谁推送了最新分支。以我的D盘为例子在D盘中的任意空白位置点击鼠标右键选择Git Bash Here或者直接在桌面选择Git Bash如果没有GitBash,那么就在自己Git的安装目录中打开并选择git-bash.exe.

以下以我自己的安装(D:\Git)目录为例：

![image-20221028101936567](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028101936567.png)

在安装目录下面选择git-bash.exe后会探出一个git的小窗，git小窗的操作类似于vim所以是不能使用Windows上的快捷键的否则可能会输入的乱码行为.

进入小窗后先进行账号的初始化命令为**git config --选项 信息 “(输入基本信息)”**

具体请参考：[git config命令使用 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/76467410 )

注册的账号名字命令为：

```tex
git config --global user.name "(输入你的名字)"
```

例如我注册一个为QuiMir的名字

![image-20221028102657429](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028102657429.png)

如何查看是否输入成功输入命令

```tex
git config --global user.name
```

![image-20221028102813034](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028102813034.png)

从控制台中可见我已经输入了名字为QuiMir的

而输入邮箱和注册账号同理：

~~~tex
git config --global user.email "(输入你的邮箱)"
~~~

![image-20221028103014726](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028103014726.png)

查看邮箱输入和查看名字输入同理

```
git config --global user.email
```

这里就不做测试了，这样我们就完成了账号和邮箱的本地初始化。

**注：以上的操作只是对本地Git仓库进行了账号和邮箱初始化如果要进行远程的推送还是需要登录远程服务器的账号和密码，在推送时以远程服务器的为准**

#### 2.1.1本地仓库的初始化

初始化的命令很简单

```tex
git init
```

我以下面文件夹为例子，你也可以打开自己随便一个文件夹为初始化仓库的文件夹

> D:\Dev-Text

![image-20221028103737010](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028103737010.png)

这样我们就初始化了一个Git的本地仓库同时文件夹中会创建一个.git文件他就是我们存储本地仓库的地方

![image-20221028103848761](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028103848761.png)

如果没有看见这个文件夹,那么请参考[怎么显示win10系统隐藏文件夹 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/259761453)或者[Win11如何查看隐藏文件？Win11查看隐藏文件的方法_当客下载站 (downkr.com)](https://www.downkr.com/news/228630_1.html)

#### 2.1.2查看本地仓库的状态

命令也是很简单

```tex
git status
```

详细可查看：[git status命令 - Git教程 (yiibai.com)](https://www.yiibai.com/git/git_status.html)

因为我本文件夹中有除了.git之外的其他文件那么输入他之后就会有以下的提示出来

![image-20221028104432415](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028104432415.png)

这写红色的都是没有添加和提交的文件也就是需要我们进行添加到本地的暂存区

#### 2.1.3添加到本地暂存区

命令为

```tex
git add (提交的文件/提交的文件夹)
```

详细可参考[git add 命令 | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-add.html)

例如我要添加OP.dev文件那么只需要写

![image-20221028104656014](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028104656014.png)

添加完之后我们再通过查看本地仓库的状态

![image-20221028104755822](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028104755822.png)

已经看见OP.dev是新的文件了这时候提示我们需要提交他到本地暂存区

同时我们也可以写以下的命令

```tex
git add .
```

将本文件夹下的全部文件都添加到本地暂存区

![image-20221028104958554](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028104958554.png)

#### 2.1.4提交到本地暂存区

Git的提交到本地暂存区的命令为：

```tex
git commit (附加命令) "(提交名字)"
```

详细可参考：[git commit 命令 | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-commit.html)

一般来说在不加附加命令的时候在git-bash下输入git commit命令就会进入vim一样控制面板的模式，如果已经知道vim怎么操作的可以使用该命令或者可以参考这篇文章[vim命令大全 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/61515833).

我一般推荐使用的命令是

```tex
git commmit -m "(对提交内容的描述)"
```

-m可以不让我们进入vim的输入模式而直接进行提交。

例如我想提交到本地暂存区并且提交的时候不使用vim的操作模式而且提交的名字为First那么就输入

![image-20221028105632622](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028105632622.png)

![image-20221028105643944](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028105643944.png)

并且输入git status查看状态时没有其他选项的时候就可以进行提交到本地仓库了

同时如果你想添加和提交一起完成那么就可以输入以下命令

```tex
git commit -am "(对提交内容的描述)"
```

这样提交和添加都会一起到暂存区，但是我不推荐你这样做因为这就意味着你,git下面的整个文件夹都会被进行提交和添加。

##### 2.1.4.1Git标签

参考来自：[Git基础 - git tag 一文真正的搞懂git标签的使用_NorthCastle的博客-CSDN博客_git tag](https://blog.csdn.net/qq_39505245/article/details/124705850)

**Git的标签准确讲来说就是给commit起变名。**

Git起标签的命令分为两种：

###### *2.1.4.1.1轻量化命令*：

```
git tag 标签名 提交版本
```

**提交版本也就是commit后面那一串哈希码值**，如果不写明提交版本那么就默认为当前版本

例如以

> [组织介绍: 本仓库的目的是为了介绍本组织还有上传规定和如何上传本组织和Git的相关事项 (gitee.com)](https://gitee.com/NLLaboratory/organization-introduction)

该仓库为例子

![image-20221101210715089](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101210715089.png)

我想以当前提交的commit也就是（093eb925bfa64cc23f04d902e94559839417b7b0）写一个标签那么可以写成

```
git tag v1.2
```

或者

```
git tag v1.2 093eb925bfa64cc23f04d902e94559839417b7b0
```

![image-20221101211010502](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101211010502.png)

###### 2.1.4.1.3*附加命令*

```
git tag -a 标签名字 提交版本 -m 附加信息
```

>说明：
>-a : 理解为 annotated 的首字符，表示 附注标签
>-m : 指定附注信息
>git tag -a 标签名称 -m 附注信息 ：直接给当前的提交版本创建一个 【附注标签】
>git tag -a 标签名称 提交版本号 -m 附注信息 ：给指定的提交版本创建一个【附注标签】

比如说我想给

> 970afb8451059badfe18be8cf3c68a787c50eb77

这串提交版本写提交版本是v1.3并且附加信息写修改了部分bug

那么我们就输入

```
git tag -a v1.3 970afb8451059badfe18be8cf3c68a787c50eb77 -m "修复了部分bug"
```

![image-20221101211732234](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101211732234.png)

可见我们已经为其打上一个标签了。

###### 2.1.4.2查看本分支的标签

在上面中我们已经介绍了两种打标签的方式，那么我们如何查看当前分支下现有的标签，可以通过以下命令：

```
git tag
```

还是以仓库

> [南宁理工学院创新实践基地/组织介绍 - 码云 - 开源中国 (gitee.com)](https://gitee.com/NLLaboratory/organization-introduction/tree/master)

为例子

通过输入git tag可见

![image-20221101220633731](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101220633731.png)

那么我们在已知标签名字的仓库下如何查看标签的内容可以通过以下命令：

```
git show 标签的名字
```

而对于轻量化和附加命令的查看详细该命令显示的是不一样的

![image-20221101220806904](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101220806904.png)

在轻量化提交命令上只会显示版本提交的基本信息。

![image-20221101220855788](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101220855788.png)

而附加命令的查看会将写的附加命令和版本基本信息都一起提交。

###### 2.1.4.1.4删除命令

如果我们输入了一个错误的标签想要删除怎么办？

那么就输入以下命令：

```
git tag -d 标签名字
```

![image-20221101211852671](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221101211852671.png)

可见我们已经将v1.2标签删除了。

###### 2.1.4.1.5提交到远程仓库

如何提交标签到远程仓库？

**标签提交到远程仓库不和推送到远程仓库一起需要单独提交**

标签远程提交的命令为：

```
git push 远程仓库的名字 标签名字
git push 远程仓库的名字 --tags
```

说明 ：
`git push 远程仓库的名字 标签名称` : 将指定的标签上传到远程仓库
`git push 远程仓库的名字 --tags` : 将所有不在远程仓库中的标签上传到远程仓库

本部分不做演示详细请看：

[Git基础 - git tag 一文真正的搞懂git标签的使用_NorthCastle的博客-CSDN博客_git tag](https://blog.csdn.net/qq_39505245/article/details/124705850)

### 2.2Git分支

在介绍Git的提交之前我们先介绍Git的分支系统,**在进行Git的分支之前请确保你至少已经进行了一次暂存区的提交**否则在暂存区没有数据的时候Git是不允许你建立新的分支。

详细可以参考这篇文章:[Git 分支管理 | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-branch.html)

*Git建立新分支的基本逻辑是复制一份主分支的副本来建立新的分支*

建立新分支

建立新分支的基本命令是

```tex
git branch "(分支名字)"
```

我想建立一个名字为main的新的分支那么就只需要输入git branch "main"

![image-20221028110554007](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028110554007.png)

Git的查看现有分支的命令是：

```tex
git branch
```

![image-20221028110807934](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028110807934.png)

关于git branch命令详细可以查看[git branch命令 - Git教程 (yiibai.com)](https://www.yiibai.com/git/git_branch.html)

Git在初始化的时候默认给你建立一个master的主分支如果我们想要切换main为主分支怎么办

那么我们就需要使用：

```tex
git checkout "(分支的名字)"
```

这个命令可以使选定的分支名字变成主分支

![image-20221028111024697](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028111024697.png)

这样main就成为了我们的主分支

那么问题来了我们想要删除一个分支怎么办,我们就需要使用:

```tex
git breach -d "(分支名字)"
```

关于*git breach*命令可以参考这篇文章本文:[git branch命令 - Git教程 (yiibai.com)](https://www.yiibai.com/git/git_branch.html)本文不对git branch命令做更多论述

例如我们新建立一个分支boy作为测试

![image-20221028111328349](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028111328349.png)

然后使用git breach -d "boy"

![image-20221028111400026](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028111400026.png)

可见已经完全删除了boy的分支。

假设我们需要将一个分支合并到当前分支怎么办那么我们就需要使用

```tex
git merge "(分支名字)"
```

我们在main分支中创建一个README.md的文件并且在其中写上Hello,World

![image-20221028111847371](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028111847371.png)

![image-20221028111859596](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028111859596.png)

我们再切换回master分支我们查看文件夹发现README没了那么我们需要将main中的README添加到master主分支中

![image-20221028112053446](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028112053446.png)

输入后发现他将main中的README合并过来了

关于git merge的详细可以勘察[Git merge 合并分支——迹忆客 (jiyik.com)](https://www.jiyik.com/w/git/git-merge)

那么接下来就到我们的远程推送和远程拉取了

###  2.3远程推送和远程拉取

#### 2.3.1远程推送

可以参考本篇文章[(16条消息) Git--建立和解除与远程仓库的关联_Jinphy的博客-CSDN博客_git解绑远程仓库](https://blog.csdn.net/Jinphy/article/details/81206304)

首先我们要已经有一个已经提交到本地暂存区的数据然后使用以下命令查看是否已经链接了远程仓库

```tex
git remote -v
```

![image-20221028113109754](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028113109754.png)

添加远程仓库的命令为

```tex
git remote add (远程主机名) (远程仓库地址)
```

以我的仓库[再赢亿把就睡觉/测试Git推送 (gitee.com)](https://gitee.com/QuiMIr/Test-git-push)

输入git remote add origin https://gitee.com/QuiMIr/Test-git-push.git

![image-20221028113336474](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028113336474.png)

可以看到我已经建立了链接那么如何推送到远程仓库那么就需要命令

```tex
git push (推送方式) (远程主机名) (本地分支)
```

完整的推送方式可以参看这篇文章:[git push 命令 | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-push.html)

我们这里使用git push -u origin "master"的方式进行推送

![image-20221028113727781](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028113727781.png)

一般来说都需要输入账号和密码的账号和密码按照远程仓库的注册和登录为准

如果我们想要解除这个推送怎么办可以使用以下命令

```tex
git remote rm (远程主机名)
```

![image-20221028114015223](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028114015223.png)

可见没有了该推送分支了。

#### 2.3.2远程拉取

还是以Dev-Text为例

**拉取命令在Git上面更像是同步也就是拉取最新的数据**.假如我在README.md里面新添加了一行话而这行话本地没有如果本地的仓库推送到远程仓库时就会出现本地仓库于远程仓库冲突不允许推送的提示

例如:

![image-20221028114541296](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028114541296.png)

那么这时候我们就需要使用以下命令

```tex
git pull (远程主机名) (远程分支)
```

![image-20221028114903272](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028114903272.png)

这时候我们就可以看到本地的READEME.md就增加了一段话我们再在本地添加一段话再推送

![image-20221028115102823](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028115102823.png)

可见已经成功了本地也已经提交.

### 2.4Git查看提交历史

Git的查看历史记录的命令为：

```
git log
```

详细可参考：[Git 查看提交历史 | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-commit-history.html)

以仓库为

> https://gitee.com/NLLaboratory/lab-notes.git

为例子:

![image-20221030184940806](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221030184940806.png)

我们在git-bash命令行中输入git log会出现提交的账号,提交的邮箱,提交的编号和提交的时间这样就可以知道每次是谁提交的了.

#### 2.4.1代码回滚

Git的查看提交历史最重要的是给我们提供了一种可以回退到以前代码的手段.比如说我提交了一份最新的代码但是在运行的时候出现了问题而我上一次的代码在运行的时候没有出现问题那么我们就可以使用Git的命令让我们回退到上一次的提交.

代码回滚的命令为:

```
git reset --hard (提交的编号)  
```

注:提交的编号为commit后面那一串

详细可参考:[git reset --hard 操作后的数据恢复 - Chris-dc - 博客园 (cnblogs.com)](https://www.cnblogs.com/dongcanliang/p/11162235.html)

例如:我想回到上一个版本那我就输入git reset --hard 98ff9d6a160a091088e2bcced86b3cce3e543611

![image-20221030192316377](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221030192316377.png)

可见我们已经回到上一个版本了

我们再次查看现在的提交历史

![image-20221030192606822](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221030192606822.png)

可见回到前面一个版本之后之前那个版本就已经没有了所以**除非你记得这一次提交的编号代码否则在回档到上一次的时候会没有上一次书写的代码**

## 3.远程仓库的克隆和推送

一般来说我们都是克隆别人的仓库来使用和更改那么怎么使用克隆别人的远程仓库呢可以输入以下命令:

```tex
git clone (克隆的远程仓库)
```

以该仓库为例

> https://gitee.com/NLLaboratory/lab-notes.git

我们需要一个文件夹来存放，例如我是以D:\Git-Text为存放的路径可以随自己而定

![image-20221028120100226](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028120100226.png)

我们已经克隆完，克隆完的文件夹一般都会把其的.git全部克隆下来所以就不需要进行初始化，我们想要在内容上进行更改，只需要进行[提交](#提交到本地暂存区)和[添加](#添加到本地暂存区)。

如果不知道已经链接远程仓库的名字，我们可以通过git remote -v命令查看已经有的远程仓库。

![image-20221028120610652](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028120610652.png)

可见我们远程仓库的地址和远程仓库的名字

注意：**每次提交前都需要pull一遍，因为你不知道别人是否已经在你之前提交过而你提交不能通过**

![image-20221028120847266](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20221028120847266.png)

每次提交之前请确保已经完成了[提交](#提交到本地暂存区)的工作，这样我们就已经完成了对于远程仓库的拉取和推送。

详细可以查看：[Git 远程仓库(Github) | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-remote-repo.html)