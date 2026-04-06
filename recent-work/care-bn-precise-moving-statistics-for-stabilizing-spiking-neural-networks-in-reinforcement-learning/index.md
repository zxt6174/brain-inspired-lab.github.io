---
layout: project
title: "CaRe-BN: Precise Moving Statistics for Stabilizing Spiking Neural Networks in Reinforcement Learning"
section_title: Recent work
section_title_key: recent_work_title
section_link: /recent-work/
tags:
  - spiking neural networks
  - reinforcement learning
  - batch normalization
---

*Zijie Xu, Xinyu Shi, Yiting Dong, Zihan Huang, Zhaofei Yu*. CaRe-BN: Precise Moving Statistics for Stabilizing Spiking Neural Networks in Reinforcement Learning. The Fourteenth International Conference on Learning Representations (ICLR), 2026.*

<div data-lang-target="en" markdown="1">
[Read the paper](https://openreview.net/forum?id=AaZVrbElhC)

## Research Background and Problem

### Background

Spiking Neural Networks (SNNs) provide highly energy-efficient and low-latency decision-making capabilities by mimicking the event-driven dynamics of biological neurons, making them ideal for neuromorphic hardware.

### Limitation of Existing Methods

However, traditional Batch Normalization (BN) suffers a severe breakdown in online Reinforcement Learning (RL) because moving statistics cannot be accurately estimated under continually shifting data distributions, leading to unstable training and suboptimal policies.

### Our Perspective

To overcome these challenges, we propose Confidence-adaptive and Re-calibration Batch Normalization (CaRe-BN), a novel normalization strategy tailored specifically to provide precise statistics and stabilize SNN-based RL without disrupting the training process.

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/background-problem.png" width="100%" %}

## Contributions

- Introduces Ca-BN (Confidence-adaptive update), a confidence-weighted moving estimator that dynamically adjusts statistics estimation based on the reliability of the current approximation to ensure unbiasedness and reduce variance.
- Introduces Re-BN (Re-calibration), a periodic correction scheme that leverages replay buffer resampling to refine inference statistics and correct accumulated estimation errors.
- Maintains the inherent energy efficiency of SNNs; the CaRe-BN layer is seamlessly fused into synaptic weights after training, introducing zero additional inference overhead during deployment.
- Achieves state-of-the-art results, improving SNN performance by up to 22.6% across different spiking neuron models and RL algorithms, and remarkably outperforming Artificial Neural Network (ANN) counterparts by 5.9%.

## Core Method

The CaRe-BN framework integrates two complementary mechanisms to enable precise, low-variance estimation of BN statistics under the nonstationary dynamics of RL. First, the Ca-BN module is applied at every update step, acting as a confidence-guided mechanism that adaptively reweights estimators to minimize the mean-squared error of BN statistics when distribution shifts occur. Second, because online estimates may still drift due to stochastic mini-batch noise, the Re-BN module is executed periodically. It draws aggregated calibration batches from the replay buffer to compute exact statistics, effectively correcting accumulated bias without requiring millions of forward passes.

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/core-method.png" width="100%" %}

## Representative Results

Extensive evaluations across discrete action spaces (Atari benchmarks) and continuous control tasks (MuJoCo suite) demonstrate that CaRe-BN significantly resolves the issue of imprecise moving statistics. SNN-based agents equipped with CaRe-BN consistently achieved higher exploration returns, converged faster, and exhibited significantly lower variance compared to standard SNNs. Notably, when paired with the TD3 algorithm, CaRe-BN allowed simple SNNs to surpass the performance of traditional ANN-based RL agents by an average of 5.9%, establishing a new state-of-the-art normalization strategy that bridges the gap between neuromorphic efficiency and high-performance RL.

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/representative-results.png" width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
[查看原文](https://openreview.net/forum?id=AaZVrbElhC)

## 研究背景与问题

### 背景

脉冲神经网络（SNN）通过模拟生物神经元的事件驱动动态，具备高能效、低时延的决策能力，因此非常适合部署在神经形态硬件上。

### 现有方法的局限

然而，传统批归一化（BN）在在线强化学习（RL）场景中会出现明显失效，因为面对持续变化的数据分布，移动统计量难以被准确估计，进而导致训练不稳定以及策略性能不理想。

### 我们的思路

为解决这些问题，我们提出了 Confidence-adaptive and Re-calibration Batch Normalization（CaRe-BN），这是一种专门面向 SNN 强化学习场景设计的新型归一化策略，能够在不打断训练流程的前提下提供更精确的统计量并稳定训练过程。

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/background-problem.png" width="100%" %}

## 创新点

- 提出 Ca-BN（置信度自适应更新）机制，通过置信度加权的移动估计器，根据当前近似结果的可靠性动态调整统计量估计，从而保证无偏性并降低方差。
- 提出 Re-BN（重校准）机制，利用经验回放缓冲区的重采样周期性修正推理统计量，并纠正累积的估计误差。
- 保持了 SNN 原有的高能效特性；CaRe-BN 层在训练完成后可以无缝融合进突触权重，部署时不会带来额外推理开销。
- 在不同脉冲神经元模型和强化学习算法上取得当前最优结果，SNN 性能最高提升 22.6%，并显著超过 ANN 强化学习基线 5.9%。

## 核心方法

CaRe-BN 框架通过两个互补机制，在强化学习的非平稳动态环境下实现对 BN 统计量的精确、低方差估计。首先，Ca-BN 模块在每次更新时都会执行，作为一种基于置信度引导的机制，在分布发生漂移时自适应地重加权估计器，以最小化 BN 统计量的均方误差。其次，考虑到在线估计仍可能因随机小批量噪声而发生漂移，Re-BN 模块会周期性执行。它从经验回放缓冲区中抽取聚合后的校准批次来计算更精确的统计量，从而在不需要数百万次前向传播的前提下有效修正累积偏差。

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/core-method.png" width="100%" %}

## 代表性结果

在离散动作空间（Atari 基准）和连续控制任务（MuJoCo 套件）上的广泛实验表明，CaRe-BN 能够显著缓解移动统计量不精确的问题。配备 CaRe-BN 的 SNN 智能体在探索回报、收敛速度和方差表现上均优于标准 SNN。尤其是在与 TD3 算法结合时，CaRe-BN 使简单 SNN 的平均性能超过传统基于 ANN 的强化学习智能体 5.9%，建立了一种连接神经形态高能效与高性能强化学习的新型归一化策略。

{% include figure.html image="/images/recent-work/care-bn-stabilizing-snn-rl/representative-results.png" width="100%" %}
</div>
