---
layout: project
title: motVidarReal2020
image: images/dataset_image/motvidar2020.gif
tags:
  - multi-object tracking
  - high-speed
  - real
  - dataset
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: a multi-object tracking dataset based on event cameras, primarily focused on tracking digit targets.
Data characteristics:
- Sampling rate: up to 20 kHz (20,000 fps)
- Temporal resolution: 300-600 times higher than conventional cameras
- Data format: binary spike event streams

### Technical Advantages
- No exposure-time limitation
- Avoids motion blur
- Particularly suitable for high-speed motion scenarios
- Microsecond-level temporal resolution for capturing instantaneous motion details

### Supported Tasks
- High-speed object tracking
- Event-stream reconstruction
- Cross-modal research
- Practical applications such as autonomous driving
- Digit target detection and tracking

### Key Features
- Ultra-high sampling: 20 kHz sampling rate for fast motion capture
- Multi-object scenes: includes complex scenes with multiple moving targets
- Real-world data: real spike sequences collected with a Vidar camera
- Suitable for real-time applications: low-latency data output supports online tracking algorithms

Dataset link: https://openi.pcl.ac.cn/Cordium/SpikeCV/datasets?page=2

{% include figure.html image="/images/dataset_image/motvidar2020.gif" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：基于事件相机的多目标跟踪数据集，主要关注数字目标的跟踪。
数据特性：
- 采样率：高达20kHz（20000fps）
- 时间分辨率：比传统相机提升300-600倍
- 数据格式：二进制spike事件流

### 技术优势
- 不受曝光时间限制
- 避免运动模糊
- 特别适合高速运动场景
- 微秒级时间分辨率，捕捉瞬时运动细节

### 可支持的任务：
- 高速运动目标跟踪
- 事件流重建算法
- 跨模态研究
- 自动驾驶等实际应用场景
- 数字目标检测与追踪

### 关键特性
- 超高速采样：20kHz采样率，捕捉高速运动细节
- 多目标场景：包含多个运动目标的复杂场景
- 真实世界数据：基于Vidar相机采集的真实场景脉冲序列
- 适合实时应用：低延迟数据输出，支持实时跟踪算法

数据集链接：https://openi.pcl.ac.cn/Cordium/SpikeCV/datasets?page=2

{% include figure.html image="/images/dataset_image/motvidar2020.gif" width="100%" %}
</div>
