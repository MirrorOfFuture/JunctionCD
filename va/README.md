# JunctionVA

For junction challenge

#  中文支持
##  配置option 1: config.yml配置1，在backup里有文件
使用tensorflow_embedding
需要安装jieba: pip install jieba
------------------------------------------
language: zh

pipeline:
- name: JiebaTokenizer
- name: CRFEntityExtractor
- name: CountVectorsFeaturizer
  OOV_token: oov
  token_pattern: '(?u)\b\w+\b'
- name: EmbeddingIntentClassifier
-----------------------------------------


##  Option 2 jieba分词，MITIE模型，sklearn意图识别分类
安装MITIE
    下载MITIE
    解压后执行python setup.py install
安装Rasa_NLU_Chi:
    下载Rasa_NLU_Chi
    解压后执行python setup.py install
MITIE模型文件以及放入data/total_word_feature_extractor_zh.dat

config.yml内容：
---------------------------------
language: zh
pipeline:
- name: MitieNLP
  model: data/total_word_feature_extractor_zh.dat
- name: JiebaTokenizer
- name: MitieEntityExtractor
- name: EntitySynonymMapper
- name: RegexFeaturizer
- name: MitieFeaturizer
- name: SklearnIntentClassifier
------------------------------------




## Rasa X使用：
1.安装：pip install rasa-x --extra-index-url https://pypi.rasa.com/simple
2.启动,在rasa 工程目录下,会一并启动rasa：
 python -m rasa x


##启动rasa：
rasa run --enable-api --cors '*'