# ***基于人工智能AI青藏高原径流预测***


## ***AI第3极——第三组 ***
## ***团队宣言：***
- 全力以赴 我们最酷
## ***成员介绍***
### **导师：**
- **彭定志教授**
- **罗群老师**
- **龚雨薇老师**
- **樊正龙老师**
### **学员:**
- **常琛**   高二  昌平区第二中学          情绪智慧掌控担当
- **白博远** 高二  昌平区实验学校      
- **侯博文** 高二  北师大二附未来科学城    好成员担当
- **邬明廷** 高一  昌平区第二中学       python技术担当
- **赵弘毅** 初三  昌平区实验学校
- **袁绍轩** 初二  首师大附育新学校      摄像担当


## ***目录***
1. 研究背景
2. 研究方法
3. PBL笔记
4. 数据处理与模型构建
5. 美好的瞬间
6. 收获与感受

## ***一、研究背景***

### *人工智能的概念与其在水文方面的应用*
  随着机器学习解决了深层网络梯度消失的问题后，人工智能得到了跨越式发展，促使社会各方面发生巨大变革。人工智能技术包括神经网络算法模型、机器学习算法模型，因其处理非线性和不确定性的强大能力，在水文预报领域取得了丰硕的研究成果。随着人工智能工作领域的不断扩展，传统水文业务也需要适应新的数据模式的冲击，构建人工智能模型，从数据的角度进行业务分析，多维度、多方法地保证水文业务的精确性与高效性，能够有效地为系统水情预报测报业务提供技术支持，为水库的多目标规划调度提供科学依据。本案例基于人工智能核心神经网络算法构建青藏地区河流径流预测模型。改编自《青藏高原东南部径流特征的空间规律及控制因子研究》

### *青藏高原的河流径流特点*

青藏高原作为“亚洲水塔”，是众多大江大河的发源地，其河流径流具有显著的特点：
- 水量丰富：青藏高原的河流径流主要来源于冰川融水和降水，这些河流为下游地区提供了重要的水资源。
- 季节性明显：由于青藏高原的气候特点，河流径流表现出明显的季节性变化。夏季降水增多，冰川融水增加，河流径流量增大；而冬季则相反，河流径流量减小。
- 内流外流并存：青藏高原的河流分为内流河和外流河。内流河主要注入高原内部的湖泊或消失于荒漠之中；外流河则注入太平洋、印度洋等大洋。
- 受气候变化影响显著：青藏高原的河流径流受气候变化的影响显著。随着全球气候变暖，冰川融化加速，河流径流量可能发生变化。同时，降水模式的改变也可能对河流径流产生影响。


### *青藏高原径流预测意义与价值*
青藏高原幅员辽阔、地势挺拔，发源了长江等亚 洲东部及南部主要大河，是我国东部地区的重要水源地。青藏高原受多个环流系统共同控制，包括太平洋季风、印度洋季风和西风南支等，因此该地区水文过程对区域气候变化敏感。受气候变化影响，青藏高原气温呈上升趋势，降水量变异性增大，掌握气候变化条件下该区域径流特征，将对我国东部地区水资源管理与保护具有重要实际意义。摘自《青藏高原东南部径流特征的空间规律及控制因子研究》

### *河流水文学与水科学*
河流水文学是陆地水文学的分支学科，是研究河流水文现象、过程及其基本规律，为防治灾害和河流开发提供河流水情和河川径流资源等基本数据，主要依靠沿河布设水文站网及通过河流水文考察来获得水文信息。
水科学（aquatic science）是一门研究水的物理、化学、生物等特征，分布、运动、循环等规律，开发、利用、规划、管理与保护等方法的知识体系。


### *将AI应用于河流径流预测——长短期记忆人工神经网络*
长短期记忆人工神经网络（long short-term memory，LSTM）与标准的RNN模型结构基本相同，但拥有更加细化的内部处理单元，能真正有效地利用长距离的时序信息。LSTM包含特殊的细胞状态和门结构，可动态地控制时间序列信息的流动和保存，能够捕获水文变量间长时间的依赖性和水流路径连通性的变化，从而提高了径流的模拟精度。摘自《基于LSTM的青藏高原冻土区典型小流域径流模拟及预测》


## ***二、研究方法***
基于长短期记忆网络的径流预测模型 
长短期记忆网络（LSTM）是一种特殊的循环神经网络，是一种循环神经网络的变体，经过改进以解决长序列数据处理中的梯度消失和梯度爆炸问题。
梯度是神经网络训练中的重要参数，在反向传播过程中，用于更新神经网络权重。由于神经网络中的层数增加，每层之间的梯度会以乘法的形式进行叠加，梯度值很小则会在接下来的反向传播中逐渐消失或者梯度值过大则会出现梯度爆炸的情况。LSTM 的作用是解决梯度消失和梯度爆炸问题，使得LSTM能够处理持续时间较长的序列数据。 
- LSTM 主要结构包括输入门、遗忘门、记忆单元和输出门，如图1所示。

![图1](007.png)
- 输入门：控制着有多少信息可以被写入到记忆单元中，也就是决定这一次的输入应该如何处理。 
- 遗忘门：遗忘门控制着前一时刻的记忆单元中的多少信息需要被丢弃，同样受当前的输入以及前一时刻的输出的影响。 
- 记忆单元：记忆单元存储着序列中所有时刻的重要信息，数据流通过输入门或遗忘门得以进入或被遗忘，在不断被更新和改变。 
- 输出门：决定了什么信息从这个时刻的记忆单元中输出，通过当前的单元状态得到输出的各个成分，进一步计算出本时刻的输出。



## ***三、PBL笔记***




## ***四、数据处理与模型构建***

## ***五、美好的瞬间***
![图1](008.jpg)
![图1](010.jpg)
![图1](009.jpg)
![图1](011.jpg)

## ***六、收获与感受***

- *常琛* 我经由浓荫满地的银杏树，庄严肃穆的教学楼；我穿过岁月有痕的校史馆，国家重点的实验室；我了解水文学、AI技术、python编程的相关知识；我掌握用AI构建模型，AI技术对青藏地区的河流径流预测；我探索水科学的无穷魅力与奇妙。在这里，我与老师交流沟通，与同学团结协作，与水科学亲密接触，收获颇丰！
  
- *邬明廷* 身处在百年师大的校园，我感到被历史的底蕴包围，心情激动。这次为时5天的活动让不仅我收获了友谊，更让我感受到了ai科技的效率。我认为学习如何与ai打交道很有意义，这可以训练我们的逻辑思维能力和解决以目标为导向的问题，真正达到培养科学思维的目的。最后，我想感谢三位导师和和同学们，感谢我们在BNU相见。

- *白博远* 很充实很忙碌，在繁重的任务重也有很多快乐......






