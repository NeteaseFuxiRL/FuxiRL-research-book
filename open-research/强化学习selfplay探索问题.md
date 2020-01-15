# 项目背景

理论上，在强化学习的self play中，需要得到针对当前平均策略（average strategies）的最优反应（best response) ，才可能收敛到纳什均衡。早期通过树搜索遍历所有情况得到最优反应，开销太大；后来产生了Generalised weakened fictitious play，不再要求最优反应，只要能无限逼近最优反应即可，于是开始使用神经网络。但是深度神经网络不能保证收敛到全局最优，绝大部分情况是局部最优，因此不能收敛到纳什均衡。
在表现上，模型会被训练时没有见过的打法、套路打败，甚至变得很蠢。

在Alpha Star中，他们设计了一种league的self play训练方式，不同的group的有不同的职责，有些用于探索奇怪的打法。在挑选对手时也使用和历史胜率有关的权重。

# 目标

1. 无论面对何种敌人，agent都可以获胜，即取得环境最大可能reward；
2. 验证训练出的模型对于未知敌人的泛化性；

# 问题挑战

该问题主要存在以下几个挑战：

- 如何设计league
- 如何获得类似于监督学习的不同风格的base line模型

# 环境支持

可提供包含多种对手的对战模拟环境。

# 评价指标

- 胜率

# 相关学术论文

1. 2019- Grandmaster level in StarCraft II using multi-agent reinforcement learning

2. 2006- Generalised weakened fictitious play

3. 2015- Fictitious Self-Play in Extensive-Form Games

4. 1951- Iterative solution of games by fictitious play

# 联系我们

有任何问题，请联系leizihan@corp.netease.com