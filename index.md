---
title: 'MoCapAct: A Multi-Task Dataset for Simulated Humanoid Control' layout: default
---

<style>thead { display: none; }</style>

## Abstract

> Control of simulated humanoid characters is a challenging benchmark for sequential decision-making methods, as it assesses a policy's ability to drive an inherently unstable, discontinuous, and high-dimensional physical system. One widely studied approach is to utilize motion capture (MoCap) data to teach the humanoid agent low-level skills (e.g., standing, walking, and running) that can be used to generate high-level behaviors. However, even with MoCap data, controlling simulated humanoids remains very hard, as MoCap data offers only kinematic information. Finding physical control inputs to realize the demonstrated motions requires computationally intensive methods like reinforcement learning. Thus, despite the publicly available MoCap data, its utility has been limited to institutions with large-scale compute. In this work, we dramatically lower the barrier for productive research on this topic by training and releasing high-quality agents that can track over three hours of MoCap data for a simulated humanoid in the dm_control physics-based environment. We release <em>MoCapAct</em>, a dataset of these expert agents and their rollouts containing proprioceptive observations and actions. We demonstrate the utility of MoCapAct by using it to train a <em>single</em> hierarchical policy capable of tracking the <em>entire</em> MoCap dataset within dm_control and show the learned low-level component can be re-used to efficiently learn high-level other tasks. Finally, we use MoCapAct to train an autoregressive GPT model and show that it can perform natural motion completion given a motion prompt.

## MoCapAct: Dataset

The MoCapAct Dataset consists of expert policies that are trained to track individual clips. A dataset of noise-augmented rollouts (containing observations and actions) is then collected from each expert. These rollouts can subsequently be used to train a multi-clip or GPT policy.

<img src="assets/MoCapAct.jpg" alt="overview" width="50%">

## Download Instructions

Add bash scripts or other instructions to download the dataset.

## Distilled Experts

Videos of experts trained using this dataset.

<table>
<tr> 
<td>
    <figure> 
        <video width="640" height="480" src="assets/go_to_target_sparse.mp4" type="video/mp4" controls></video>         
        <figcaption>Go-to-Target Task.</figcaption>
    </figure>
</td>

<td>
<figure> <img src="assets/cmu_humanoid.png" alt="house_lumber_bot" data-alt="assets/cmu_humanoid.png" width="60%" /> </figure></td>
</tr>
</table>

# Authors

These are our authors