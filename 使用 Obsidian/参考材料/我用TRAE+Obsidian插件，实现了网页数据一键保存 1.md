![Image](https://mmbiz.qpic.cn/sz_mmbiz_png/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbNVFc8mdFNzVsHicR5QHicOamY3LiaoJjOdoMHWaZjkx1tCvPBkdL53VCw/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)

有人说，未来人与人之间的差距，不在“会不会用AI”，而在“你喂给AI的是什么”。

说实话，大模型越来越强，真正卡住普通人的不是参数，不是算力，而是——数据质量。

![Image](https://mmbiz.qpic.cn/sz_mmbiz_jpg/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbvozEkv9wahlZlS8Sue8gcSElNTvZK1OfhmusXxPN9ArDVMqo2XHxJQ/640?wx_fmt=jpeg&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=1)

你让AI去网上“自己查”，它查到的是金子还是沙子，你根本控制不了。

结果就是：模型很强，结论很虚。

所以我最近干了一件特别朴素、但特别有效的事：用 Trae + Obsidian插件（浏览器一键保存）把高质量数据先“抓到自己碗里”，再让AI做分析。

这套玩法，我把它叫做：给AI配一个“数字参谋部”。你负责定方向和选原料，AI负责切菜、摆盘、做趋势图。

👇这篇文章我会手把手带你从0到1做完：把官方统计数据保存到本地 → 在 Trae 里提取关键指标 → 生成可交互的趋势报告（HTML）。

![图片](https://mmbiz.qpic.cn/sz_mmbiz_gif/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCb6ThoiargzKgRXnZZmnibGPicqwMKHvnFBt7SicKYKU38hN66WrCJyqBNxg/640?wx_fmt=gif&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=2)

## 01 先把底层逻辑说透：AI的上限=你给它的“食材”

很多人用AI翻车，不是因为不会写提示词，而是因为“数据源不干净”。

简单来说：

数据质量低 → 结论再漂亮也没用。

数据质量高 → 你随便问两句都能出洞见。

这就像做菜。

你拿路边随便捡的菜叶子，再厉害的大厨也救不回来。

你拿国家统计局这种“金子级食材”，AI随便一炒都是硬菜。

![Image](https://mmbiz.qpic.cn/sz_mmbiz_jpg/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbdEfgI6NEjPnC6odVic9WtylX22ib1cux2Cs9sribgGianEoMs3eeayrI4Q/640?wx_fmt=jpeg&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=3)

所以最优解不是“让AI到处乱搜”，而是：

先锁定权威数据源（官方信息）→ 统一保存进自己的资料库 → 再让AI做归纳、提取、可视化。

比如

我们要分析房地产，最好的源头在哪里？国家统计局。

![Image](https://mmbiz.qpic.cn/sz_mmbiz_png/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbXGGRtObTOeXdKPuVDg2ACqm6RrT5gsDPr9kR89a1MpyRhCd8CNxOlg/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=4)

这些地方的数据，是高质量的数据源。它们不带情绪，不带立场，只有冷冰冰但最真实的数字。

但是，网页上的数据密密麻麻，怎么给 Trae？复制粘贴？还有图片和数据表，整理起来非常麻烦。

![Image](https://mmbiz.qpic.cn/sz_mmbiz_gif/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbcR23hNDaNq411bl3IdjS1Afm5YPMUQOEOMf652w53Ag5TnvBQKOgmA/640?wx_fmt=gif&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=5)

这就需要用到下面的神器。👇

## 02 实战演示：用 Obsidian 一键收集，让 Trae 做两段式加工

这部分我按“结果展示 → 准备工作 → 最终完成”来走，你跟着做就行。

### （一）结果展示：你最终会得到什么？

你会得到一个可以直接用浏览器打开的 HTML 报告：

可复制、可分享：手机能看，电脑能看，发同事也能看。

![图片](https://mmbiz.qpic.cn/sz_mmbiz_gif/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCb6ThoiargzKgRXnZZmnibGPicqwMKHvnFBt7SicKYKU38hN66WrCJyqBNxg/640?wx_fmt=gif&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=6)

### （二）准备工作：3分钟把“采集器”装好

![Image](https://mmbiz.qpic.cn/sz_mmbiz_jpg/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbARYfHb8JePsDGReOd4iaSGyQCkKzhemTribmnQm8dhprxvHvzbb9iaj1A/640?wx_fmt=jpeg&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=7)

1）打开 Chrome 或者 Edge 的扩展商店

2）搜索“Obsidian”（不能登录扩展商店的朋友可以使用Edge浏览器）

3）一键安装

4）安装完成后，把它置顶到扩展栏（方便随手保存）

![Image](https://mmbiz.qpic.cn/sz_mmbiz_png/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbxBibI63XwnnYoM7zicicVicAtSicTdEs7AXZ7oicAQshscicZPlV3xXg6wbzQ/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=8)

![Image](https://mmbiz.qpic.cn/sz_mmbiz_png/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbojGCcfRcFGXiaGT4Hf8LSNzeH3t9WWt0U8hSCZBcP4vkDdeLxYVCMNg/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=9)

你可以把它理解为：一个“网页保存按钮”。打开内容网页，点一下，它就存进你本地的文件夹中。

“Obsidian”配置方法

这个小插件其实有一堆很实用的选项。我建议你装好后先做两件事，体验会顺很多：

![Image](https://mmbiz.qpic.cn/sz_mmbiz_png/icMjSHOpnbia96rfiaB7S0EroRxsdbJhhCbEuu4rZeYweic7Clth2tfwib3CAzNkgS9DdWNb5XH6yrfCK5FGnRBMxug/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=10)

改成中文界面：点插件的设置（齿轮）→ 左侧【常规/General】→ 语言选【简体中文】

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

让它直接保存到本地：在【保存行为】里选择【保存文件】→ 文件会直接进你电脑的【下载】目录

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

在新建模板下“Default”设置属性名称，我都修改成了中文。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

使用这个方式保存数据到本地，后面你再把“下载目录里的文件”统一搬进自己的Trae文件夹，数据就彻底归你了。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

Trae的基础教程去看以前的分享，上手很简单，比Office要容易。

[硅谷大佬暴论：AI编程没练满2000小时，世界级大神也只能算实习生](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247485885&idx=1&sn=fa42b51d97e42d1508bf32a4a272604a&scene=21#wechat_redirect)

[我用 Trae 扒光了上市公司的底牌，轻松分析100万字以上财报](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247485710&idx=1&sn=deac356ce01fea6a95eb16101ab93f7a&scene=21#wechat_redirect)

[我用Trae训练了专家知识，帮我分析政策文件](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247485794&idx=1&sn=530c851c720b7fddcb3830733123df4e&scene=21#wechat_redirect)

[我用 Trae + 飞书 MCP，给 AI 装上了“第二大脑”【保姆级教程】](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247486034&idx=1&sn=a4857ffa6db2b94cfe0bef52f60859d7&scene=21#wechat_redirect)

### （三）最终完成：Trae 里用“两段式”把原料变成报告

我个人强烈建议你用“两段式”流程，不要一步到位直接让AI生成HTML。

为什么？因为直接生成HTML很容易漏掉你想要的字段，表达乱，后期改起来痛苦。

两段式的好处是：你永远有一份“底层干净数据”可控可追溯。

#### 阶段1：归纳与提取（先把数据提纯成一份结构化内容文档）

这一步就是要把所有数据中的主要部分，进行原文提取摘录，形成一个md文档。

什么是Markdown，可以在后台回复「Markdown」获取文档，10分钟学会。

提示词就是根据已有数据，详细描述需要摘录什么内容。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

完成后会得到一份新的文档，这就是底层数据汇总。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

#### 阶段2：生成可交互报告（把结构化数据变成可视化页面）

当你已经有了“按年份整理好的md数据”，再让 Trae 生成 HTML 数据分析报告：

这一步你可以自由发挥，可以使用下面的提示词作为初步尝试。你也可以选择“优化输入内容”，让trae自动帮你优化提示词。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

或者参考我之前分享的，如何使用skill去控制设计风格。

[99%的 SKILLS 都很“鸡肋”，但用好了是真香，扣子 + TRAE 双平台手把手配置](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247486149&idx=1&sn=a50e9a3bb4a11e81573d8f224c70b146&scene=21#wechat_redirect)

总之，有多种使用方式，但并没有技术难点，我重点讲方法，提示词没有特别构思。

如果后期你要添数据，也按这两个动作走：

1）先更新底层文档（补充原始数据）

2）再更新网页表达（把新增内容加到HTML里）

你会发现这套流程非常“可控”：数据不丢、逻辑不乱、改起来不抓瞎。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

当你有了多年数据，真正有价值的是“对比”。把AI当“分析师”用

比如房地产这类问题：

房价到底有没有在降？趋势处于什么阶段？

当你拥有了这份数据后，当你提出你的任何疑问，你会发现，你拥有了顶级的AI数据参谋。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这个方式轻松实现了过去我们不可能完成的任务。

Trae是一个编程软件，但我真的是把它当成一个数据分析，与大模型沟通的窗口来用的，因为我发现普通人要的不是“会编程”，而是“会指挥”。Trae就是一个指挥台。

## 03 写在最后

你觉得这套方法怎么样呢，评论区告诉我。

如果你对我做的房地产趋势交互HTML感兴趣，后台回复“地产”，我免费发你一份。

回复“Markdown”，10分钟学会与AI交流的文本语言。

我是漂亮的行动派，我们下次见。

让 AI 成为你的超级助手。

专注 AI 提效，和大家分享好用、实用的 AI方法。

![Image](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

[![图片](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247486034&idx=1&sn=a4857ffa6db2b94cfe0bef52f60859d7&scene=21#wechat_redirect)

[![图片](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247485950&idx=1&sn=2b892c703c060ba9bd06fe99ae173334&scene=21#wechat_redirect)

[![图片](data:image/svg+xml,%3C%3Fxml%20version='1.0'%20encoding='UTF-8'%3F%3E%3Csvg%20width='1px'%20height='1px'%20viewBox='0%200%201%201'%20version='1.1'%20xmlns='http://www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate\(-249.000000,%20-126.000000\)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)](https://mp.weixin.qq.com/s?__biz=MzkzNDk2MDI3Mw==&mid=2247485904&idx=1&sn=d6b1d35cc988f1d8f718c967134dccbc&scene=21#wechat_redirect)