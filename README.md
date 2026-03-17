# ML Learning Notes

## Learning Goal（英文）
- Understand machine learning fundamentals
- Explore medical imaging applications

---

## 1. Machine Learning Basics（英文标题）

机器学习的核心可以理解为：
- 模型（Model）
- 损失函数（Loss）
- 优化（Optimization）

其目标是学习一个从输入到输出的映射函数。

---

## 2. Medical AI Pipeline（英文标题）

通过阅读相关论文，我总结医学AI的基本流程为：

1. 数据：
- CT影像（通常为3D）
- 数据分布不均衡

2. 任务：
- 分类（如癌症检测）
- 报告生成

3. 模型：
- CNN / Transformer
- 多模态模型（VLM）

4. 评价：
- 常用AUC指标

---

## 3. Paper Insights（英文标题）

### AI-based gastric cancer screening

这篇论文主要完成了：
- 基于CT影像进行癌症筛查
- 使用AUC作为主要评价指标

---

## 4. Thoughts（英文标题）

- 我发现AUC在医学任务中非常重要
- 医学影像问题本质上可以转化为机器学习问题
- 对多模态模型（图像+文本）比较感兴趣
