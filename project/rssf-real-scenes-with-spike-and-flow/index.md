---
layout: project
title: RSSF(Real Scenes with Spike and Flow)
image: images/dataset_image/rssf_1024_optimized.gif
tags:
  - optical flow
  - simulate
  - dataset
collaborators: 
collaborator_icons: []
---
<style>
@media (max-width: 860px) {
  .rssf-grid { grid-template-columns: 1fr !important; }
}
</style>

<div data-lang-target="en">
  <div class="dataset-features">
    <h4>Challenges Addressed</h4>
    <ul>
      <li><strong>The gap between synthetic data and real scenes:</strong> conventional synthetic data, such as the graphics-model data used by SCFlow, often suffer from unrealistic textures, simplified lighting, and limited motion patterns, which leads to weak generalization in real scenes. RSSF significantly narrows this gap by simulating spike streams from the real high-resolution Slow Flow dataset.</li>
      <li><strong>Temporal continuity modeling of spike streams:</strong> spike cameras output continuous binary spike streams, and each individual spike reflects an integrated result rather than an instantaneous state. Traditional methods therefore struggle to capture spatiotemporal correlations. RSSF supports continuous-motion modeling with multi-interval optical-flow ground truth (dt=20, 40, 60), addressing the underuse of temporal information.</li>
      <li><strong>The difficulty of labeling real spike data:</strong> it is hard to directly annotate optical flow for real spike-camera data. RSSF bypasses this bottleneck by generating spike streams and optical-flow ground truth through simulation with strict correspondence.</li>
    </ul>
  </div>

  <div class="rssf-grid" style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px; align-items: start;">
    <div>
      <h3>Dataset Basics</h3>
      <ul>
        <li>Foundation: built on the Slow Flow dataset, containing 41 real-world scenes and supporting multi-scale optical-flow estimation</li>
        <li>Temporal resolution: 20 interpolation steps between adjacent frames</li>
        <li>Data split:
          <ul>
            <li>Training set: 30 scenes with different resolutions and spike-frame counts, totaling 9.64k+ optical-flow fields and 193k+ spike frames</li>
            <li>Test set: 11 scenes, with the first 200 optical-flow fields from each scene, totaling 2.2k optical-flow fields and 44.22k spike frames</li>
          </ul>
        </li>
      </ul>
    </div>

    <div>
      {% include figure.html image="/images/dataset_image/rssf_statistics.png" width="100%" %}
    </div>
  </div>

  <div class="dataset-features">
    <h4>Data Format, Structure, and Label Definition</h4>
    <ul>
      <li><strong>Input data (spike streams):</strong>
        <ul>
          <li>Format: a 3D binary tensor of shape H×W×T, where T is the temporal length.</li>
          <li>Storage: typically stored in `.dat` format.</li>
        </ul>
      </li>
      <li><strong>Labels (optical-flow ground truth):</strong>
        <ul>
          <li>Format: an H×W×2 floating-point tensor, where each pixel contains horizontal displacement <code>u</code> and vertical displacement <code>v</code>.</li>
          <li>Temporal span: each sample provides optical-flow fields for three intervals: dt=20, 40, and 60.</li>
          <li>Generation: optical flow is estimated from high-resolution image sequences using the GMA network and then aligned with spike streams through motion simulation.</li>
        </ul>
      </li>
      <li><strong>RSSF directory structure:</strong>
        <code style="cursor: pointer;"
          onclick="if(this.classList.contains('expanded')) { this.classList.remove('expanded'); this.innerHTML=`<pre style='margin: 0; padding: 0;'>RSSF<br>├── imgs<br>└── spike</pre>`; } else { this.classList.add('expanded'); this.innerHTML=`<pre style='margin: 0; padding: 0;'>RSSF<br>├── imgs<br>│   ├── train<br>│   │   ├── horses__000000<br>│   │   │   ├── 0000136.png<br>│   │   │   ├── 0000137.png<br>│   │   │   └── ...<br>│   │   ├── kids__000000<br>│   │   │   └── ...<br>│   │   └── ...<br>│   └── test<br>│       └── ...<br>└── spike<br>    ├── train<br>    │   ├── horses__000000<br>    │   │   └── *.dat<br>    │   ├── kids__000000<br>    │   │   └── *.dat<br>    │   └── ...<br>    └── test<br>        └── ...</pre>`; }">
          <pre style="margin: 0; padding: 0;">
