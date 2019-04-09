# Welcome to NLP-2019-huanhuan-homework-2

## 内容涵盖：
- THUCNews中文数据集分析探索
- IMDB英文数据集分析探索
- 学习召回率、准确率、F1值、ROC曲线、AUC、PR曲线等这些基本概念

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


### 3. 分类模型和回归模型评估指标    

- **分类模型评估**   

| 指标           | 描述           | Scikit-learn函数  |  
|:-------------: |:-------------:| :-----|   
| Precision | 精准度 | from sklearn.metrics import precision_score | 
| Recall | 	召回率  | from sklearn.metrics import recall_score |  
| F1 | F1值    |    from sklearn.metrics import f1_score |  
| Confusion Matrix | 	混淆矩阵 | from sklearn.metrics import confusion_matrix | 
| ROC | 	ROC曲线 |  from sklearn.metrics import roc |  
| AUC | ROC曲线下的面积 |  from sklearn.metrics import auc |   

- **回归模型评估**   

|               指标            |        描述           | Scikit-learn函数  |  
|:----------------------------: |:--------------------:| :-----| 
| Mean Square Error (MSE, RMSE) |     平均方差          | from sklearn.metrics import mean_squared_error | 
| Absolute Error (MAE, RAE)     |   	绝对误差          | 	from sklearn.metrics import mean_absolute_error, median_absolute_error|  
| R-Squared                     |     R平方值           |    from sklearn.metrics import r2_score |   

**3.0 知识补充--混淆矩阵**   
- TP(True Positive): 真实为1，预测也为1（将正类预测为正类数）
- FN(False Negative): 真实为1，预测为0（将正类预测为负类数）
- FP(False Positive): 真实为0，预测为1（将负类预测为正类数误报）
- TN(True Negative): 真实为0，预测也为0（将负类预测为负类数）  
将这四个指标一起呈现在表格中，就能得到如下这样一个矩阵，我们称它为混淆矩阵（Confusion Matrix）：  
![hunxiaojuzheng-1](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/hunxiaojuzheng-1.jpg?raw=true) 

- 混淆矩阵的指标  
  预测性分类模型，肯定是希望越准越好。那么，对应到混淆矩阵中，那肯定是希望TP与TN的数量大，而FP与FN的数量小。所以当我们得到了模型的混淆矩阵后，就需要去看有多少观测值在第二、四象限对应的位置，这里的数值越多越好；反之，在第一、三四象限对应位置出现的观测值肯定是越少越好。  
  
- 混淆矩阵的API  
![hunxiaojuzhengAPI-2](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/hunxiaojuzhengAPI-2.jpg?raw=true)

**3.1 准确率(accuracy)**  
    准确率是我们最常见的评价指标，而且很容易理解，就是被分对的样本数除以所有的样本数，通常来说，正确率越高，分类器越好。
- 公式  
![zhunquelvgongshi-3](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/zhunqulvgongshi-3.jpg?raw=true)  
- 准确率的API    
![zhunquelvAPI-4](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/zhunquelvAPI-4.jpg?raw=true)   

**3.2 精确率、精度(Precision)**  
  表示被分为正例的示例中实际为正例的比例（即模型预测是正例的所有结果中，模型预测对的比例）。
- 公式  
![jingquelvgongshi-5](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/jingquelvgongshi-5.jpg?raw=true)  
- 准确率的API    
![jingquelvAPI-6](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/jingqueluAPI-6.jpg?raw=true)    

**3.3 召回率(Recall)**  
  召回率是覆盖面的度量，度量有多个正例被分为正例（即在真实值是正例的所有结果中，模型预测对的比例）
- 公式  
![zhaohuilvgongshi-7](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/zhohuilvgongshi-7.jpg?raw=true)  
- 召回率的API    
![zhaohuilvAPI-8](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/zhaohuilvAPI-8.jpg?raw=true)   

**3.4 F1值(F1 score)**  
 用来衡量二分类模型精确度的一种指标。它同时兼顾了分类模型的准确率和召回率。F1分数可以看作是模型准确率和召回率的一种加权平均，取值范围从0到1的，1代表模型的输出最好，0代表模型的输出结果最差。  
![F1-9](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/F1-9.jpg?raw=true)    
其中，P代表Precision，R代表Recall。  
- F1值的API     
![F1API-10](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/F1API-10.jpg?raw=true)  

**3.5 ROC(Receiver Operating Characteristic)曲线**
- ROC曲线：接收者操作特征曲线(receiver operating characteristic curve)，是反映敏感性和特异性连续变量的综合指标，roc曲线上每个点反映着对同一信号刺激的感受性。  
- ROC曲线的横轴是假正率（FP_rate）、是TPR,纵轴是真正率（TP_rate），ROC曲线的面积就是AUC（Area Under the Curve）。  

