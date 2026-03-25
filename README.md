# ML Learning Notes

## 1. Machine Learning Basics
（李宏毅）
机器学习旨在学习一个从输入到输出的函数。ML = Model + Loss + Optimization

eg:

1. Model

```text
y = b + c^T σ(b + W x)
```
- x: feature（输入变量）
- y: prediction
- W, b, c: parameters（参数）
- σ: activation，这里是sigmoid function
- 单一线性模型表达能力有限（高bias），引入非线性激活函数（如 sigmoid），通过多层或多单元组合，可以逼近任意连续函数。

2. Loss

L(y, ŷ)

衡量预测与真实值的差距

Epoch：完整遍历一次训练数据

Update：基于一个 batch 进行一次参数更新

关系：
1 epoch = (dataset size / batch size) 次 update

3. Optimization

调整参数，使 loss 最小

 Gradient Descent: 

 Critical Point(saddle point鞍点/local minima局部最小值)
```text
∇f(x) = 0 的点
```
Critical point 分类依赖于 Hessian：

- λ 全正 → local minimum
- λ 全负 → local maximum
- λ 有正有负 → saddle point

高维中：
- saddle point ≫ local minimum

Momentum

Core Idea
- 利用历史梯度累积，加速收敛

Update Rule
- v ← βv - η∇L  
- θ ← θ + v

Effects
- 加速收敛
- 减少震荡
- 平滑噪声

Insight
> Momentum = 梯度的指数加权平均

adaptive methods(自适应学习率)
- RMSProp

- v ← βv + (1-β)(∇L)^2
-  θ ← θ - η * ∇L / sqrt(v)
-  β ∈ (0, 1)，通常取 0.9 / 0.99 / 0.999
-  β：动量/指数平均系数（constant）

RMS（simple average）：
- 对所有历史梯度平方做平均
→ 权重相同
→ 无法适应动态变化

RMSProp（EMA）：
- 对梯度平方做指数加权平均
→ 新数据权重大
→ 旧数据逐渐遗忘
→ 更适合训练过程中的非平稳变化

- Adam

4.evaluation

N-fold Cross Validation:评估模型的泛化能力，减少单次划分带来的随机性.


部分名词解释：

- regression(回归):预测连续值
- classification(分类)：预测离散类别
- structured learning(结构化学习)：预测具有内部结构的输出
- model（模型）:具有未知参数的函数
- Deep Learning（深度学习） = 多层非线性函数的嵌套，用层级结构表达复杂模式

hyperparameter:batch size 同时影响：

1. 计算效率（time）
- 单次 update：
-   small batch → 更快（无并行）
-    large batch → 更慢

-有 GPU 并行：
-    small ≈ large（甚至 large 更高效）

-每个 epoch：
-    small → 慢
-    large → 快 

2. 梯度性质（gradient）
- small batch：只用部分数据 → 梯度是估计值 → 有随机误差
- large batch：接近全数据 → 梯度更接近真实梯度

3. 优化路径（optimization）
- small batch 的噪声：
- → 提供“随机扰动”
- → 帮助跳出 saddle point / sharp minima
- →better
- large batch：
- → 梯度太精确
- → 容易卡在局部结构
- →worse

4. 泛化能力（generalization）
- small batch → noisy gradient
- → 不容易陷入 sharp minima
- → 更容易找到 flat minima
- → 对参数扰动更robust
- → 泛化更好
## 2. 从Foundation model for cancer imaging biomarkers学习影像基础模型与自监督预训练的系统范式与评估框架


---

## 3.2.从AI-based large-scale screening of gastric cancer from noncontrast CT imaging学会从0完成模型的建模到评估


---

## 4.从LLaVA-Med: Training a Large Language and Vision Assistant for Biomedicine in One Day和Towards a holistic framework for multimodal LLM in 3D brain CT radiology report generation学会根据从私有数据出发，构建一个可以用于大模型训练的数据集



---

## 5. 从A generalist vision–language foundation model for diverse biomedical tasks学会通用医学 VLM 的开源轻量方案与跨任务评测



---

## 6. Thoughts
