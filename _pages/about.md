---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

# Hi, I'm voidpxL!

我目前从事多源传感器感知方向的算法研发，主要专注于 **毫米波雷达感知数据处理**、**毫米波雷达与视觉的融合感知**、以及 **智能算法工程化部署**。

我的兴趣包括以下方向：

- **Radar数据处理和应用**
- **融合感知** 
- **数据可视化**
- **AI Agent**

在项目中，我主要承担系统方案设计、算法实现与性能落地。长期关注和追求 **实时、稳定、可量化、工程可维护**。

# Portfolios

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/RVF.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[雷视融合]()

RV1126B系统中，搭载大角度的摄像头及和4D毫米波雷达，进行基于RKNN的目标检测、目标跟踪和雷视融合跟踪，输出稳定融合轨迹，并进行对应的可视化展示和报警策略。

</div>
</div>

<!--

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/TC_cls.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[交通雷达数据处理]()

示例

- 示例
</div>
</div>

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/lane.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[流量检测&车道检测]()

示例

- 示例
</div>
</div>


<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/DL.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[电力防外破]()

示例

- 示例
</div>
</div>
-->

# Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">T-ITS</div><img src='images/projects/RETA.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[RETA: 4D Radar-based End-to-End Joint Tracking and Activity Estimation for Low-Observable Pedestrian Safety
in Cluttered Traffic Scenarios](https://ieeexplore.ieee.org/document/10285516)

IEEE Transactions on Intelligent Transportation Systems

> The paper proposes RETA, it enhances weak-target localization via an integrated detection–tracking algorithm using raw unthresholded radar measurements, and performs continuous activity recognition with a decomposed DC-RCNN and CTC without manual pre-segmentation.

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IoT-J</div><img src='images/projects/STIF.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[STIF: A Spatial–Temporal Integrated Framework for End-to-End Micro-UAV Trajectory Tracking and Prediction With 4-D MIMO Radar](https://ieeexplore.ieee.org/document/10044147)

IEEE Internet of Things Journal

> The paper proposes STIF, a spatial–temporal integrated trajectory tracking and prediction framework for micro-UAVs, which combines a PF-TBD joint detection–tracking algorithm with an intention-aware Transformer prediction model to exploit long-sequence spatial–temporal dependencies and enhance both tracking and prediction performance. 
</div>
</div>

- [Pedestrian Detection and Trajectory-Tracking based FMCW radar For Autonomous Driving](https://ieeexplore.ieee.org/document/10401665), 2023 38th Youth Academic Annual Conference of Chinese Association of Automation (YAC), Oral, Best Student Paper Award-Finalist.

- 15 篇发明专利

# Awards

# Others