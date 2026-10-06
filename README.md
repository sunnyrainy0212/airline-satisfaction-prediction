# Airline Satisfaction Prediction

基于 Kaggle Playground Series S6E10 的航空公司乘客满意度预测项目。

## 项目简介
本项目基于 Kaggle Playground Series S6E10 竞赛数据，目标为预测航空公司乘客满意度。数据包含约 70 万条训练样本、30 万条测试样本，涵盖乘客年龄、性别、客户类型、舱位等级、飞行距离、延误时间及 14 项服务评分（如机上 WiFi、在线值机、座椅舒适度、餐饮等）。

使用 Python 完成数据清洗与特征工程：分类变量用众数填充并做 One-Hot 编码，数值变量用中位数填充，训练集与测试集编码对齐。建模采用随机森林分类器（200 棵树、最大深度 15、类别权重平衡），Kaggle 测试集 AUC 0.956。通过特征重要性分析发现，在线值机体验、舱位等级、机上 WiFi 服务是影响乘客满意度的最关键因素，而乘客人口统计特征影响相对较小。

## 数据
- 来源：Kaggle Playground Series S6E10
- 规模：训练集 70 万条 × 23 列，测试集 30 万条 × 22 列
- 目标变量：satisfaction（True/False）
- 评估指标：AUC

## 方法
- 数据清洗：分类变量众数填充 + One-Hot 编码；数值变量中位数填充
- 模型：随机森林（n_estimators=200, max_depth=15, class_weight="balanced"）
- 特征重要性：在线值机、舱位等级、机上 WiFi 为关键特征

## 结果
- Kaggle 测试集 AUC：0.956

## 文件
- `notebook2e43e5287d.ipynb`：完整流程
- `submission.csv`：提交文件
- `requirements.txt`：依赖库

## 链接
- Kaggle 竞赛：https://www.kaggle.com/competitions/playground-series-s6e10
- 我的 Kaggle 主页：https://www.kaggle.com/sunnyrainy0212
