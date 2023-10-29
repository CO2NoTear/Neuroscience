本周进展：
1. 阅读了《Artificial Neural Networks for Neuroscientists: A Primer》，
	- 细致地复习了ANN的基本架构：learning problem, network architecture, training algorithm，了解了最基本的一种RNN架构：vanilla RNN以及LSTM的基本实现方式，激活函数的选择，以及RNN的训练算法BPTT。进一步地，粗浅地了解了连续时间下的RNN的数学模型和训练算法的改良。
	- 了解了一种通用的网络相似度计量方式RSA，通过比较两个网络对于不同任务的相异性矩阵，计算两个相异性矩阵的相关系数或者直接线性拟合，来评判两个网络的相似度。
2. 阅读了《Task representations in neural networks trained to perform many cognitive tasks》，
	- 对于cognitive tasks在RNN上的任务表达有了初步的认识：宏观上任务输入分为三个部分：规则、定点信号（文中称为fixation，个人觉得在任务表达的作用里像发令枪）、刺激模式，其中直接的单任务表达不需要特殊的规则输入，使用多个任务指导RNN进行任务复合时才需要对规则进行约束；定点信号在普通任务中具有发号施令的作用，即定点信号下降沿编码了输出信号的开始时刻，而RealTime系列任务中由于要求网络在刺激模式出现的即刻做出反应，所以定点信号为常值；刺激信号根据任务特性进行编码，例如文章中设计的“Go”系列任务需要网络给出前进方向，方向被编码到环状的输入输出位上。
	- 训练任务的策略也有区别：1. 训练过程中随机插入任务；2. 顺序训练20个任务。文章发现后者更接近生物的认知训练过程，并且在近期任务和利用近期任务的复合完成新任务的表现上更优秀。
	- 对网络的evaluation还没有完全认识，只知道作者使用了自己设计的Task Variance的评估方式，略微复杂具体内容需要之后再啃。
3. 简单阅读了《Catalyzing next-generation Artificial Intelligence through NeuroAI》，文中提到的Embodied Turing Test对于通用AI-agent给出了认知任务设计方向：尝试用AI解决现实世界中的生物能轻易实现的感知-驱动型任务，并且有针对性地设计、评估AI的表现。
4. 阅读了《Growing Brains: Co-emergence of Anatomical and Functional Modularity in Recurrent Neural Networks》，该文章是对[2.] 中提出的任务表达方式进行的实际应用，通过对RNN的active单元增加distance regularization项来约束其位置，并且允许RNN单元间进行位置互换，最终使得网络的参数图像呈现较好的clustering，在性能上优于不考虑位置约束的网络。作者将其成为Brain Inspired Modular Training (BIMT)算法，训练后形成的clusters成为functional modular。
5. 正在阅读《A Survey on Large Language Model based Autonomous Agents》，系统性地了解并认识LLM下的AI-agent如何构建、应用和评估。
6. 从Llama官网下载了Llama 2和 Code Llama 的模型数据，下一步计划在本地部署和调试模型。
本周计划：阅读AI-agent和LLM相关论文，寻找将RNN的任务表达应用到LLM的方法，或者寻找适合于LLM的任务表达。