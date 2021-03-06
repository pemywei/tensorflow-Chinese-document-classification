# Tensorflow Chinese Document Classification
## Preparation
### My Hardware
4-core CPU, 16G memory, 64G SSD, 1 Titan Z graphics card (12G display memory, two GPU)
### My OS
Ubuntu 16.04.1
### Data Set
[搜狗20061127新闻语料(包含分类)@百度盘](https://pan.baidu.com/s/1bnhXX6Z)<br> 
Includes 9 classes of news corpus such as finance, IT, health, sports, tourism, education, recruitment, culture and military.Each category has 1,990 texts.
### Requirements
* numpy >= 1.12.1<br>
* tensorflow 1.4.0<br>
* scikit-learn 0.19.1<br>
* jieba<br>
* zhon
## Why This Project?
[Hierarchical Attention Networks for Document Classification](http://www.aclweb.org/anthology/N16-1174) is a classic paper uses attention mechanism for document<br> classification.At present,open source code about Chinese document classification based on deep learning still less.So I<br> use the sogou news corpus and tensorflow to achieve a Chinese classifier.Fig1 shows the training results and finally this<br> model achieves 0.806780 accuracy(as shown in Fig2) in the test set.My [Chinese blog](http://blog.yeliangli.com/nlp/%E5%9F%BA%E4%BA%8E%E6%B7%B1%E5%BA%A6%E5%AD%A6%E4%B9%A0attention%E6%9C%BA%E5%88%B6%E7%9A%84%E4%B8%AD%E6%96%87%E6%96%87%E6%9C%AC%E5%88%86%E7%B1%BB%E4%BB%A3%E7%A0%81%E5%AE%9E%E7%8E%B0.html) gives a code analysis of this project <br>and welcome to look up.
## How to get started?
1. First you need to download the database and extract it to the code directory.<br>
2. Command "python3 preprocess.py" used to generate TFRecords format files for training and testing.<br>
3. Command "python3 train.py" achieve training.<br>
4. After the training is completed, you can use the command "python3 evaluate.py" to achieve the model evaluation in the
  test set.
## Figure
![](https://github.com/YeliangLi/tensorflow-Chinese-document-classification/raw/master/picture/trainingResults.png)<br>
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Fig1 training results<br><br>
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
![](https://github.com/YeliangLi/tensorflow-Chinese-document-classification/raw/master/picture/evaluationResult.png)<br>
&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Fig2 evaluation results
                                  
