# 课题背景

在某些真实的游戏AI应用场景中，游戏策划对AI的表现有“像人”(亦称为AI拟人化)的需求。

以吃鸡类游戏为例，在游戏初期或是一些特殊时段，常常会因为在线人数过少而无法凑满一局，从而导致玩家匹配时间过长或是失败。 为了优化玩家体验，游戏方会添加游戏AI减少玩家匹配时间。 但另一个方面，过多的(不像人的)游戏AI会降低玩家在游戏中获得的成就感，进而导致玩家流失。 故游戏方对凑人数时使用的AI具有更高的“像人”的要求。

目前，学术界对此类问题的解决方案通常是采用模仿学习。但模仿学习需要大量的玩家数据，而游戏的需要此类的AI正是用以应对真实玩家不足的情况，此处存在矛盾。

# 问题定义

- 针对少样本的情况下，如何使用模仿学习或是强化学习方法，得到一个策略层面的拟人化游戏AI

# 问题挑战

- 少样本: 训练这种游戏AI大部分情况下无法事先得到大量玩家数据
- 评价指标模糊: 策略层面的拟人化尚无较为公认的量化指标可供直接优化

# 环境支持

- 有真实玩家参与的游戏项目即可, 但最高环境的最优策略较难学习到(针对玩家和AI均是)

# 评价指标

- AI在游戏场景中的实际表现和reward指标

# 相关文献

暂缺, 待补充

# 联系我们

Email: guankai1@corp.netease.com