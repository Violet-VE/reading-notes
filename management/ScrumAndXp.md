# 硝烟中的Scrum和XP
![cover](https://img3.doubanio.com/view/subject/l/public/s6275660.jpg)

    作者: 克里伯格 
    出版社: 清华大学
    副标题: 我们如何实施Scrum
    译者: 李剑 
    出版年: 2011-1
    页数: 166
    定价: 29.00元
    ISBN: 9787302243335

[豆瓣链接](https://book.douban.com/subject/5501718/)

## 第2章  我们怎样编写产品backlog
产品backlog是Scrum的核心，也是一切的起源。

我们叫它`故事（story）`，有时候也叫做`backlog条目（事项）`。

- `ID`统一标识符，就是个自增长的数字而已。以防重命名故事以后找不到它们。
- `Name（名称）`  简短的、描述性的故事名。比如“查看你自己的交易明细”。它必须要含义明确，这样开发人员和产品负责人才能大致明白我们说的是什么东西，跟其他故事区分开。它一般由2到10个字组成。
- `Importance（重要性）`  产品负责人评出一个数值，指示这个故事有多重要。例如10或150。分数越高越重要。
- `Initial estimate（初始估算）`  团队的初步估算，表示与其他故事相比，完成该故事所需的工作量。最小的单位是`故事点（story point）`，一般大致相当于一个“理想的人天”（man-day）。
    - 问一下你的团队，“如果可以投入最适合的人员来完成这个故事（人数要适中，通常为2个），把你们锁到一个屋子里，有很多食物，在完全没有打扰的情况下工作，那么需要几天，才能给出一个经过测试验证、可以交付的完整实现呢？”如果答案是“把3个人关在一起，大约需要4天时间”，那么初始估算的结果就是12个故事点。
    - 不需要保证这个估值绝对无误（比如两个故事点的故事就应该花两天时间），而是要保证相对的正确性（即，两个点的故事所花费的时间应该是四个点的故事所需的一半）。
- `How to demo（如何做演示）`  它大略描述了这个故事应该如何在sprint 演示上进行示范，本质就是一个简单的测试规范。“先这样做，然后那样做，就应该得到……的结果。”
    - 如果你在使用TDD（测试驱动开发），那么这段描述就可以作为验收测试的伪码表示。
- `Notes（注解）`  相关信息、解释说明和对其他资料的引用等等。一般都非常简短。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/55186824.jpg)

### 额外的故事字段
- `Track（类别）`  当前故事的大致分类，例如“后台系统”或“优化”。这样产品负责人就可以很容易选出所有的“优化”条目，把它们的级别都设得比较低。类似的操作执行起来都很方便。
- `Components（组件）`  通常在Excel文档中用“复选框”实现，例如“数据库，服务器，客户端”。团队或者产品负责人可以在这里进行标识，以明确哪些技术组件在这个故事的实现中会被包含进来。
- `Requestor（请求者）`  产品负责人可能需要记录是哪个客户或相关干系人最先提出了这项需求，在后续开发过程中向他提供反馈。
- `Bug tracking ID（Bug跟踪ID）`  如果你有个bug跟踪系统，就像我们用的Jira一样，那么了解一下故事与bug之间的直接联系就会对你很有帮助。

### 我们如何让产品backlog停留在业务层次上
指出如何解决问题的应该是开发团队，产品负责人只需要关注业务目标。

只要发现这种面向技术的故事，我一般都会问产品负责人 “但是为什么呢”这样的问题，一直问下去，直到我们发现内在的目标为止。然后再用真正的目标来改写这个故事（“提高在后台系统中搜索并生成表单的响应速度”）。

## 第3章  我们怎样准备sprint计划
**在sprint计划会议之前，要确保产品backlog的井然有序**。

- 只能有一个产品backlog和一个产品负责人（对于一个产品而言）。
- 所有重要的backlog条目都已经根据重要性被评过分，不同的重要程度对应不同的分数。
- 其实，重要程度比较低的backlog条目，评分相同也没关系，因为它们在这次sprint计划会议上可能根本不会被提出来。
- 无论任何故事，只要产品负责人相信它会在下一个sprint实现，那它就应该被划分到一个特有的重要性层次。
- 分数只是用来根据重要性对backlog条目排序。假如A的分数是20，而B的分数是100，那仅仅是说明B比A重要而已，绝不意味着B比A重要五倍。如果B的分数是21而不是100，含义也是一样的！
- 最好在分数之间留出适当间隔，以防后面出现一个C，比A重要而不如B重要。当然我们也可以给C打一个20.5分，但这样看上去就很难看了，所以我们还是留出间隔来！
- 产品负责人应当理解每个故事的含义（通常故事都是由他来编写的，但是有的时候其他人也会添加一些请求，产品负责人对它们划分先后次序）。他不需要知道每个故事具体是如何实现的，但是他要知道为什么这个故事会在这里。

## 第4章  我们怎样制定sprint计划
sprint计划会议会产生一些实实在在的成果：

- sprint目标
- 团队成员名单（以及他们的投入程度，如果不是100%的话）
- sprint backlog（即sprint中包括的故事列表）
- 确定好sprint演示日期
- 确定每日Scrum会议的时间和地点

### 为什么产品负责人必须参加
为什么整个团队和产品负责人都必须要参加sprint计划会议？每个故事都含有三个变量，它们两两之间都对彼此有着强烈依赖。

`范围（scope）`和`重要性（importance）`由产品负责人设置。`估算（estimate）`由团队设置。

### 为什么不能在质量上让步
我尽力把`内部质量`和`外部质量`分开。

- 外部质量是系统用户可以感知的。运行缓慢、让人迷糊的用户界面就属于外部质量低劣。
- 内部质量一般指用户看不到的要素，它们对系统的可维护性有深远影响。可维护性包括系统设计的一致性、测试覆盖率、代码可读性和重构等等。

经验告诉我：牺牲内部质量是一个糟糕透顶的想法。现在节省下来一点时间，接下来的日子里你就要一直为它付出代价。一旦我们放松要求，允许代码库中暗藏问题，后面就很难恢复质量了。

### sprint 计划会议日程
#### 确定sprint目标
sprint目标需要回答这个根本的问题，“我们为什么要进行这个sprint？为什么我们不直接放假算了？”要想从产品负责人的口中诱导出sprint目标，你不妨一字不差地问他这个问题看看。

#### 决定sprint要包含的故事
哪些故事需要从产品 backlog拷贝到sprint backlog中，如下图所示。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/50758087.jpg)

