# 智识的生产流程

> 首先需要再三阅读文末所参考的相关文章或书籍，尤其是阳老师的文章。本文只是在其基础上讨论如何通过 GitHub 以及相关工具来实现高效的智识生产流程。

## 卡片

[卡片](https://en.wikipedia.org/wiki/Index_card)是知识的最小单位，以原文摘抄的形式输入，以读书卡片的形式输出

> An index card consists of card stock (heavy paper) cut to a standard size, used for recording and storing small amounts of discrete data.

```
Q4. 卡片写什么
各位同学被要求写作以下类型的卡片，它们往往代表着人类知识体系中的精髓：

- 术语卡：阅读中出现过的学术术语或者作者特定黑话
- 人名卡：阅读中出现过的人名，以及他的个人简介如何
- 反常识卡：有什么理论模型/推断证据/故事/行动，挑战了你的既有常识
- 金句卡：收集性感的句子
- 行动卡：写下你可以执行的行动
- 技巧卡：积累你学到的技巧
- 任意卡：此处自行发挥
```

在上述的卡片外，我们特别强调 `问答卡`，这种类型的卡片，它暗含了人生的基本模式，遇到问题- 拆解问题 - 解决问题 - 遇到问题。同一个问题可能会出现在多个情景中，正如 Hacker 的基本态度之一 `No problem should ever have to be solved twice.` 如果我们将问题和答案的划分粒度够细，便于检索，那么重复解决问题的这个问题就算解决了。

现代社会中，纸质卡片固然还有其价值，但我们可以使用 GitHub 来让这个工作更加高效。

我们将通过 `gist` 来创造卡片，参考 [Stack Overflow](https://stackoverflow.com/a/5537451) 我们可以在 `Gist description` 中通过 `#tag1` `#tag2` 的方式来添加标签来对卡片进行分类，建议至少两个标签：

- 卡片分类标签: 例如 `c_term`， `c_q&a` 等等，其中 `c_` 前缀表示 `category` 便于后期程序处理；
- 话题分类标签：例如 `t_lua`，`t_linux` 等等，其中 `t_` 前缀表示 `topic` 便于后期生产文档
- 其他标签：Do whatever you want.

### 为什么不使用 `issue` 做卡片

主要有三个原因：

1. 创建 `issue` 必须设定标题与不建议给卡片写标题的原则冲突；
2. 公开项目的 `issue` 任何人都可以 `comment`，会给后期带来麻烦
3. 在公开项目中，无法创建私有 `issue`

## 文件

这里所指的文件是可用于交流的完整输出，如文章、论文、绘画文件或产品原型图

主要包括如何导入 `gist` 中的内容，根据内容生成文档，个人润色，最终发布到个人媒体平台的半自动化流程。

在 GitHub 上创建一个项目，例如 `<your github account>.github.io` ，结构目录如下：

```bash
|-- + diagram /     # 图表、流程图等
|-- + doc /         # 最终生成的 HTML 文档
|-- + img /         # 引用的相关图片
|-- + public /      # 公共文件，例如 css js 等
|-- + src /         # 润色的 markdown 文档
|-- + tmp /         # 由工具临时生成的 markdown 文档
|--- config.yml     # 配置文件

```

当然，上面这种枯燥的工作不需要人来做，我们打算创建一个工具来完成该任务，WIP

## 项目

项目是指涉及多人或更长时间的系统输出，如图书或APP开发。

项目中需要进行 `R&D` 这里往往是产生大量问题的与源头，这里我们遵循 **源头引用原则** 。

在 `R&D` 过程也就是一个发散和收敛的过程，在发散过程中遇到的问题和解决方案不一定会真正应用到项目中去，如果不做好记录，这些问题和解决方案慢慢就消失了。而 **源头引用原则** 就是不考虑具体项目实际应用什么方案，而是统一将 `R&D` 过程中遇到的问题和解决方案作为 `问答卡` 存储起来，然后在项目应用时，直接编写 `TODO` 列表，将卡片中问题和解决方案引用附加到相关的 `Item` 就可以了。

## 工具

WIP

## 参考

- [构建优雅的知识创造系统](http://www.yangzhiping.com/psy/yang-KnowledgeSystem.html)
- [跨年答疑（3）：卡片十二问](http://www.yangzhiping.com/psy/happy-new-year-faq3.html)
- [智识的生产技术](https://book.douban.com/subject/26786537/)

## Changelog

- 2018-01-05 @hexcola created.
