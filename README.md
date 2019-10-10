## auto_modeling: 自动化建模脚本

输入规定格式数据集,可全自动化或半自动化建模

### 方法

建模流程主要通过以下几种方法完成:

1. 数据集划分
2. 特征筛选
3. 超参数优化
4. 可视化结果报表

### 用法

参考auto\_modeling\_usage\_自定义.ipynb和auto\_modeling\_usage\_全自动.ipynb了解如何使用

可直接点击下面的链接直接查看自动生成的HTML报表（需等待10S-30S）：
[result_report](http://htmlpreview.github.io/?https://github.com/lizhigu1996/auto_modeling_usage/blob/master/usage/result/result_report_complete.html)
 


### 依赖

* numpy = 1.16.2
* pandas = 0.24.2
* scikit-learn = 0.20.3
* scipy = 1.2.1
* matplotlib = 3.0.3
* seaborn = 0.9.0
* warnings
* time
* gc
* lightgbm = 2.2.3
* xgboost = 0.82
* sklearn_pandas = 1.8.0
* sklearn2pmml = 0.43.0
* hyperopt = 0.1.2 (可使用贝叶斯优化的tpe算法和随机搜索优化超参数,官方文档:[hyperopt](https://github.com/hyperopt/hyperopt))
* bayesian-optimization = 1.0.1 (可使用贝叶斯的高斯过程算法优化超参数,官方文档:[Bayesian Optimization](https://github.com/fmfn/BayesianOptimization))
* plotly = 3.7.1 (生成交互式可视化报表,官方文档:[plotly](https://plot.ly/python/))
* shap = 0.28.5 (解释机器学习模型,官方文档:[shap](https://github.com/slundberg/shap))
* codecs
* os
* sys
* webbrowser


### 结构

> ### auto_modeling
> * \_\_init\_\_.py
> * data\_split.py
>     > data\_split -- 数据集划分
> * feature\_select.py
>     > feature\_select -- 特征选择
> * para\_optimize.py
>     > para\_optimize -- 超参数优化
> * result\_report.py
>     > result\_report -- 可视化结果报表
> * other\_function.py
>     > get\_coltype\_datalist -- 处理数据集、区分变量类型
>     
>     > get\_mapper -- 封装变量处理方法
>     
>     > get\_learning\_curve -- 绘制学习曲线
>     
>     > get\_bset\_para\_model -- 选择模型并建立
>     
>     > get\_pp\_data\_trans -- 处理陪跑数据集
>     
>     > get\_group\_final -- 按照正态分布分组的方案
>
>     > get\_result\_table -- 各组/各等分情况
>     
>     > get\_group\_score -- 各组预测结果阈值
>     
>     > get\_model\_file -- 输出模型文件
>
>     > get\_index\_values -- 计算各指标值
> 
>     > get\_data\_trans -- 处理其他数据集
> 
>     > read\_model\_pkl -- 读取pkl文件
> 
>     > modifying\_pmml -- 修改pmml文件
> 
>     > get\_model\_explain -- 回溯模型解释器
> 
>     > get\_predict\_explain -- 获取单样本预测值解释
>
>     > get\_model\_predict -- 获取模型预测结果(pipeline、pkl文件、pmml文件)
> * full\_automatic.py
>     > full\_automatic\_simplet -- 简单模式全自动建模
>     
>     > full\_automatic\_complete -- 完整模式全自动建模
