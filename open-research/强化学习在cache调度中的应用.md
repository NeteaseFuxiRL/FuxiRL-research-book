# 课题背景

游戏场景呈现需要不断加载游戏场景内物体的模型，然后经过渲染展示在手机或者电脑屏幕上。加载渲染场景模型需要一定的时间开销，通过cache机制可以缩短模型的加载时间， 提高游戏体验（不会出现人物已经在移动， 周围的模型还没有加载渲染完成）。因此， 游戏资源加载的cahce调度算法十分重要， 当前游戏采用LRU算法管理cache，希望提出基于RL的算法，提供更合理的cache管理方式，减少资源交换次数，提高cache内实际加载资源的使用率。

# 问题定义

假设cache容量固定（通常为128），且每个资源占用cache容量一样大。
有一系列的资源请求（资源请求序列和玩家的游戏轨迹路线相关）和cache，对于每一个请求有cache hit和cache miss两种情况。当cache miss的时候，需要对该资源进行处理：1）是否放入cache中 2）如果cache满了，需要替换cache里面的那一个资源。
需要学习一个最优策略，当有请求时对cache进行操作，使得平均命中率最大。

### 目标

提高加载资源的命中率

# 问题挑战

- 游戏中资源数量过多，资源的表示方式影响算法的学习能力
- 资源的请求在每一帧末以批量的形式提出，单个请求处理速度较慢，如何在考虑资源请求的先后顺序的同时对请求进行批量处理

# 环境支持

可以提供倩女幽魂新手村任务过程中玩家的资源请求

# 评价指标

命中率

# 相关学术论文

1. 2019-RLCache: Automated Cache Management Using Reinforcement Learning
2. 2019-Adaptive Caching via Deep Reinforcement Learning
3. 2017-A Deep Reinforcement Learning-Based Framework for Content Caching

# 联系我们

有任何问题，请联系huyue1@corp.netease.com