每个矩形都表示一个故事，按重要性排序。最重要的故事在列表顶部。矩形尺寸表示故事大小（也就是以故事点估算的时间长短）。括号的高度表示团队`估算的生产率`（estimated velocity），也即团队认为他们在下一个sprint中所能完成的故事点数。

#### 产品负责人如何对sprint放哪些故事产生影响
![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/93093787.jpg)

产品负责人很失望，因为故事D不会被放到sprint里面。

首先，他可以重新设置优先级。如果他给故事D赋予最高的重要级别，团队就不得不把它先放到sprint里面来（在这里需要把C扔出去）。

其次，他可以更改范围——缩小故事A的范围，直到团队相信故事D能在这个sprint里完成为止。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/61334836.jpg)

最后，他还可以拆分故事。产品负责人判断出故事A中某些方面实际并不重要，所以他把A分成两个故事A1和A2，赋给它们不同的重要级别。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/24916866.jpg)

#### 团队怎样决定把哪些故事放到sprint里面
我们在这里使用两个技术。

1. 本能反应。
2. 生产率计算。

下图中，左边是sprint启动时的`估算的生产率`，右边是sprint结束时的`实际生产率`。每个矩形都是一个故事，里面的数字表示这个故事的原始估算。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/23112468.jpg)

那个sprint里面**差不多(Almost)** 可以完成的故事怎么处理？为什么我们在实际生产率里面没把它的部分故事点数算进来？呵呵，这就突出表现了Scrum的要求（实际上也是敏捷软件开发和精益制造的要求）：把事情完全做完！达到可以交付的状态！事情只做了一半，它的价值就是0（也许还会是负数）。

看看团队的历史。看看他们在过去几个sprint里面的生产率是多少，然后假定在下一个sprint里面生产率差不多不变。

这项技术也叫 **“昨日天气”（yesterday’s weather）** 。要想使用该技术，必须满足两个条件：团队已经完成了几个sprint（这样就可以得到统计数据），会以几乎完全相同的方式（团队长度不变，工作状态等条件不变）来进行下一个sprint。当然也不是绝对如此。

我们估算的单位是**故事点（story point）**，差不多可以对应于“理想化的人-天”。一个理想化的人-天是完美、高效、不受打扰的一天，但这种情况太少见了。我们还必须考虑到各种因素，例如要把未计划到的工作添加到sprint中、人们患病不能工作等等。

那我们的估算生产率肯定要比50少了。少多少呢？我们引入 **“投入程度”（focus factor）** 这个词来看一下。

把上一个sprint中完成的所有故事的原始估算加起来，得到的和就是**实际生产率**。

![](http://ou8qjsj0m.bkt.clouddn.com//18-5-1/13577720.jpg)

从上面的公式中可以看出，下个sprint的估算生产率是20个故事点。这表明团队这个sprint中所能做的故事点数之和不能超过20。














