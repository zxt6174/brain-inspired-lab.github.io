---
layout: project
title: DENSE-spike and Outdoor-spike
image: images/dataset_image/Outdoor-spike.png
tags:
  - depth estimation
  - monocular
  - spike camera
  - dataset
  - autonomous driving
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: monocular depth-estimation datasets for spike cameras, covering both synthetic environments and real-world scenes.
Scene categories:
- DENSE-spike: diverse scenes generated with the CARLA simulator, including different weather and lighting conditions
- Outdoor-spike: real road scenes captured from a driving perspective
Data format:
- DENSE-spike: spike-stream data at 346×260×128 (128 timestamps)
- Outdoor-spike: real spike-stream data at 400×250@40kHz
Dataset scale:
- DENSE-spike: 8 sequences (5 training / 2 validation / 1 test)
- Outdoor-spike: 33 real road-scene sequences

### Data Generation and Acquisition
- DENSE-spike: generated from base scenes in the CARLA simulator; video frame rate is increased to 3840 fps and then converted into spike streams through a dedicated algorithm
- Outdoor-spike: collected with a professional Vidar spike camera, including natural noise and real illumination changes

### Supported Tasks
- Monocular depth estimation: recover depth information from a single-channel spike stream
- Cross-domain transfer: transfer from synthetic data to real-world scenes
- Autonomous-driving perception: depth estimation from realistic driving viewpoints

### Key Features
- DENSE-spike: provides accurate depth labels across diverse weather and lighting conditions
- Outdoor-spike: real-world data with natural noise and actual lighting variation
- Complementarity: the two datasets complement each other and support validation of generalization from synthetic to real data

Dataset links:

DENSE-spike https://pan.baidu.com/s/1Lg2spMW4OYlsYy0iT4u_7g (password:1008).

Outdoor-spike https://pan.baidu.com/s/1hji5GnFH5Ke_nDt-1Q76rg (password:1997).

{% include figure.html image="/images/dataset_image/dense-spike-result.png" caption="Examples from the DENSE-spike dataset" width="100%" %}
{% include figure.html image="/images/dataset_image/outdoor-spike-result.png" caption="Examples from the Outdoor-spike dataset" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：为脉冲相机提供单目深度估计数据集，涵盖合成环境和真实世界场景。
场景类别：
- DENSE-spike：基于CARLA模拟器生成的多样化场景，包括不同天气和光照条件
- Outdoor-spike：真实道路场景，模拟自动驾驶视角
数据格式：
- DENSE-spike：346×260×128(128个时间戳)的脉冲流数据
- Outdoor-spike：400×250@40kHz的真实脉冲流数据
数据规模：
- DENSE-spike：8个序列(5训练/2验证/1测试)
- Outdoor-spike：33个真实道路场景序列

### 数据生成与采集
- DENSE-spike：基于CARLA模拟器生成基础场景，将视频帧率提升至3840fps，通过专业算法转换为脉冲流数据
- Outdoor-spike：使用专业Vidar脉冲相机采集，包含自然噪声和实际光照变化

### 可支持的任务：
- 单目深度估计：从单通道脉冲流中恢复深度信息
- 跨域迁移：从合成数据迁移到真实场景
- 自动驾驶环境感知：模拟真实自动驾驶视角的深度估计

### 关键特性
- DENSE-spike：包含高精度深度标签，覆盖多样的天气和光照条件
- Outdoor-spike：真实环境数据，包含自然噪声和实际光照变化
- 互补性：两个数据集相互补充，支持模型从合成到真实的泛化能力验证

数据集链接：

DENSE-spike https://pan.baidu.com/s/1Lg2spMW4OYlsYy0iT4u_7g (password:1008).

Outdoor-spike  https://pan.baidu.com/s/1hji5GnFH5Ke_nDt-1Q76rg (password:1997).

{% include figure.html image="/images/dataset_image/dense-spike-result.png" caption="DENSE-spike数据集示例" width="100%" %}
{% include figure.html image="/images/dataset_image/outdoor-spike-result.png" caption="Outdoor-spike数据集示例" width="100%" %}
</div>
