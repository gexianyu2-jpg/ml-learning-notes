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
4.evaluation
N-fold Cross Validation:评估模型的泛化能力，减少单次划分带来的随机性.


部分名词解释：regression(回归):预测连续值  classification(分类)：预测离散类别  structured learning(结构化学习)：预测具有内部结构的输出  model（模型）:具有未知参数的函数  Deep Learning（深度学习） = 多层非线性函数的嵌套，用层级结构表达复杂模式
## 2. 从Foundation model for cancer imaging biomarkers学习影像基础模型与自监督预训练的系统范式与评估框架


---

## 3.2.从AI-based large-scale screening of gastric cancer from noncontrast CT imaging学会从0完成模型的建模到评估


---

## 4.从LLaVA-Med: Training a Large Language and Vision Assistant for Biomedicine in One Day和Towards a holistic framework for multimodal LLM in 3D brain CT radiology report generation学会根据从私有数据出发，构建一个可以用于大模型训练的数据集



---

## 5. 从A generalist vision–language foundation model for diverse biomedical tasks学会通用医学 VLM 的开源轻量方案与跨任务评测



---

## 6. Thoughts
