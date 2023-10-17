# Main Job
- Read Primer, and try follow the code on github to implement RNN.

# What Have been Learnt
- Reviewed Linear Algebra for PCA, SVD and relating things.
- Unsupervised learning is quite relevant to, and used to, model the development of sensory cortices, which are neural responses of visual areas, including early areas and higher areas.
- RNN: activity of neurons at time $t$, $r_t$ is driven by last time activity $r_{t-1}$ with corresponding weights $W_r$. Simultaneously, the input at $t$, $x_t$ will be added with corresponding weights $W_x$, too. Output of the network is working with another connections $W_y$, and the whole network is representing as: $$\mathbf{r_t} = f(\mathbf{W}_r\mathbf{r}_{t-1}+\mathbf{W}_x\mathbf{x}_t+\mathbf{b}_r)$$ and output as $$y_t = \mathbf{W}_y\mathbf{r}_t + \mathbf{b}_y$$
	- Back Propagation algorithm has to be upgraded to the time-based version, BPTT, due to the network architecture. $$\frac{\partial L}{\partial \mathbfit{r}_t} = \mathbf{W}_r^T\frac{\partial L}{\partial \mathbfit{r}_{t-1}} = [\mathbf{W}_r^T]^2\frac{\partial L}{\partial \mathbfit{r}_{t-2}} = \cdots.$$ Obviously, the gradient for the final layer is likely to grow extremely BIG when the norm of $\mathbf{W}_r$, $||\mathbf{W}_r||$ has a a maximum eigenvalue of $>1$ , and seemingly go vanished when eigenvalue $<1$ (ambiguous in the Primer).
	  Several solutions is in the References:
	  Network architecture work:
	  LSTM[^BPTT1], DeepResdualLeaning[^BPTT2] 
	  Initializing connectivity work:
	  paper[^BPTT3]
- CNN: kernel as neurons? Weights are shared among the kernels with same shape and channels. Also, weights are only relevant to the displacement between the pre- and postsynaptic neurons (I think it means the **pixels** in CV tasks, too.) $$W^{(i)}_{i_Ci_Hi_W,j_Cj_Hj_W} = W^{(i)}_{i_C,j_C}(i_H-j_H, i_W-j_W)$$ Therefore, the absolute spatial information is not used in the network, preserving the **spatial invariance** on processing.

# Questions
- What's the actual meaning of **spatial invariance**? in CV?

# Interesting Things to be Reminded



[^BPTT1]: Hochreiter, S., and Schmidhuber, J. (1997). Long short-term memory. Neural Comput. 9, 1735–1780. **==LSTM==** [links](http://refhub.elsevier.com/S0896-6273(20)30705-4/sref67)
[^BPTT2]: He, K., Zhang, X., Ren, S., and Sun, J. (2016). Deep residual learning for image recognition. In 2016 IEEE Conference on Computer Vision and Pattern Recog- nition (IEEE), pp. 770–778. 
[^BPTT3]: Le, Q.V., Jaitly, N., and Hinton, G.E. (2015). A simple way to initialize recurrent networks of rectified linear units. arXiv, 1504.00941 [links](https://arxiv.org/abs/) 1504.00941.
