---
layout: project
title: PKU-Vidar-DVS
image: images/dataset_image/pku-vidar-dvs-result.png
tags:
  - object detection
  - multi-modal
  - spike camera
  - dataset
  - high-speed
  - low-light
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: a multimodal asynchronous object-detection dataset for spike cameras, designed for high-speed object detection, low-light perception, and validation of multimodal fusion algorithms.

Scene categories: diverse scenes involving high-speed motion, low-light conditions, and complex backgrounds across both indoor and outdoor environments.

Data format:
- Vidar (fovea-like vision): spikes at 400×250 resolution and 20,000 Hz sampling rate
- DVS (peripheral-like vision): asynchronous events, 12 million events per second, with microsecond-level temporal resolution

Dataset scale: 490 sequences (about 5 seconds each), annotated at 50 Hz, with 215.5k bounding boxes covering 9 object categories.

### Core Characteristics
Multimodal asynchronous data: combines the static texture information of Vidar with the dynamic response of DVS to provide complementary visual cues.

High spatiotemporal resolution: Vidar provides high-frequency texture information, while DVS provides microsecond-level temporal resolution, making the dataset suitable for high-speed object detection.

Challenging scene coverage: includes fast motion (such as rotating characters at 1500 r/min), low-light environments (tunnels and night scenes), and scenes with strong dynamic-range conflicts.

### Data Format and Directory Structure
- DVS data: event-stream format containing x/y coordinates, polarity, and timestamps
- Vidar data: `.dat` format, where each pixel uses 8 bits to represent a time bin
- Label data: each row corresponds to one annotated frame and includes bounding-box coordinates and category IDs

### Supported Tasks
- Asynchronous multimodal object detection: jointly exploit Vidar and DVS data
- High-speed object detection: capture fast-moving targets with high temporal resolution
- Low-light perception: evaluate algorithm performance under extreme lighting conditions
- Multimodal fusion: explore effective ways to fuse different sensing modalities

Dataset link: https://git.openi.org.cn/lijianing/PKU-Vidar-DVS/datasets

{% include figure.html image="/images/dataset_image/pku-vidar-dvs-compare.png" caption="Comparison of dataset parameters" width="100%" %}
{% include figure.html image="/images/dataset_image/pku-vidar-dvs-see-result.png" caption="Visualization samples from the dataset" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：为脉冲相机提供多模态异步目标检测数据集，用于高速物体检测、低光环境感知和多模态融合算法验证。

场景类别：包含高速运动、低光照条件、复杂背景等多样化场景，覆盖室内和室外环境。

数据格式：
- Vidar(类中央凹视觉): 尖峰流(Spikes)，400×250分辨率，20,000Hz采样率
- DVS(类周边视觉): 异步事件流(Events)，每秒1200万事件，微秒级时间分辨率

数据规模：490段序列(每段约5秒)，50Hz标注频率，总标注框数达215.5k，覆盖9类物体。

### 数据集核心特点
多模态异步数据：结合Vidar的静态纹理信息和DVS的动态响应特性，提供互补的视觉信息。

高时空分辨率：Vidar提供高频纹理信息，DVS提供微秒级时间分辨率，适应高速运动物体检测。

挑战性场景覆盖：包含高速运动(如1500r/min旋转字符)、低光照环境(隧道、夜间)和动态范围冲突场景。

### 数据格式和目录结构
- DVS数据：事件流格式，包含x/y坐标、极性和时间戳
- Vidar数据：.dat文件格式，每个像素8位代表时间bin
- 标签数据：每行代表一帧标注，包含边界框坐标和类别ID

### 可支持的任务：
- 异步多模态目标检测：联合利用Vidar和DVS数据
- 高速运动物体检测：利用高时间分辨率捕捉快速移动目标
- 低光照环境感知：验证算法在极端光照条件下的性能
- 多模态融合算法开发：探索不同模态数据的有效融合方式

数据集链接：https://git.openi.org.cn/lijianing/PKU-Vidar-DVS/datasets

{% include figure.html image="/images/dataset_image/pku-vidar-dvs-compare.png" caption="不同数据集参数对比" width="100%" %}
{% include figure.html image="/images/dataset_image/pku-vidar-dvs-see-result.png" caption="数据集可视化抽样" width="100%" %}
</div>
