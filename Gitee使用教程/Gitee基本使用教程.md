# Gitee基本使用教程

## 本教程面向的对象

这个教程主要面对的是不会使用Gitee/Github/Gitlab等一些开放平台的同学，如果你会使用以上的任何一个开放平台但是不会写markdown或者Git的话那么请看[markdown教程](./markdown教程.md)或者[Git初始教程](./Git初始教程.md)。本文的文本可能有一些错误如果发现错误的地方请打issues笔者都会看，那么我们就来看看Gitee是什么和怎么用Gitee吧。

*注：学会Gitee基本使用教程之后，理论上这套教程可以在Github/Gitlab等很多开放平台(才不是因为它们很像)，但是如果发现不同和的就需要进行对应平台的学习。*

## 什么是Gitee

Gitee 是一个版本控制和协作的代码托管平台(不仅可以托管代码，还可以托管文档与图片资料）。 它可以让你和其他人一起在远程或本地项目上进行协作。

本教程将为您介绍 Gitee 的一些基础知识，如：仓库、分支、分支修改确认以及 Pull Request (代码评审）。您将创建自己的 Text-Gitee 仓库，并学习 Gitee 的 Pull Request 工作流

提示：

1. 您可在单独的浏览器窗口打开此页面，以便按步骤操作时进行查看
2. 在创建仓库前确认自己是否绑定了邮箱，若没有可点击右上角头像，进入设置，在“多邮箱配置”中进行设置

## 使用Gitee

### 创建Gitee仓库

仓库是用来存放自己的一个项目、一个练习的资料库。

仓库内可以存放的内容包括：文件夹、文件、图片等任何在计算机中可以识别的元素。

创建仓库的时候推荐一般要一起创建README.md的文档来介绍这个仓库是干什么，存放什么的，怎么使用这个仓库或者这个仓库隶属于那个组织，谁赞助了这个仓库等。总之README.md就是这个仓库的个人介绍，一般都会推荐写。

除此之外还可以选择开源许可证文件(如果不知道或者没见过这个那么可以请看[五分钟看懂开源协议 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/80075905)这篇文章介绍了什么是开源协议)，让你明确自己的资源别人开源如何使用。

好了说了那么多说一下如何创建一个自己的仓库吧：

创建自己的仓库分为两种方式：

1. 从该平台创建
2. 从其他平台导入

#### 创建Gitee仓库步骤

以Gitee这个平台为例子，在登入/注册完之后会进入到这样的一个画面：

![image-20230412204748801](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412204748801.png)

如果你和我的不一样也不需要紧张，因为这是我个人的。

我们开源看到右上角中有一个加号：

![image-20230412204936356](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412204936356.png)

我们将鼠标悬停靠近那个加号或者点那个加号：

![image-20230412205027532](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412205027532.png)

然后再点击新建仓库的页面：

![image-20230412205101373](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412205101373.png)

我们将仓库名称设置为Text-gitee，路径会自动匹配仓库名称可以选择自己自定义或者就按照他匹配的名称

![image-20230412205511227](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412205511227.png)

仓库介绍的话可填可不填都不会影响我们接下来的步骤。

##### 初始化仓库

![image-20230412205905289](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412205905289.png)

选择语言：就是你这个仓库主要的编程语言是什么，根据仓库的目的选择语言，创建后可以更改。

.gitignore：就是你在git提交的时候需要过滤掉的文件，就像C/C++语言当中的dll、exe、obj等这些都是项目运行时生成的相对整个仓库来说都是没有必要的存在(点名批评VS你生成那么一大堆一个几十k的代码几百M的编译器生成文件)所以如果加上.gitignore就是过滤掉不需要提交的文件，同时这个也是可以更改的打开后生成这样的一长串：

![image-20230412210546877](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412210546877.png)

添加开源许可证：这个前面说过了不记的可以看看前面。

##### 设置模板

这个就比较简单了

![image-20230412210742167](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412210742167.png)

这个就是询问你要不要在创建的时候加上这几个文件和模板，我推荐时加上Readme文件或者在本地创建时手写也可以，其他的两个暂时用不到暂时不进行介绍。

##### 选择分支模型

![image-20230412210929083](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412210929083.png)

这个就比较复杂了这个首先你先要具备使用Git的基本知识，关于分支之后我们会在[Git初始教程](./Git初始教程.md)中提到这里暂时不展开说明这个选择分支模型。

那么我们就只需要创建一个带有Readme文件的仓库就好了就像这样：

![image-20230412211207144](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412211207144.png)

这样我们就创建完毕一个新的仓库了：

![image-20230412211302903](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412211302903.png)

### 创建一个新分支

创建新分支是为了避免在修改文本时丢失原始信息的一种有效方式。为了确保文本修改的正确性和完整性，我们需要在新分支上进行修改，并与原始文档进行对比，以确定修改的地方和删除的内容。如果发现副本中的有价值的原始记录内容被删除，我们可以继续修改副本，以保留这些有价值的信息。这样可以避免在修改文本时丢失重要信息而导致不必要的损失。

![看懂Git工作流](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/49e51a56668b4628adcde4a31eb886e0~tplv-k3u1fbpfcp-zoom-in-crop-mark_1512_0_0_0.webp)

#### 创建一个分支步骤

创建完之后我们会在克隆/下载一览当中看到：

![image-20230412212005566](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212005566.png)

这里有一个分支，点击这个分支我们就可以进入到这样的一个页面：

![image-20230412212108794](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212108794.png)

点击新建分支就会出现这样的一个界面：

![image-20230412212341678](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212341678.png)

我们给这个新分支起一个响亮的名字就叫main好了下面的分支属性我们可以不用管，分支备注可写可不写。点击确定，这样我们就创建了一个新分支：

![image-20230412212555047](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212555047.png)

### 修改分支并提交更改

#### 修改分支并提交更改步骤

![image-20230412212646312](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212646312.png)

我们点击master这里会发现会有一个main这时我们点击main，那么现在我们就切换到main分支了（虽然说都一样就是了）。我们在main分支中的README.md当做一些手脚，点击README.md进入到界面当中：

![image-20230412212836381](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212836381.png)

点上红色箭头指向的编辑按钮：

![image-20230412212956809](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412212956809.png)

进入到文本里面：

![image-20230412213020981](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213020981.png)

我们就在前面添上一句第一次测试

![image-20230412213122240](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213122240.png)

滑到后面提交它，回到README.md我们可以看到我们写的第一次测试已经出现在第一行了。

![image-20230412213135067](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213135067.png)

至此我们已经修改分支并且提交它了。

### 提交Pull Request

Pull Request是一种协作方式，它允许开发人员将自己所做的修改请求合并到代码库的主干分支中。这种方式使得多人协作开发变得更加简单和高效。具体来说，开发人员可以在自己的分支上进行修改，然后将修改请求提交到主干分支，代码库管理员可以在代码评审后，决定是否将修改请求合并到主干分支中。这种方式保证了代码库的稳定性和安全性，同时也方便了多人协作开发过程中的交流和管理。

#### 提交Pull Request步骤

点击顶部的Pull Request切换到Pull Request的界面

![image-20230412213657126](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213657126.png)

切换到之后点击新建Pull Requests

![image-20230412213830480](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213830480.png)

我们选择源分支为main，目标分支为master

给其起标题名为Text,说明为First text PR

![image-20230412213944470](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230412213944470.png)

之后我们再滑到下面选择创建Pull Request，这样我们就创建了首个Pull Request。

### 合并提交的Pull Request

作为仓库的拥有者，在合并提交的Pull Request前一定要确认新分支的修改是否符合自己的期望，如果不符合可以在线反馈自己的意见。

让我们来完成历史性的一刻吧！

#### 合并分支步骤

1. 进入Pull Request页面，选择开启的，点击Text这个Pull Request。

![image-20230413122611532](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413122611532.png)

2. 可在文件选项中查看提交的分支与 master 分支有什么差别，可通过颜色对比查看。

（白色：无修改；红色：删减内容；蓝色：新增内容）

![image-20230413122736723](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413122736723.png)

3. 点击审查通过，测试通过。

![image-20230413122852141](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413122852141.png)

之后我们就填写Pull Request的标题和内容

![image-20230413123242388](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413123242388.png)

合并完我们就会发现已合并了，但是Gitee给我们提供了一个回退的功能，可以还原到合并之前的状态。

![image-20230413123404944](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413123404944.png)

这样我们就完成了合并并提交Pull Request了。

### 打Issue

**issue**：在issue中，发布的内容应该是**代办事项（to do list）**。
**例如**，在issue中发送**推荐实现的新特性**，**需要修复的BUG**，**需要改进的内容**。

**如果发现一个仓库文本当中或者图片当中有错误的地方那么请务必在这个仓库中打ISSUE并且说明错误的原因或者你对文本有疑问的地方也可以打ISSUE**。

#### 打Issue步骤

我们点开我们的仓库，然后进入首栏就可以看见Issues了，我们点击Issues，之后再点击新建Issue。

![image-20230413123806414](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230413123806414.png)

这里我们可以看到右边有几个选项，

![image-20230416165730355](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230416165730355.png)

分别介绍一下：

1. 负责人：负责人是指该 Issue 的处理人员，一般为仓库创始人或管理员，也可以是其他仓库管理员。如果不知道应该指定谁为负责人，建议指定仓库创始人为负责人。
2. 标签：标签用于标记 Issue 的类型和主要内容，可以自定义标签，也可以使用系统自带的标签。标签可以明确问题类型，如修复 bug、添加新功能等。
3. 分支：如果项目中有多个分支，需要指定 Issue 发生在哪个分支上，以便负责人更好地处理该问题。
4. 开始日期和截止日期：开始日期指 Issue 的创建日期，截止日期是结束 Issue 的负责人填写的。截止日期有助于提醒负责人尽快解决问题，保证项目的进度和质量。
5. 置顶选项和优先级：这两个选项由负责人填写，用于设置 Issue 的处理优先级和重要程度。
6. Pull Request：如果在创建 Issue 时已经提交了 Pull Request，需要填写此项以便跟踪代码合并的过程。

接下来我们填写一个标题为：修正`README.md`。

内容为修正`README.md`。

指定负责人为仓库创建者(你自己)，标签为bug，分支为master，其他则默认不填。

![image-20230416171403558](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230416171403558.png)

点击创建，我们回到仓库的Issues就发现我们已经创建完一个开启的名为修正`README.md`的Issue了。

![image-20230416171523652](./git%E5%9F%BA%E6%9C%AC%E6%95%99%E7%A8%8B.assets/image-20230416171523652.png)

## 写在最后

至此，我们的Gitee基本使用教程已经完成了(芜湖，完结散花)。如果想要深入了解怎么提交和修增文本那么请看[Git初始教程](./Git初始教程.md)，如果不知道markdown是什么请看[markdown教程](./markdown教程.md)。如果你已经学习完本篇还有其他的两篇那么你就可以参加我们或者自己创建项目了，期待那就是下一个全绿大佬。
