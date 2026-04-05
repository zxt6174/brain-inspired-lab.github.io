---
layout: project
title: momVidarReal2021
image: images/dataset_image/Bananas_1.gif
tags:
  - high-speed
  - real
  - dataset
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: a high-speed vision dataset containing 51 real-scene spike sequences, designed to support algorithm research and development.

Scene categories:
- Ball-motion scenes: 13 sequences (badminton, table tennis, football, basketball, tennis, etc.)
- Complex-motion scenes: 8 sequences (drones, multiple moving balls, playing cards with ping-pong balls, etc.)
- Special scenes: 8 sequences (rotating characters, laser points, etc.)
- Daily-life scenes: 22 sequences (fruits and various household objects, etc.)

Data characteristics:
- Image resolution: 400×250
- Sampling frequency: 20,000 Hz
- Data format: binary spike event streams

### Dataset Structure
The dataset contains 12 subcategories and a total of 51 sequences. Each sequence corresponds to one video clip, and the structured organization is convenient for research and development.

### Supported Tasks
- Image reconstruction: reconstruct high-speed motion scenes from spike streams
- High-speed object detection and tracking: detect and track fast-moving objects
- Motion analysis: motion segmentation, optical-flow estimation, trajectory analysis, and related tasks
- Camera ego-motion analysis: study how camera motion affects imaging and develop motion-compensation algorithms
- Multi-object interaction analysis: analyze occlusions and interactions among multiple objects

### Key Features
- Ultra-high sampling rate: 20,000 Hz for capturing transient motion details
- Diverse scenes: includes ball-motion, complex-motion, special, and daily-life scenes
- Real-world data: entirely captured from real complex scenes, avoiding the gap between synthetic and real data
- Rich sequence coverage: 51 sequences provide ample data for training and testing
- Addresses high-speed motion challenges: mitigates motion blur caused by the low frame rate of conventional cameras

Dataset link: https://openi.pcl.ac.cn/Cordium/SpikeCV/datasets?page=2

{% include figure.html image="/images/dataset_image/Badminton_HitNet2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Bananas_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Basketball_2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/DroneAndBalls_3.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Flying-Rotation-Ego.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/FlyingBalls.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/FlyingPokerPingpong.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Football_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Keyboard_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LaserPoint_5-1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LaserPoint_Matrix.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LifeScene_1-1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Orange_.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Pingpong_Serve.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Tennisball_2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/interval_method.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/window_method.gif" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：包含51段真实场景脉冲序列的高速视觉数据集，用于促进算法研究和开发。

场景类别：
- 运动球类场景：13个序列（羽毛球、乒乓球、足球、篮球、网球等）
- 复杂运动场景：8个序列（无人机、多球运动、纸牌与乒乓球等）
- 特殊场景：8个序列（旋转字符、激光点等）
- 生活场景：22个序列（水果和各种生活用品等）

数据特性：
- 图像分辨率：400×250
- 采样频率：20,000 Hz
- 数据格式：二进制spike事件流

### 数据集结构
数据集包含12个子类别，共51个序列，每个序列代表一段视频片段，采用结构化组织便于研究和开发。

### 可支持的任务：
- 图像重建：从脉冲流重建高速运动场景
- 高速目标检测与追踪：检测和跟踪高速运动物体
- 运动分析：运动分割、光流估计、运动轨迹分析等
- 相机自运动研究：研究相机运动对成像的影响，开发运动补偿算法
- 多物体交互分析：分析多物体间的遮挡与交互

### 关键特性
- 超高速采样率：20,000Hz，捕捉瞬态运动细节
- 多样化场景：涵盖运动球类、复杂运动、特殊场景和生活场景
- 真实世界数据：全实拍复杂场景，避免合成数据与真实场景的差距
- 丰富的序列数量：51个序列，提供充足的训练和测试数据
- 解决高速运动挑战：克服传统相机帧率低导致的运动模糊问题

数据集链接：https://openi.pcl.ac.cn/Cordium/SpikeCV/datasets?page=2

{% include figure.html image="/images/dataset_image/Badminton_HitNet2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Bananas_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Basketball_2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/DroneAndBalls_3.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Flying-Rotation-Ego.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/FlyingBalls.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/FlyingPokerPingpong.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Football_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Keyboard_1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LaserPoint_5-1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LaserPoint_Matrix.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/LifeScene_1-1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Orange_.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Pingpong_Serve.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/Tennisball_2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/interval_method.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/window_method.gif" width="100%" %}
</div>
