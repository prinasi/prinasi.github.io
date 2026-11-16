---
title: "3D Gaussian Splatting 基础笔记"
date: 2026-11-16T22:45:00+08:00
draft: false
tags: ["科研", "3DGS", "Computer Vision"]
categories: ["科研"]
description: "3D 高斯泼溅 (3DGS) 的核心公式与数学表述。"
math: true
---

## 3D 高斯表示

3D 高斯在空间中的几何分布由协方差矩阵 $\Sigma$ 和中心均值 $\mu$ 决定：

$$G(x) = \exp\left(-\frac{1}{2} (x - \mu)^T \Sigma^{-1} (x - \mu)\right)$$

为了保证协方差矩阵 $\Sigma$ 在优化过程中始终保持半正定性，通常将其分解为四元数对应的旋转矩阵 $R$ 和缩放对角矩阵 $S$：

$$\Sigma = R S S^T R^T$$

通过投影到相机平面后，得到 2D 协方差矩阵 $\Sigma'$：

$$\Sigma' = J W \Sigma W^T J^T$$

其中 $J$ 为透视投影的仿射逼近雅可比矩阵，$W$ 为观察变换矩阵。
