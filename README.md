# 创建客户细分

------
## 项目背景
近日，一家批发经销商尝试着针对一些客户改变其发货方式，从原来的每周五次每次早上发货，改为了更为便宜的每周三次每次晚上发货。起初，发货方式的改变并没有带来任何显著的负面结果，于是该批发商将这一更为便宜的变动推广到了所有客户。几乎同一时刻，该批发商开始收到客户对发货服务变动的投诉，也有的客户开始取消提货。该批发商受到的损失比节省下来的钱还要多。

## 客户目标与要求
该批发经销商希望确定他们的客户特征和信息，以帮助他们在未来做出更加明智的商业决策。

## 解决方案及结果
利用非监督学习技术，看看客户之间存在哪些相似之处，并以最佳的方式将客户细分为不同类别。
### 使用的语言和库
> * Python
> * Numpy
> * pandas
> * matplotlib
> * Sklearn


### 分析样本数据

> * 样本总数: 440
> * 特征数: 6
观察统计数据（mean, std, min, 25%, 50%, 75%, max）
观察几个样本的实际数据情况

### 处理原始数据并构建合适的模型
观察发现数据存在很大的偏度，通过对数函数进行特征缩放。随后剔除极端的样本点。然后进行PCA（主成分分析）并进行降维。
构建 **K Means**聚类模型，分别聚为2，3，4，5类。

### 结果
利用Sklearn库中的silhouette_score工具选择最佳的聚类数为 2 类。