- 先来了解下，对于计算ROC最重要的三个概念就是TPR, FPR, 截断点（thresholds）。
（1）**TPR：真实的正例1中，被预测为正例的比例**  
TPR即True Positive Rate，TPR = TP/(TP+FN)。(其中，样本中的真实正例类别总数即TP+FN)    
（2）**FPR：真实的反例0中，被预测为正例的比例**  
FPR即False Positive Rate，FPR=FP/(TN+FP)。(其中，样本中的真实反例类别总数为FP+TN)    
（3）截断点thresholds  
   机器学习算法对test样本进行预测后，可以输出各test样本对某个类别的相似度概率。比如t1是P类别的概率为0.3，一般我们认为概率低于0.5，t1就属于类别N。这里的0.5，就是”截断点”。  
- **ROC图像**  
![ROC](https://github.com/HuanwenW/MyPostImag/blob/master/190408-NLP-gainian/ROC.jpg?raw=true)  

**最理想的分类器，就是对样本分类完全正确，即FP=0，FN=0。所以理想分类器TPR=1，FPR=0**      
(1) 曲线与FP_rate轴围成的面积（记作AUC）越大，说明性能越好，即图上L2曲线对应的性能优于曲线L1对应的性能。即：**ROC曲线越靠近A点（左上方）性能越好，代表模型越好，即ACU接近1** ；曲线越靠近B点（右下方）曲线性能越差。  
(2) A点是最完美的performance点，B处是性能最差点。  
(3) 位于C-D线上的点说明算法性能和random猜测是一样的–如C、D、E点。位于C-D之上（即曲线位于白色的三角形内）说明算法性能优于随机猜测–如G点，位于C-D之下（即曲线位于灰色的三角形内）说明算法性能差于随机猜测–如F点。  
(4) 虽然ROC曲线相比较于Precision和Recall等衡量指标更加合理，但是其在高不平衡数据条件下的的表现仍然过于理想，不能够很好的展示实际情况。    
- **AUC**  
AUC (Area Under Curve) 被定义为ROC曲线下的面积，显然这个面积的数值不会大于1。又由于ROC曲线一般都处于y=x这条直线的上方，所以AUC的取值范围一般在0.5和1之间。使用AUC值作为评价标准是因为很多时候ROC曲线并不能清晰的说明哪个分类器的效果更好，而作为一个数值，对应AUC更大的分类器效果更好。简单说：AUC值越大的分类器，正确率越高。  

**从AUC判断分类器（预测模型）优劣的标准：**
  AUC = 1，是完美分类器，采用这个预测模型时，存在至少一个阈值能得出完美预测。绝大多数预测的场合，不存在完美分类器。
  0.5 < AUC < 1，优于随机猜测。这个分类器（模型）妥善设定阈值的话，能有预测价值。
  AUC = 0.5，跟随机猜测一样（例：丢铜板），模型没有预测价值。
  AUC < 0.5，比随机猜测还差；但只要总是反预测而行，就优于随机猜测。  
  
**3.6 PR（Precision-Recall）曲线**   

PR曲线指的是Precision Recall曲线，中文为查准率（精度）-查全率（召回）曲线。PR曲线在分类、检索等领域有着广泛的使用，来表现分类/检索的性能。  
如果是分类器的话，通过调整分类阈值，可以得到不同的P-R值，从而可以得到一条曲线（纵坐标为P，横坐标为R）。通常随着分类阈值从大到小变化（大于阈值认为P），查准率(精度)减小，查全率（召回率）增加。比较两个分类器好坏时，显然是查得又准又全的比较好，也就是的PR曲线越往坐标（1，1）的位置靠近越好。

## 参考博客
1. [TensorFlow官方教程：影评文本分类|TensorFlow ](https://tensorflow.google.cn/tutorials/keras/basic_text_classification)  
2. [科赛 - Kesci.com](https://www.kesci.com/home/project/5b6c05409889570010ccce90)  
3. [博客中的数据集部分和预处理部分：CNN字符级中文文本分类-基于TensorFlow实现](https://blog.csdn.net/u011439796/article/details/77692621)  
4. [text-classification-cnn-rnn/cnews_loader.py at mas...](https://github.com/gaussic/text-classification-cnn-rnn/blob/master/data/cnews_loader.py)  
5. [机器学习之类别不平衡问题 (2) —— ROC和PR曲线_慕课手记](https://www.imooc.com/article/48072)
6. [ROC与AUC的定义与使用详解](https://blog.csdn.net/shenxiaoming77/article/details/72627882)
7. [混淆矩阵、准确率、精确率、召回率、F值、ROC曲线、AUC、PR曲线-Sklearn.metrics评估方法](https://www.jianshu.com/p/5df19746daf9)
8. [混淆矩阵的定义](https://blog.csdn.net/Orange_Spotty_Cat/article/details/80520839)
8. [机器学习：准确率(Precision)、召回率(Recall)、F值(F-Measure)、ROC曲线、PR曲线](https://blog.csdn.net/quiet_girl/article/details/70830796)
