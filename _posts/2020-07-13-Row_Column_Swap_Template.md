---
title: Row & Column Swap Template
search: true
categories:
  - SQL
published: true
toc: true
toc_label: ON THIS PAGE
toc_icon: crosshairs
tag: Easy
---

## Row_Column_Swap_Template

![image](/assets/images/行列互换.png)

```
select A,
-- 第2步，在行列互换结果表中，其他列里的值分别使用case和max来获取
max(case B when 'm' then C else 0 end) as 'm',
max(case B when 'n' then C else 0 end) as 'n'
from cook
-- 第1步，在行列互换结果表中按第1列分组
group by A;
```
