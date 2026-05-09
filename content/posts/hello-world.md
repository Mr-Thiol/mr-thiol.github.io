---
title: "My First Post with Math"
date: 2026-01-13T20:00:00+08:00
draft: true  # 【关键】把 true 改成 false，否则默认不显示
tags: ["Chemistry", "Hugo", "AI for Science"]  # <--- 加上这一行！注意格式
categories: ["Research"] # 顺便也可以加上分类
---

## Welcome

这是我的第一个 Hugo 网站。

### 测试数学公式 (MathJax)
我们可以使用 LaTeX 编写量子化学公式：

$$
\hat{H}\Psi = E\Psi
$$

对于谐振子模型：
$$E_n = \hbar \omega (n + \frac{1}{2})$$

### 测试代码高亮
```python
def get_catalyst_performance(d_band_center):
    """
    A simple function to predict activity based on d-band center
    """
    return -0.5 * d_band_center + 0.2