---
layout: project
title: Neuromorphic Computing Paradigms Enhance Robustness through Spiking Neural Networks
section_title: Recent work
section_title_key: recent_work_title
section_link: /recent-work/
tags:
  - spiking neural networks
  - neuromorphic computing
---

*Jianhao Ding, Zhaofei Yu*, Jian K. Liu, Tiejun Huang. Neuromorphic Computing Paradigms Enhance Robustness through Spiking Neural Networks. Nature Communications. 2025, 16(1): 10175.*

<div data-lang-target="en" markdown="1">
[Read the paper](https://www.nature.com/articles/s41467-025-65197-x)

## Research Background and Problem

### Background

Deep learning models have achieved remarkable success across a wide range of tasks, including image recognition and decision-making systems, but their reliability is still threatened by adversarial attacks that introduce imperceptible perturbations to input data.

### Limitation of Existing Methods

Existing artificial neural networks (ANNs) exhibit limited robustness, as even minor input modifications can lead to significantly incorrect predictions, which raises serious concerns in safety-critical applications such as autonomous driving and human-machine interaction.

### Our Perspective

To address this limitation, we explore neuromorphic computing paradigms and leverage spiking neural networks (SNNs), which exploit temporal dynamics and brain-inspired processing mechanisms to enhance robustness against adversarial perturbations.

{% include figure.html image="/images/recent-work/neuromorphic-robustness/background-problem.png" width="100%" %}

## Contributions

- Demonstrate that temporal processing in SNNs is a key factor for improving robustness against adversarial attacks.
- Propose encoding strategies that prioritize task-critical information early in the temporal sequence.
- Introduce early-exit decoding methods to mitigate the impact of later perturbations.
- Design specialized training algorithms to better capture temporal dependencies and improve generalization.
- Propose a fusion encoding strategy to balance robustness and performance on natural data.

## Core Method

The proposed approach leverages the temporal characteristics of spiking neural networks to improve robustness. Specifically, input data are encoded into temporal spike sequences where important information is presented earlier, allowing the network to make reliable decisions before adversarial perturbations accumulate. In addition, early-exit decoding mechanisms reduce the influence of later noise, while temporal-aware training algorithms optimize spike timing dependencies. Furthermore, a fusion encoding strategy integrates multiple encoding schemes to enhance robustness under diverse attack scenarios.

SNNs exhibit capacities to protect themselves against adversarial attacks imperceptible to human vision by leveraging meticulously crafted encoding strategies and precise control over decoding duration.

{% include figure.html image="/images/recent-work/neuromorphic-robustness/core-method.png" width="100%" %}

## Representative Results

Experimental results on datasets such as CIFAR-10 show that the proposed SNN-based methods significantly outperform conventional ANNs in adversarial settings, achieving up to twice the robustness. At the same time, the model maintains high energy efficiency, making it suitable for real-world safety-critical and resource-constrained applications.

{% include figure.html image="/images/recent-work/neuromorphic-robustness/representative-results.png" caption="Accuracy comparison of SNNs with the fused encoding (enc.) versus non-fused ANN and SNN models, using the rate and TTFS decodings (dec.) on clean and four attacked datasets." width="100%" %}
</div>

<div data-lang-target="zh" hidden markdown="1">
[查看原文](https://www.nature.com/articles/s41467-025-65197-x)

## 研究背景与问题

### 背景

深度学习模型已经在图像识别、决策系统等广泛任务中取得了显著成功，但其可靠性仍然受到对抗攻击的威胁。这类攻击只需对输入数据加入人眼几乎不可察觉的微小扰动，就可能显著影响模型判断。

### 现有方法的局限

现有人工神经网络（ANN）在鲁棒性方面仍存在明显不足，即使是很小的输入改动也可能导致模型产生严重错误的预测。这一问题在自动驾驶、人机交互等安全关键场景中尤其令人担忧。

### 我们的思路

针对这一局限，我们从神经形态计算范式出发，引入脉冲神经网络（SNN）。该类模型利用时间动态和脑启发的信息处理机制，以提升系统在对抗扰动下的鲁棒性。

{% include figure.html image="/images/recent-work/neuromorphic-robustness/background-problem.png" width="100%" %}

## 创新点

- 证明了 SNN 中的时间处理机制是提升对抗攻击鲁棒性的关键因素。
- 提出将任务关键信息优先编码到时间序列前部的编码策略。
- 引入早退出解码方法，以减弱后期扰动带来的影响。
- 设计面向时间依赖关系的专用训练算法，以提升模型的泛化能力。
- 提出融合编码策略，在自然数据性能与鲁棒性之间取得更好平衡。

## 核心方法

该方法利用脉冲神经网络的时间特性来提升鲁棒性。具体而言，输入数据首先被编码为时间脉冲序列，使关键信息优先出现在前期时间步，从而让网络能够在对抗扰动累积之前作出更可靠的决策。同时，早退出解码机制可以削弱后期噪声的影响，面向时间建模的训练算法则进一步优化脉冲时序依赖关系。此外，融合编码策略整合了多种编码方式，以增强模型在不同攻击场景下的鲁棒性。

通过精心设计的编码策略以及对解码时长的精确控制，SNN 展现出抵御对人类视觉几乎不可察觉的对抗攻击的能力。

{% include figure.html image="/images/recent-work/neuromorphic-robustness/core-method.png" width="100%" %}

## 代表性结果

在 CIFAR-10 等数据集上的实验结果表明，所提出的基于 SNN 的方法在对抗攻击场景下显著优于传统 ANN，鲁棒性最高可提升至两倍。同时，该模型依然保持较高的能效，适用于真实世界中对安全性要求较高且资源受限的应用场景。

{% include figure.html image="/images/recent-work/neuromorphic-robustness/representative-results.png" caption="融合编码 SNN 与非融合的 ANN、SNN 模型在干净数据及四种攻击数据上的准确率对比，其中解码方式包括 rate 与 TTFS。" width="100%" %}
</div>
