# UHPC-replication
Six ML algorithms were used to predict the mechanical properties of fiber-type UHPC . Reproduced core conclusions matched the original paper: CatBoost performed best, DNN the poorest. Yet, data-related issues caused acceptable discrepancies in SHAP feature importance ranking and GUI predicted values.

![](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

# 混凝土强度预测系统

基于机器学习的混凝土抗压/抗折强度预测工具，集成 CatBoost、XGBoost、LightGBM 等多种算法，提供 SHAP 可解释性分析和 PyQt5 交互界面。

# 📋 目录

- [环境准备](#环境准备)
- [安装依赖](#安装依赖)
- [运行方式](#运行方式)
- [功能说明](#功能说明)
- [模拟结果](#模拟结果)

##  🔧 环境准备

### 1. 虚拟机配置
- 下载并配置 VMware 虚拟环境

### 2. Python 环境
- 安装 Python **3.10.12**
- 建议创建虚拟环境：
  ```
  python3.10 -m venv venv
  source venv/bin/activate  # Linux/Mac
  # 或 venv\Scripts\activate  # Windows
  ```
  
##  📦 安装依赖
```bash
git clone https://github.com/Yves1415/UHPC-replication.git
cd UHPC-replication
pip3 install -r requirements.txt
# pip install numpy pandas matplotlib seaborn shap xgboost lightgbm catboost scikit-learn tensorflow pyqt5
```

 ### 验证安装
```
python -c "import shap; import catboost; import PyQt5; print('所有依赖安装成功')"
```

 ##  🚀 运行
```
python main2.py
```

 ##  📊 功能说明

| 模块	| 功能描述 |
|:---------:|:---------:|
|数据生成	| 模拟 863 组抗压 + 321 组抗折数据（基于论文 Table 1-2 统计特征）|
|模型训练	| 支持 CatBoost、XGBoost、LightGBM、GBM、ExtraTree、DNN |
|科研绘图	| SHAP 分析、雷达图、热力图、误差分析 |
|GUI 界面	| 交互式强度预测软件（基于 PyQt5）|


# 模拟结果

> 在这里添加图片的说明，并且说明使用什么数据训练的结果

![](asserts/figure1.png)

![](asserts/figure2.png)

![](asserts/figure3.png)

![](asserts/figure4.png)

![](asserts/figure5.png)

![](asserts/figure6.png)

> 在这里添加不同模型在数据集下的表现，例如：
> 需要你补齐数据

|模型         |R-Square           |RMSE   |
|-------------|-------------------|-------|
|XGBoost      |0.912              |0.102  |

<div align="right">
    <b><a href="#目录">↥ back to top</a></b>
</div>