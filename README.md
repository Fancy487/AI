# ***基于人工智能AI青藏高原径流预测***
## ***研究背景***
### *青藏高原径流预测意义与价值*
青藏高原幅员辽阔、地势挺拔，发源了长江等亚 洲东部及南部主要大河，是我国东部地区的重要水源地。青藏高原受多个环流系统共同控制，包括太平洋季风、印度洋季风和西风南支等，因此该地区水文过程对区域气候变化敏感。受气候变化影响，青藏 高原气温呈上升趋势，降水量变异性增大，掌握气候变化条件下该区域径流特征，将对我国东部地区水资源管理与保护具有重要实际意义。《青藏高原东南部径流特征的空间规律及控制因子研究》

### *长短期记忆人工神经网络*
长短期记忆人工神经网络（long short-term memory，LSTM）与标准的RNN模型结构基本相同，但拥有更加细化的内部处理单元，能真正有效地利用长距离的时序信息。LSTM包含特殊的细胞状态和门结构，可动态地控制时间序列信息的流动和保存，能够捕获水文变量间长时间的依赖性和水流路径连通性的变化，从而提高了径流的模拟精度。将LSTM应用于受季节性降雪影响的岷江源头区，并与RNN、BP对比，结果表明LSTM实现了流域状态的长期存储和更新，径流模拟结果明显优于RNN、BP模型。LSTM相较于RNN能较好地模拟 融雪径流，LSTM特殊的结构能够有助于提高模拟精度. 摘自《基于LSTM的青藏高原冻土区典型小流域径流模拟及预测》



