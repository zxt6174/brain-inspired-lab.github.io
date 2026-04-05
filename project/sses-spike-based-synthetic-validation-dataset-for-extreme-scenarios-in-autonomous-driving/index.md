---
layout: project
title: SSES (Spike-based Synthetic validation dataset for Extreme Scenarios in autonomous driving)
image: images/dataset_image/sses.png
tags:
  - optical flow
  - simulate
  - dataset
  - autonomous driving
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: a synthetic spike-camera dataset focused on extreme autonomous-driving scenarios, supporting the training and evaluation of unsupervised optical-flow estimation models.

Scene categories: 10 extreme scenarios simulating traffic accidents, covering a variety of street environments, weather conditions (rain and fog), and moving targets (vehicles and pedestrians/cyclists).

Data format: spike streams are generated at 40 kHz for microsecond-level optical-flow analysis; the dataset includes multimodal data such as spikes, RGB frames, optical-flow ground truth, instance segmentation, and depth.

Dataset scale: built on the CARLA simulator, with each sequence lasting 0.5-1.5 seconds.

### Why This Dataset Matters
- Fills an important gap: provides the first synthetic dataset for validating spike-camera algorithms in extreme autonomous-driving scenarios.
- Promotes unsupervised learning: supports the training and evaluation of unsupervised optical-flow estimation models, reducing reliance on real annotated data.
- Improves robustness: diverse extreme-scene design helps models adapt to complex dynamic environments and supports safety-critical applications.

### Data Generation Pipeline
1. Build diverse scenes with the CARLA simulator.
2. Render RGB frames at 500 fps.
3. Increase the temporal rate to 40 kHz through optical-flow interpolation.
4. Simulate the "integrate-and-fire" mechanism of spike cameras.
5. Provide ground truth for optical flow, instance segmentation, and depth.

### Dataset Advantages
- High dynamics: fast motion of vehicles and pedestrians simulates real emergency situations.
- Multimodal data: includes spike streams, RGB frames, optical-flow ground truth, instance segmentation, and depth information.
- Coverage of extreme scenarios: focuses on high-risk scenes such as traffic accidents, filling a gap left by existing real datasets.
- High temporal resolution: spike streams generated at 40 kHz support microsecond-level optical-flow analysis.

### Supported Tasks
- Unsupervised optical-flow estimation: reduce dependence on real annotated data.
- High-speed object detection and tracking: perceive targets under extreme conditions.
- Autonomous-driving perception: improve perception in complex and dynamic environments.

Dataset link: not public.

{% include figure.html image="/images/dataset_image/sses_result.png" caption="Results of the proposed method in the associated paper on this dataset" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：专注于自动驾驶极端场景的脉冲相机合成数据集，支持无监督光流估计模型的训练与评估。

场景类别：10个模拟交通事故的极端场景，涵盖各种街道环境、天气条件（雨天、雾天）和运动目标（车辆、行人/骑行者）。

数据格式：脉冲流以40kHz生成，支持微秒级光流分析；包含脉冲流、RGB帧、光流真值、实例分割和深度信息的多模态数据。

数据规模：基于CARLA模拟器构建，每个数据序列持续0.5-1.5秒。

### 数据集意义
- 填补空白：为脉冲相机在自动驾驶极端场景下的算法验证提供了首个合成数据集
- 推动无监督学习：支持无监督光流估计模型的训练与评估，减少对真实标注数据的依赖
- 提升鲁棒性：通过多样化极端场景设计，帮助模型适应复杂动态环境，推动安全关键应用的发展

### 数据生成方法
1. 基于CARLA模拟器构建多样场景
2. 以500fps渲染RGB帧
3. 通过光流插值将帧率提升至40kHz
4. 模拟脉冲相机的"积分-发射"机制
5. 提供光流、实例分割和深度信息的地面真实值

### 数据集优势
- 高动态性：车辆和行人的高速运动，模拟真实世界的紧急情况
- 多模态数据：包含脉冲流、RGB帧、光流地面真实值、实例分割和深度信息
- 极端场景覆盖：专注于高风险场景，如交通事故，填补真实数据集的空白
- 高时间分辨率：脉冲流以40kHz生成，支持微秒级光流分析

### 可支持的任务：
- 无监督光流估计：减少对真实标注数据的依赖
- 高速目标检测与跟踪：在极端场景下的目标感知
- 自动驾驶环境感知：提升复杂动态环境中的感知能力

数据集链接：未公开

{% include figure.html image="/images/dataset_image/sses_result.png" caption="文章所提算法在此数据集上的结果" width="100%" %}
</div>
