# Main Job
- Read ANN for Neuroscience Primer

# What Have been Learnt
- Reviewed the Machine Learning training process and algorithms. SGD. 
- Supervised learning: task with a correct answer. 
- Reinforcement learning: at time step $t$, agent receiving observation $o_t$, under the situation $s_t$, and producing an action $a_t$, receiving a reward $r_t$. The overall target is to maximize the cumulative reward $R = \sum_t r_t$ at the end of each task.
	- Without NN, Reinforcement learning still played well on cognitive study. By modeling and observing how the agent's behavior adapts over time, **value-based** behavior is studied.
	- **Sure-bet option** that guarantees a small reward is preferable for subjects (agents) with **less confidence** on themselves about making a perceptual judgement. Therefore, the output of RL is unsure, since it depends on the subjects' confidence level at their perceptual decisions.
- Unsupervised learning: no targets
	- TO BE LEARNT: PCA, and how PCA make correspondence with finding the first component in a simple neural network.
# Questions
- Q: Supervised learning target outputs are **behavioral**, what dose **"behavioral"** mean? A reference[^2] is followed
	- A(probably): perceptual decision-making task. See A, say A; see B, say B. So there is absolutely a correct answer, whether it's A or B.
- Q: What is **value-based** behavior in RL?
	- A: It is a decision making strategy based on some value. Meanwhile, another strategy is featuring with **memory**, or other non-valued concepts.

# Interesting Things to be Reminded
- MLP with enough neurons can approximate arbitrary functions:[^1]


[^1]:Hornik, K., Stinchcombe, M., and White, H. (1989). Multilayer feedforward net- works are universal approximators. Neural Netw. 2, 359–366. [links](http://refhub.elsevier.com/S0896-6273(20)30705-4/sref69)
[^2]: McIntosh, L.T., Maheswaranathan, N., Nayebi, A., Ganguli, S., and Baccus, S.A. (2016). Deep learning models of the retinal response to natural scenes. Adv. Neural Inf. Process. Syst. 29, 1369–1377. [links](http://refhub.elsevier.com/S0896-6273(20)30705-4/sref118)