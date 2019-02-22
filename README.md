# BERT-FINE-TUNING
## 准备
* 数据源的准备
    
	BERT采用监督式学习方式，训练样本需要进行标注	

        美 B-LOC
	    国 I-LOC
		的 O
		华 B-PER
		莱 B-PER
		士 B-PER
		， O
		我 O
		和 O
		他 O
		谈 O
		笑 O
		风 O
		生 O
		。 O

* 模型的下载

    1. [BERT 源码库](https://github.com/google-research/bert):TensorFlow code and pre-trained models for BERT
  
    2. [BERT-Base, Multilingual Cased](https://storage.googleapis.com/bert_models/2018_11_23/multi_cased_L-12_H-768_A-12.zip): 104 languages, 12-layer, 768-hidden, 12-heads, 110M parameters

	    [BERT-Base, Chinese](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip): Chinese Simplified and Traditional, 12-layer, 768-hidden, 12-heads, 110M parameters
			
    3. BERT支持多语言的版本，其推出的中文版本单独训练效果更好。
       
        	BERT-Base, Chinese文件夹：
            1. TensorFlow检查点（bert_model.ckpt）包含预先训练的权重（实际上是3个文件）。
            2. vocab.txt用于将WordPiece映射到word id的词汇文件（）。
            3. 配置文件（bert_config.json），指定模型的超参数。

* 文件夹

        bert--bert源代码库
	    checkpoint--bert模型	   
              
   	    data--训练数据
		
		
  
       
 


