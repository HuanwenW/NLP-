# Welcome to NLP-2019-huanhuan-homework-2

## 内容涵盖：
- THUCNews中文数据集分析探索
- IMDB英文数据集分析探索
- 学习召回率、准确率、ROC曲线、AUC、PR曲线这些基本概念

### 1. THUCNews中文数据集  

**1.1 数据说明**  

  THUCNews是根据新浪新闻RSS订阅频道2005~2011年间的历史数据筛选过滤生成，包含74万篇新闻文档（2.19 GB），均为UTF-8纯文本格式。我们在原始新浪新闻分类体系的基础上，重新整合划分出14个候选分类类别：财经、彩票、房产、股票、家居、教育、科技、社会、时尚、时政、体育、星座、游戏、娱乐。  

**1.2 数据下载**  

- 完整版：[数据由清华大学免费提供，需提交一些个人基本信息（如：姓名、邮箱等）](http://thuctc.thunlp.org/message)
- 部分版：[数据由Datawhale学习小组提供](https://pan.baidu.com/s/1hugrfRu) 密码：qfud  

**1.3 数据分析**  

### 2. IMDB英文数据集  

**2.1 数据说明**  

 IMDB是短文本情感分析二分类数据集，每条样本是一个txt文件。包括训练集、测试集、没有标签的数据。其中，训练集：25000条，正负各12500条；测试集：25000条，正负各12500条  

**2.2 数据下载**  

- 数据由[斯坦福大学提供](http://ai.stanford.edu/~amaas/data/sentiment/)  

**2.3 数据分析**  

| 指标           | 描述           | Scikit-learn函数  |  
|:-------------: |:-------------:| :-----:|  
| Precision      | right-aligned | $1600 |  
| Recall      | centered      |   $12 |  
| F1 | are neat      |    $1 |  
| Confusion Matrix| are neat      |    $1 | 
| ROC| are neat      |    $1 | 
| AUC| are neat      |    $1 | 
### 3. 分类模型和回归模型评估指标  



## 参考博客
1. [TensorFlow官方教程：影评文本分类|TensorFlow ](https://tensorflow.google.cn/tutorials/keras/basic_text_classification)  
2. [科赛 - Kesci.com](https://www.kesci.com/home/project/5b6c05409889570010ccce90)  
3. [博客中的数据集部分和预处理部分：CNN字符级中文文本分类-基于TensorFlow实现](https://blog.csdn.net/u011439796/article/details/77692621)  
4. [text-classification-cnn-rnn/cnews_loader.py at mas...](https://github.com/gaussic/text-classification-cnn-rnn/blob/master/data/cnews_loader.py)  
5. [机器学习之类别不平衡问题 (2) —— ROC和PR曲线_慕课手记](https://www.imooc.com/article/48072)
