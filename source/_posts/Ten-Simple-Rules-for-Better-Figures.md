---
title: Ten Simple Rules for Better Figures
date: 2017-12-14 14:09:35
tags: 可视化
categories: 可视化
---
科学可视化经典定义为图形化显示科学数据的过程。 但是，这个过程远非直接的或自动的。 有很多不同的方法来表示相同的数据：散点图，线性图，条形图和饼图，等等。 此外，使用相同类型的情节的相同数据可能被视为非常不同，取决于谁在看数字。 科学可视化的更准确的定义将是人与数据之间的图形界面。 在这篇短文中，我们旨在提供一套基本的规则来改善图形设计，并解释一些常见的陷阱。

## Rule 1: Know Your Audience

## Rule 2: Identify Your Message

## Rule 3: Adapt the Figure to the Support Medium

## Rule 4: Captions Are Not Optional

## Rule 5: Do Not Trust the Defaults

## Rule 6: Use Color Effectively

## Rule 7: Do Not Mislead the Reader

## Rule 8: Avoid “Chartjunk”

## Rule 9: Message Trumps Beauty

## Rule 10: Get the Right Tool

<!-- more -->

```
import matplotlib.pyplot as plt
import numpy as np

plt.figure()

languages =['Python', 'SQL', 'Java', 'C++', 'JavaScript']
pos = np.arange(len(languages))
popularity = [56, 39, 34, 34, 29]

# change the bar color to be less bright blue
bars = plt.bar(pos, popularity, align='center', linewidth=0, color='lightslategrey')
# make one bar, the python bar, a contrasting color
bars[0].set_color('#1F77B4')

# soften all labels by turning grey
plt.xticks(pos, languages, alpha=0.8)
# remove the Y label since bars are directly labeled
#plt.ylabel('% Popularity', alpha=0.8)
plt.title('Top 5 Languages for Math & Data \nby % popularity on Stack Overflow', alpha=0.8)

# remove all the ticks (both axes), and tick labels on the Y axis
plt.tick_params(top='off', bottom='off', left='off', right='off', labelleft='off', labelbottom='on')

# remove the frame of the chart
for spine in plt.gca().spines.values():
    spine.set_visible(False)
    
# direct label each bar with Y axis values
for bar in bars:
    plt.gca().text(bar.get_x() + bar.get_width()/2, bar.get_height() - 5, str(int(bar.get_height())) + '%', 
                 ha='center', color='w', fontsize=11)
plt.show()
```