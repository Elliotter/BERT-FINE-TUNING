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
		
# Bert的使用
##程序整体流程
   
   * Full_tokenizer:字典文件
   * 数据预处理
## Bert配置
* bert_config.json
      
        {
          "attention_probs_dropout_prob": 0.1,  #乘法attention时，softmax后dropout概率
  		  "directionality": "bidi",    
          "hidden_act": "gelu",   #隐藏层dropout概率
          "hidden_dropout_prob": 0.1, 
          "hidden_size": 768,  #隐藏单元数
          "initializer_range": 0.02,  #初始化范围
          "intermediate_size": 3072,  #升维维度
          "max_position_embeddings": 512,  #一个大于seq_length的参数，用于生成position_embedding
          "num_attention_heads": 12, #每个隐藏层中的attention head数
          "num_hidden_layers": 12,  #隐藏层数
          "pooler_fc_size": 768, 
          "pooler_num_attention_heads": 12, 
          "pooler_num_fc_layers": 3, 
          "pooler_size_per_head": 128, 
          "pooler_type": "first_token_transform", 
          "type_vocab_size": 2,  #segment_ids类别 [0,1]
          "vocab_size": 21128  #词典中词数
         }

## 数据预处理
read_data

tokenizer 生成 tokenizer.tokenize(word)
input_ids
input_mask
segment_ids
labels_id
		
  
       
 


