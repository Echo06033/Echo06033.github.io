---
title: markdown学习手记
categories:
  - 学习
tags:
  - CS
date: 2026-10-22 17:51:53
cover: /img/markdown.png
description:
---

#首先一些常用学习资源（文末有完整资源）
[commonmark官方文档](https://commonmark.org/help/)
[速查表](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
[GitHub官方文档](https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

# Markdown 常用格式

> 一份包含：基本语法介绍 + 资源推荐

---

## 一、Markdown介绍

Markdown 是一种**轻量级标记语言**，用纯文本编写、可转成 HTML。由 John Gruber 在 2004 年创建，后续发展出 **CommonMark**（标准化规范）和 **GFM**（GitHub 扩展，实际使用最广）。

**没有唯一官方标准**，各平台有细微差异（GitHub、Typora、Obsidian、知乎等）。

---

## 二、常用语法格式

### 1. 文本样式

```markdown
**加粗**
*斜体*
***粗斜体***
~~删除线~~
`行内代码`
```

效果：
**加粗**　*斜体*　***粗斜体***　~~删除线~~　`行内代码`

### 2. 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

### 3. 列表

```markdown
### 无序列表
- 项目一
- 项目二
  - 子项目（缩进两个空格）

### 有序列表
1. 第一项
2. 第二项
3. 第三项
```
效果：
- 项目一
- 项目二
  - 子项目（缩进两个空格）
1. 第一项
2. 第二项
3. 第三项

### 4. 链接与图片

```markdown
#超链接
[链接文字](https://example.com)

![图片描述](图片URL地址)

#顶部锚点跳转
[跳转到某个标题](#标题文字)  ← 标题转小写、空格变-
```

举例：
[我的博客](https://echo06033.github.io/)
![picture](C:\Users\XW\Pictures\Screenshots\a.jpg)
[链接与图片](#4-链接与图片)
注意：写锚点跳转的时候，英文需要变为小写，符号要省去，空格要替换为-（比如标题`###Title above_all`应该写为`#title-aboveall`）

### 5. 代码块

````markdown
```python
def hello():
    print("你好")
```
````
效果：(第一行的python是注明了代码块的语言，也可以不加)
```python
def hello():
    print("你好")
```
注：可使用嵌套代码块，只要在外层使用````即可

### 6. 引用

```markdown
> 这是一段引用
>
> > 嵌套引用
```
效果：
> 这是一段引用
>
> > 嵌套引用

### 7. 表格

```markdown
| 列1 | 列2 | 列3 |
|------|------|------|
| 数据 | 数据 | 数据 |

### 表格对齐（左/中/右）
| 左对齐 | 居中 | 右对齐 |
| :------ | :---: | ------: |
| 内容    | 内容  | 内容    |
```
效果：
| 列1 | 列2 | 列3 |
|------|------|------|
| 数据 | 数据 | 数据 |

| 左对齐 | 居中 | 右对齐 |
| :------ | :---: | ------: |
| 内容    | 内容  | 内容    |

### 8. 分割线

```markdown
---
```

### 9. 任务清单（GFM，GitHub/Typora 支持）

```markdown
- [x] 已完成的事项
- [ ] 待办事项1
- [ ] 待办事项2
```
效果：
- [x] 已完成的事项
- [ ] 待办事项1
- [ ] 待办事项2

### 10. 转义字符

```markdown
\* 星号　\# 井号　\_ 下划线
```

用反斜杠 `\` 转义

效果：
\* 　\# 　\_ 

### 11. 其他进阶格式

````markdown
### 表情
:smile:  :rocket:  :fire:  :warning:

### 折叠（GitHub 支持）
<details>
<summary>点开查看</summary>
这里是被折叠的内容
</details>

### 数学公式（KaTeX/MathJax 渲染器支持）
行内公式：$E = mc^2$

块级公式：
$$
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
$$

### Mermaid 流程图（部分平台支持）
```mermaid
graph LR
A[开始] --> B{判断}
B -->|是| C[完成]
B -->|否| A
```
````

效果：
:smile:  :rocket:  :fire:  :warning:
<details>
<summary>点开查看</summary>
这里是被折叠的内容
</details>
行内公式：$E = mc^2$

块级公式：
$$
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
$$

---

## 三、学习资源

### 正规官方

| 链接 | 说明 |
|------|------|
| [CommonMark 官方教程](https://commonmark.org/help/) | 标准化规范的官方交互式教程 |
| [CommonMark Spec 完整规范](https://spec.commonmark.org/) | 完整技术规范，遇到边界情况查阅 |
| [John Gruber 原版 Markdown](https://daringfireball.net/projects/markdown/) | Markdown 发明者的原始定义 |
| [GitHub 官方帮助文档（中文）](https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) | GFM 官方中文文档，日常最实用 |
| [GitHub 官方 Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) | 全球最流行的速查表 |

### 中文热门教程

| 链接 | 说明 |
|------|------|
| [菜鸟教程 Markdown](https://www.runoob.com/markdown/md-tutorial.html) | 中文访问量最高 |
| [掘金 Markdown 相关文章](https://juejin.cn/search?query=markdown%20%E8%AF%AD%E6%B3%95) | 技术博主实战案例 |
| [知乎 Markdown 讨论](https://www.zhihu.com/search?type=content&q=Markdown%20%E5%85%A5%E9%97%A8) | 工具推荐与技巧 |

### 交互式在线练习

| 链接 | 说明 |
|------|------|
| [Markdown Live Preview](https://markdownlivepreview.com/) | 实时预览编辑器 |
| [StackEdit](https://stackedit.io/) | 在线编辑器+教程 |

---

### 推荐编辑器：
- Obsidian：个人知识库、学习笔记、日记、项目资料；最均衡的首选。
- Typora：专注写作，所见即所得体验非常舒服；适合不想折腾功能的人。
- VS Code：写技术文档、代码仓库里的 README / docs；Git、预览和扩展很方便。
- MarkText：免费开源、界面简洁，适合轻量本地 Markdown 编辑。
- Notion：协作和数据库能力强，但并非原生本地 Markdown 工作流，导出与离线体验相对一般。
- Bear（Mac/iPhone）：写作体验漂亮顺滑，适合苹果生态，但跨平台有限。