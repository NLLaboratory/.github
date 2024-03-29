# markdown

___

## 1. markdown是什么？

```markdown```的文件后缀是```.md```。也就是说，本文档也是用```markdown```书写的。

```markdown```是一种**用于记录笔记的文件**。

___

## 2. 为什么使用markdown来记笔记？

因为流行，大家都用这个语言来记录笔记。

我们常见的```README.md```就是用markdown写的。

___

## 3. 如何使用markdown？

这里是菜鸟教程中的[markdown教程](https://www.runoob.com/markdown/md-tutorial.html)

***

### 3.1 标题

**写法如下：**

```markdown
# 一级标题
## 二级标题
### 三级标题
...
```

> 这里需要注意的是，#后要加一个空格。

**显示效果如下：**

# 一级标题

## 二级标题

### 三级标题

___

### 3.2 斜体

**写法如下：**

```markdown
*斜体文字*
```

**显示效果如下：**
*斜体文字*

___

### 3.3 加粗

**写法如下：**

```markdown
**被加粗文字**
```

**显示效果如下：**
**被加粗文字**

___

### 3.4 删除线

**写法如下：**

```markdown
~~被加粗文字~~
```

**显示效果如下：**
~~被加粗文字~~

___

### 3.5 分割线

**写法如下：**

```markdown
***
```

**显示效果如下：**

***

___

### 3.6 列表

**写法如下：**

```markdown
* 第一项
* 第二项
* 第三项
```

> 这里需要注意的是，*后面要加个空格。

**显示效果如下：**

* 第一项
* 第二项
* 第三项

___

### 3.7 数字列表

**写法如下：**

```markdown
1. 第一项
2. 第二项
3. 第三项
```

> 这里需要注意的是，.后面要加空格。

**显示效果如下：**

1. 第一项
2. 第二项
3. 第三项

___

### 3.8 区块

**写法如下：**

```markdown
> 这是一个区块
>> 这是一个嵌套区块
```

**显示效果如下：**

> 这是一个区块
>
> > 这是一个嵌套区块

___

### 3.9 代码

**写法如下：**

```markdown
`这里是代码`
```

**显示效果如下：**
`这里是代码`

___

### 3.10 链接

**写法如下：**

```markdown
[链接名](链接地址)
```

**显示效果如下：**
[链接名](链接地址)

___

### 3.11 图片

**写法如下：**

```markdown
![图片名](图片地址)
```

**显示效果如下：**
![图片名](D:/Git-Text/lab-notes/%25E5%258F%2582%25E4%25B8%258EGitee%25E7%25BB%2584%25E7%25BB%2587%25E5%25BF%2585%25E5%25A4%2587%25E7%259F%25A5%25E8%25AF%2586/markdown/%25E5%259B%25BE%25E7%2589%2587%25E5%259C%25B0%25E5%259D%2580)

___

### 3.12 页内跳转

**写法如下：**

```
[显示的文字1](#1)
<span id="1"/>

[显示的文字2](#2)
<span id="2"/>
```

> 这里点击**显示的文字1**，就会跳转到\<span id="1"/>的所在行。
> 这里点击**显示的文字2**，就会跳转到\<span id="2"/>的所在行。

**显示效果如下：**
[显示的文字1](#1)
<span id="1"/>

[显示的文字2](#2)
<span id="2"/>