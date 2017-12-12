---
title: Principles of Information Visualization
date: 2017-12-09 10:51:13
tags: 
- Python
- Matplotlib
- MachineLearning
categories: 
- Python
- Matplotlib
- 可视化
---
## Inroduction
本课程的主要内容是理解如何更清楚地向那些对数据感兴趣的利益相关者传达数据。有许多不同的利益相关者可能对使用视觉材料感兴趣。  
例如，你想和同行的数据科学家分享公正的数据表达，他们能够做出自己的推论和解释。但是，您也希望能够与可能熟悉域名但正在寻找具体可操作见解的经理和主管分享数据故事。  
在这个课程中将学会得到一个新的可视化技术，你将被要求扩展matplotlib代码库来增强其功能。这是您作为数据科学家的重要一步。要超越使用现成的工具，而是能够修改它们以支持理解数据和问题的新方法。
<!-- more -->
## Tools for Thinking about Design (Alberto Cairo)
- 首先是抽象和形象
- 第二个方面是功能性和装饰性
- 第三个维度是密度和亮度
- 第四个方面是图形的维度
- 第五个维度是独创性和熟悉性
- 最后一个维度是新颖性和冗余性维度

## Graphical heuristics: Data-ink ratio (Edward Tufte)
introduces two interesting graphical heuristics, the data-ink ratio and chart junk.
 
 Tufte的第一个图形启发式是data-ink rate数据墨水比率。 Tufte将数据墨水定义为图形的不可擦除核心。根据所表示的数字的变化排列非冗余墨水,建议我们删除那些不会为图形添加新信息的元素。

 另一个启发式称为chartjunk。现在，Tufte比其他形式的非数据墨水更受制于图表垃圾。事实上，他认为统计图上的艺术装饰就像我们数据图形中的杂草。

 ## The Truthful Art (Alberto Cairo)
- The first quality of a good visualization is that it's truthful.
    - First, we have to be honest with ourselves when we clean and summarize data. 
    - The second obligation is to our audience. 
- The second quality of a visualization to consider is whether it is functional or not. 
- The third quality of visualization, Cairo shares is whether it is beautiful or not. 
- The fourth quality of visualization from Cairo is that information graphics should be insightful. 
- The final quality of visualization which Cairo proposes is information graphics should be enlightening