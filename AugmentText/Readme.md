# AugmentText

# 概述
    - 文本数据增强的有效方法:
    - 一个是回译（翻译两次，例如中文到英文，然后英文再到中文），
    - 另外一个就是EDA（同义词替换、插入、交换和删除），插入和交换当时确实没有想到用


###github项目地址为###
    https://github.com/yongzhuo/nlp_xiaojiang/tree/master/AugmentText


# 回译（相对靠谱）
    - 1.在线翻译工具（中文->[英、法、德、俄、西班牙、葡萄牙、日、韩、荷兰、阿拉伯]等语言）
       - 谷歌翻译(google)，谷歌翻译不用说，应该是挺好的，语言支持最多，不过我暂时还不会翻墙注册账户
       - 百度翻译(baidu)，百度翻译不用说，国内支持翻译语言最多的了(28种互译)，而且最大方了，注册账户后每月有200万字符的流量，超出则49元人民币/百万字符
    - 2.离线翻译工具
       - 1.自己写，收集些语料，seq2seq,nmt,transformer
       - 2.小牛翻译，比较古老的版本了，win10或者linux都可以，不过只有训练好的中英互译
             地址:http://www.niutrans.com/index.html

# 同义词替换（还行）
    - 1.eda(其实就是同义词替换、插入、交换和删除)   
        - 中文实现的demo，github项目zhanlaoban/eda_nlp_for_Chinese，地址:https://github.com/zhanlaoban/eda_nlp_for_Chinese
    - 2.word2vec、词典同义词替换
        - 不同于1中使用synonyms工具查找同义词，可以使用gensim的词向量，找出某个词最相似的词作为同意词。
        - 还可以使用同义词典机械查找，词典可用fighting41love/funNLP，github地址:https://github.com/fighting41love/funNLP/tree/master/data/

# 句法、句子扩充、句子缩写（比较困难、）
    - 1.句子缩写，查找句子主谓宾等
        - 有个java的项目，调用斯坦福分词工具(不爱用)，查找主谓宾的
        - 地址为:（主谓宾提取器）https://github.com/hankcs/MainPartExtractor
    - 2.句子扩写  todo
    - 3.句法 todo

# HMM-marko（质量较差）
    - HMM生成句子原理: 根据语料构建状态转移矩阵，jieba等提取关键词开头，生成句子
        - 参考项目:https://github.com/takeToDreamLand/SentenceGenerate_byMarkov

# 深度学习方法 todo
    - seq2seq
    - bert
    - transformer
    - GAN


# 参考/感谢
* eda_chinese：[https://github.com/zhanlaoban/eda_nlp_for_Chinese](https://github.com/zhanlaoban/eda_nlp_for_Chinese)
* 主谓宾提取器：[https://github.com/hankcs/MainPartExtractor](https://github.com/hankcs/MainPartExtractor)
* HMM生成句子：[https://github.com/takeToDreamLand/SentenceGenerate_byMarkov](https://github.com/takeToDreamLand/SentenceGenerate_byMarkov)
* 同义词等：[https://github.com/fighting41love/funNLP/tree/master/data/](https://github.com/fighting41love/funNLP/tree/master/data/)
* 小牛翻译：[http://www.niutrans.com/index.html](http://www.niutrans.com/index.html)
