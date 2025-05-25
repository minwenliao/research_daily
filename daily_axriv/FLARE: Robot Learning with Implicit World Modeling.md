
contribution:
1) 仅需对标准VLA模型进行极少的架构调整（增加少量标记）

2) 

method：
1) "In our main experiments, we apply this objective at layer 6 out of 8 total layers in the DiT architecture."

在DiT的中间层（8层中的第6层）插入附加的Future Tokens，这些tokens通过交叉注意力与当前状态交互，输出未来嵌入预测


2) "At its core, FLARE predicts a compact representation of the robot’s future observation from the hidden states of the action denoising network. FLARE operates in two key stages."