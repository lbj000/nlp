1. pLSA、共轭先验分布；LDA主题模型原理    
    pLSA  
    我们可以看看日常生活中人是如何构思文章的。如果我们要写一篇文章，往往是先确定要写哪几个主题。  
    譬如构思一篇自然语言处理相关的文章，可能 40\% 会谈论语言学、30\% 谈论概率统计、20\% 谈论计算机、  
    还有10\%谈论其它的主题：说到语言学，我们容易想到的词包括：语法、句子、乔姆斯基、句法分析、主语…；  
    谈论概率统计，我们容易想到以下一些词: 概率、模型、均值、方差、证明、独立、马尔科夫链、…；  
    谈论计算机，我们容易想到的词是： 内存、硬盘、编程、二进制、对象、算法、复杂度…；  
    我们之所以能马上想到这些词，是因为这些词在对应的主题下出现的概率很高。我们可以很自然的看到，  
    一篇文章通常是由多个主题构成的、而每一个主题大概可以用与该主题相关的频率最高的一些词来描述。  
    ![img](https://github.com/lbj000/nlp/blob/master/game-plsa.jpg)  
    ![img](https://github.com/lbj000/nlp/blob/master/plsa-doc-topic-word.jpg)  
    共轭先验分布  
    在贝叶斯统计中，如果后验分布与先验分布属于同类，则先验分布与后验分布被称为共轭分布，而先验分布被称为似然函数的共轭先验。  
    LDA主题模型原理  
    对于上述的 PLSA 模型，贝叶斯学派显然是有意见的，doc-topic 骰子θ→m和 topic-word 骰子φ→k都是模型中的参数，  
    参数都是随机变量，怎么能没有先验分布呢？于是，类似于对 Unigram Model 的贝叶斯改造，我们也可以如下在两个  
    骰子参数前加上先验分布从而把 PLSA 对应的游戏过程改造为一个贝叶斯的游戏过程。由于φ→k和θ→m都对应到多项  
    分布，所以先验分布的一个好的选择就是Drichlet分布，于是我们就得到了 LDA(Latent Dirichlet Allocation)模型。  
    
    ![img](https://github.com/lbj000/nlp/blob/master/game-lda-1.jpg)  
    ![img](https://github.com/lbj000/nlp/blob/master/lda-dice.jpg)  
2. LDA应用场景   
    这个简单的LDA模型提供了一个强大的工具来发现和探索大量文档集合中的隐藏的主题结构。但是，  
    在众多使用LDA建模的好处是，它可以嵌入到更加复杂的场景之中，从而达到更加复杂的目标。  
    从LDA诞生起，它就被不断地扩展和适配。
3. LDA优缺点   
4. LDA 参数学习   
5. 使用LDA生成主题特征，在之前特征的基础上加入主题特征进行文本分类  
    ![img](https://github.com/lbj000/nlp/blob/master/向量化.png)  
    ![img](https://github.com/lbj000/nlp/blob/master/topic_word.png)  
    ![img](https://github.com/lbj000/nlp/blob/master/Document-Topic.png)  
