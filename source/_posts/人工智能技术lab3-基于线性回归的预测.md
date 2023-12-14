---
title: 人工智能技术lab3(基于线性回归的预测)
date: 2023-11-26 10:04:38
tags: 人工智能技术
categories: lab
---
## [source code and requirements](https://github.com/Lilinzta/ai)
## 0.实验环境
```sh
OS: Arch Linux(rolling)
LANG: Python 3.11.5
```
## 4.运行
```sh
python lab3/main.py
```
> lab3/main.py
```python
# 导入必要的库
import matplotlib.pyplot as plt
from sklearn.datasets import fetch_california_housing
from sklearn.model_selection import train_test_split
from sklearn.linear_model import linearregression
from sklearn.metrics import mean_squared_error


def main():

    # 加载加利福尼亚州房价数据集
    housing_22 = fetch_california_housing()
    x_22, y_22 = housing_22.data, housing_22.target

    # 划分数据集为训练集和测试集
    x_train_22, x_test_22, y_train_22, y_test_22 = train_test_split(
        x_22, y_22, test_size=0.2, random_state=42)

    # 初始化线性回归模型
    model_22 = linearregression()

    # 训练模型
    model_22.fit(x_train_22, y_train_22)

    # 在测试集上进行预测
    y_pred_22 = model_22.predict(x_test_22)

    # 评估模型性能
    mse_22 = mean_squared_error(y_test_22, y_pred_22)
    print(f'mean squared error on test set: {mse_22}')

    # 绘制真实值与预测值的对比图
    plt.scatter(y_test_22, y_pred_22)
    plt.xlabel('true values')
    plt.ylabel('predictions')
    plt.title('true values vs. predictions')
    plt.show()


if __name__ == "__main__":
    main()


```
## 5.实验结果
<img src=/res/post/ai/lab3-result.jpg width=100% />