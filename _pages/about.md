---
layout: single
title: "Profile"
permalink: /
author_profile: true   # 该页显示左侧栏
classes: wide
---

I am a doctoral researcher focusing on **hardware–software co-design** for deep learning accelerators.  
My current work builds a closed-loop platform that **reinforcement-learning (RL)**. I am broadly interested in ** computer architecture**, and **hardware aware modeling**.

在读博士，研究方向为深度学习加速器的**架构—算法协同设计**，围绕 ** DSE/RL 调度** 优化时延与能耗，目标是面向资源受限设备的高效推理。

## Research Focus
**Primary Research Areas:** AI Accelerators, RL-based Scheduling, Computer Architecture, DFT/Reliability

- Tile-level DAG extraction, weight-reuse modeling, conflict-aware scheduling  
- RL (PPO) for tile/PE allocation; reward shaping for latency/energy/utilization  
- INT8/FP16 MAC pipeline analysis; NVDLA-style CMAC RTL instrumentation  
- Dataflow (DC/Winograd/Eyeriss)–aware cycle/energy estimation

## Selected Publications
> 下方会**自动列出**你在 `_publications/` 目录里的条目（按时间倒序，最多 5 篇）。想展示更多，请到导航里的 **Publications** 页面。

{% assign pubs = site.publications | sort: 'date' | reverse %}
{% for p in pubs limit:5 %}
- **{{ p.title }}**. {{ p.authors }}. *{{ p.venue }}*, {{ p.date | date: "%Y" }}.{% if p.paperurl %} [[PDF]]({{ p.paperurl }}){% endif %}{% if p.code %} [[Code]]({{ p.code }}){% endif %}
{% endfor %}

## News
- 2025-09 — Released RL-driven tile scheduler preprint (draft).  
- 2025-06 — Published tile-trace JSON spec v1.0.

## Contact
- Email: weixiangqing6@gmail.com  
- GitHub: https://github.com/wxq96  
##- Google Scholar: https://scholar.google.com/citations?user=YOURID

