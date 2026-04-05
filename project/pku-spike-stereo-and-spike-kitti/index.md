---
layout: project
title: PKU-Spike-Stereo and Spike-KITTI
image: images/dataset_image/pku-spike-stereo-result.png
tags:
  - depth estimation
  - stereo
  - spike camera
  - dataset
collaborators: 
collaborator_icons: []
---

<div data-lang-target="en" markdown="1">
Purpose: stereo depth-estimation datasets for spike cameras, covering both real scenes and simulated environments.

Scene categories: PKU-Spike-Stereo contains indoor and outdoor scenes; Spike-KITTI is converted from the KITTI dataset and preserves road-scene characteristics.

Data format:
- PKU-Spike-Stereo: a dual-spike-camera system (400×250 resolution, 20 kHz sampling rate) synchronized with a ZED depth camera (1280×720@30 fps)
- Spike-KITTI: converts classic KITTI videos into spike-stream format

Dataset scale:
- PKU-Spike-Stereo: 10,750 pairs of spike-stream samples and 877 sets of high-quality synchronized depth labels
- Spike-KITTI: 200 stereo pairs (160 for training / 40 for testing)

### Dataset Structure
The PKU-Spike-Stereo dataset provides precise spatiotemporal alignment. Through dedicated image registration, the spike streams and depth maps are tightly synchronized, making the dataset particularly suitable for depth estimation of high-speed moving objects.

### Supported Tasks
- Stereo depth estimation: compute depth with a dual-spike-camera system
- Cross-modal fusion: combine spike streams with conventional camera data to improve depth-estimation accuracy
- High-speed motion depth estimation: overcome motion blur from conventional cameras in fast scenes

### Key Features
- Precise spatiotemporal alignment: high-accuracy synchronization between spike streams and depth maps
- Rich scene diversity: covers multiple indoor and outdoor scenes
- Large sample size: provides sufficient data for training and evaluation
- Optimized for high-speed motion: particularly suitable for depth estimation of fast-moving objects

Dataset link: not yet public. Related paper: https://www.jdl.link/doc/2011/20221228_Learning_Stereo_Depth_Estimation_with_Bio-Inspired_Spike_Cameras.pdf

{% include figure.html image="/images/dataset_image/pku-spike-stereo.png" caption="Structure of the PKU-Spike-Stereo dataset" width="100%" %}
{% include figure.html image="/images/dataset_image/kitti-result.png" caption="Evaluation results on the Spike-KITTI dataset" width="100%" %}
{% include figure.html image="/images/dataset_image/in1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/in2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/in3.gif" caption="Sample indoor cases" width="100%" %}
{% include figure.html image="/images/dataset_image/out1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/out2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/out3.gif" caption="Sample outdoor cases" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
用途：为脉冲相机提供立体深度估计数据集，涵盖真实场景和模拟环境。

场景类别：PKU-Spike-Stereo包含室内和室外场景；Spike-KITTI基于KITTI数据集转换，保留道路场景特征。

数据格式：
- PKU-Spike-Stereo：双脉冲相机系统(400×250分辨率，20kHz采样率)，与ZED深度相机(1280×720@30fps)同步
- Spike-KITTI：将经典KITTI数据集视频转换为脉冲流格式

数据规模：
- PKU-Spike-Stereo：10,750对脉冲流数据，877组高质量同步深度标签
- Spike-KITTI：200对立体图像(160训练/40测试)

### 数据集结构
PKU-Spike-Stereo数据集提供精确的时空对齐，通过专业图像配准实现脉冲流与深度图的精确同步，特别适合高速运动物体的深度估计。

### 可支持的任务：
- 立体深度估计：利用双脉冲相机系统进行深度计算
- 跨模态融合：结合脉冲流与传统相机数据提高深度估计精度
- 高速运动深度估计：克服传统相机在高速场景下的运动模糊问题

### 关键特性
- 精确的时空对齐：脉冲流与深度图的高精度同步
- 丰富的场景类型：室内/室外多种场景覆盖
- 大样本量：提供充足的训练和测试数据
- 高速运动优化：特别适合快速移动物体的深度估计

数据集链接：尚未公开，文章链接为 https://www.jdl.link/doc/2011/20221228_Learning_Stereo_Depth_Estimation_with_Bio-Inspired_Spike_Cameras.pdf

{% include figure.html image="/images/dataset_image/pku-spike-stereo.png" caption="PKU-Spike-Stereo数据集结构" width="100%" %}
{% include figure.html image="/images/dataset_image/kitti-result.png" caption="Spike-KITTI数据集测试结果" width="100%" %}
{% include figure.html image="/images/dataset_image/in1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/in2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/in3.gif" caption="室内抽样案例" width="100%" %}
{% include figure.html image="/images/dataset_image/out1.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/out2.gif" width="100%" %}
{% include figure.html image="/images/dataset_image/out3.gif" caption="室外抽样案例" width="100%" %}
</div>
