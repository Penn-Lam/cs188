---
comments: true
dg-publish: true
tags:
  - notes
---

> [!PREREQUISITE]
>
> - [有限状态机](https://www.wikiwand.com/zh/articles/%E6%9C%89%E9%99%90%E7%8A%B6%E6%80%81%E6%9C%BA)

## note

### Agents

- 理性代理 (*rational agent*)
    - 一个具有目标或偏好的实体，试图执行一系列行动，以在这些目标下产生最佳/最优的预期结果。
- 反射代理 (*reflex agent*)
    - 一个不考虑其行为后果，而是仅根据当前世界状态选择行动的。
- PEAS（性能度量，环境，执行器，传感器）

<u>Agents的设计很大程度上取决于代理所作用的环境类型。</u>我们可以以下方式来描述环境类型：

- 在**partially observable environments（部分可观测环境）**, 代理无法获得关于状态的完整信息，因此代理必须对世界状态有一个内部估计。这与完全可观测环境形成对比，在完全可观测环境中，代理拥有关于其状态的完整信息。
- **Stochastic environments（随机环境）**在转换模型中存在不确定性，即在特定状态下采取行动可能有多个可能的结果，并且这些结果有不同的概率。这与**deterministic environments（确定环境）**形成对比，在确定环境中，在某个状态下采取行动只有一个确定会发生的结果。
- 在**multi-agent environments（多智能体环境）**，智能体与其他智能体一起在环境中行动。因此，智能体可能需要随机化其行为以避免被其他智能体“预测”。
- 如果环境在智能体对其采取行动时没有发生变化，那么这个环境被称为**静态环境**。这与智能体与它交互时发生变化的动态环境形成对比。
- 如果环境具有已知物理，那么过渡模型（即使随机）对智能体来说是已知的，它可以在规划路径时使用这一点。如果**物理未知**，智能体将需要采取有意的行动来学习未知动力学。

> [!HELP]
>
> 在这里，`know physics` 应该是指已经被人类探索出来的规律；而 `unknown physics` 则是指尚且没有得知的规律。

## link

- [cs188-sp24-note01](https://inst.eecs.berkeley.edu/~cs188/sp24/assets/notes/cs188-sp24-note01.pdf)