RSSF
├── imgs
└── spike</pre>
        </code>
      </li>
    </ul>
  </div>

  {% include figure.html image="/images/dataset_image/rssf_train.png" caption="Samples from the training set" width="100%" %}
  {% include figure.html image="/images/dataset_image/rssf_test.png" caption="Samples from the test set" width="100%" %}
</div>

<div data-lang-target="zh" hidden>
  <div class="dataset-features">
    <h4>解决的困难与挑战</h4>
    <ul>
      <li><strong>合成数据与真实场景的差距：</strong>传统合成数据（如SCFlow使用的图形模型数据）存在纹理不真实、光照简化、运动模式单一等问题，导致模型在真实场景中泛化能力差。RSSF通过基于真实高分辨率数据集（Slow Flow）模拟脉冲流，显著缩小了这一差距。</li>
      <li><strong>脉冲流的时间连续性建模：</strong>脉冲相机输出的是连续二进制脉冲流，单个脉冲仅反映积分结果而非瞬时状态，传统方法难以提取时空关联特征。RSSF通过多时间步长光流真值（dt=20,40,60）支持连续运动建模，解决了时间信息利用不足的问题。</li>
      <li><strong>真实数据标注难题：</strong>脉冲相机的真实数据难以直接标注光流。RSSF通过模拟生成脉冲流与光流真值的严格对应关系，绕过了真实数据标注的瓶颈。</li>
    </ul>
  </div>

  <div class="rssf-grid" style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px; align-items: start;">
    <div>
      <h3>数据集基础</h3>
      <ul>
        <li>数据基础：基于 Slow Flow 数据集，含 41 个真实世界场景，支持多尺度光流估计</li>
        <li>时间分辨率：帧间插值 20 步</li>
        <li>数据划分：
          <ul>
            <li>训练集：30 个场景，不同分辨率与脉冲帧数，共 9.64k+ 光流场，193k+ 脉冲帧</li>
            <li>测试集：11 个场景，每场景前 200 个光流场，共 2.2k 光流场，44.22k 脉冲帧</li>
          </ul>
        </li>
      </ul>
    </div>

    <div>
      {% include figure.html image="/images/dataset_image/rssf_statistics.png" width="100%" %}
    </div>
  </div>

  <div class="dataset-features">
    <h4>数据集结构格式与标签定义</h4>
    <ul>
      <li><strong>输入数据（脉冲流）：</strong>
        <ul>
          <li>格式：H×W×T 的三维二进制张量（T为时间步长）。</li>
          <li>存储方式：可能以dat格式存储</li>
        </ul>
      </li>
      <li><strong>标签（光流真值）：</strong>
        <ul>
          <li>格式：H×W×2 的浮点张量，每个像素包含水平位移 u 和垂直位移 v。</li>
          <li>时间跨度：每个样本对应 dt=20,40,60 三种时间间隔的光流场。</li>
          <li>生成方式：通过GMA网络从高分辨率图像序列中估计光流，并通过运动模拟确保与脉冲流的严格对齐。</li>
        </ul>
      </li>
      <li><strong>RSSF 数据集目录结构：</strong>
        <code style="cursor: pointer;"
          onclick="if(this.classList.contains('expanded')) { this.classList.remove('expanded'); this.innerHTML=`<pre style='margin: 0; padding: 0;'>RSSF<br>├── imgs<br>└── spike</pre>`; } else { this.classList.add('expanded'); this.innerHTML=`<pre style='margin: 0; padding: 0;'>RSSF<br>├── imgs<br>│   ├── train<br>│   │   ├── horses__000000<br>│   │   │   ├── 0000136.png<br>│   │   │   ├── 0000137.png<br>│   │   │   └── ...<br>│   │   ├── kids__000000<br>│   │   │   └── ...<br>│   │   └── ...<br>│   └── test<br>│       └── ...<br>└── spike<br>    ├── train<br>    │   ├── horses__000000<br>    │   │   └── *.dat<br>    │   ├── kids__000000<br>    │   │   └── *.dat<br>    │   └── ...<br>    └── test<br>        └── ...</pre>`; }">
          <pre style="margin: 0; padding: 0;">
RSSF
├── imgs
└── spike</pre>
        </code>
      </li>
    </ul>
  </div>

  {% include figure.html image="/images/dataset_image/rssf_train.png" caption="训练集抽样展示" width="100%" %}
  {% include figure.html image="/images/dataset_image/rssf_test.png" caption="测试集抽样展示" width="100%" %}
</div>
