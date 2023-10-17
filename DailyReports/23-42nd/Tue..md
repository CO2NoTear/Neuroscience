# Main Job
- Read Primer, Impl RNN.

# What Have been Learnt
- Non-linear activation function is the essence for the power of ANNs. Biologically, the activation neurons can be analogized to the counterparts in a brain.
	- ReLU is often used in feedforward networks $$f(x) = max(x,0)$$mainly for it's derivative is 1 for neurons with positive outputs, and is manually set to 0 with negative outputs. Maybe that's for the good of the BP algorithm, because it allows high value output in the network, namely non-saturating. 
	- Hyperbolic tangent function is often used in RNN $$f(x)=tanh(x)=\frac{sinh(x)}{cosh(x)}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$
	- Normalization: $$\hat x=\gamma\frac{x_i-\mu}{\sigma}+\beta$$Quite common in statistical math, ensuring the actual input for the network, $\hat x$, has same mean, $\beta$, and same variance, $\gamma$, and both of these two parameters are trainable.
- Improvement on SGD:
	- Learning rate decay: gradually decay learning rate to encourage finer-tuning params.
	- Momentum: strides $\Delta \theta$ based on smoothed gradient $\mathbf{v}^{(j)}$ ,$$\mathbf{v}^{(j)}=\mu \mathbf{v}^{(j-1)} + \frac{\delta L^{(j)}}{\delta \theta}, \quad 0<\mu<1$$$$\Delta \theta = -\eta \mathbf{v}^{(j)}$$
	- Regularization: *learnt in Machine Learning.*
- RNNs can be compared with brains, side-by-side. Many levels are included:
	- [?] Single-neuron activity and selectivity
	- [?] Population decoding
	- [?] State-space dynamics
	- [?] Network responses to perturbation
- by building RNN on perceptual decision task parallel to subject animals, **==examining RNN's dynamics==** can explain neuron activation pattern. Task irrelevant features are presented, but selectively filtered out and integrated over time during evidence accumulation.
	- It enlightens that by building a better RNN on challenging tasks may reveal more about the brain mechanism. 
- RNN in neuroscience should use continuous time scale, which means the derivative of $r(t)$ should be modified as below: $$\tau \frac{d\mathbf{r}}{dt} = -\mathbf{r}(t)+f(\mathbf{W}_r\mathbf{r}(t)+\mathbf{W}_x\mathbf{x}(t)+\mathbf{b}_r)$$where $\tau$ is a tiny single-unit timescale. Furthermore, the BPTT algorithm need to be modified, too. For instance, the **==FORCE==** algorithm modifying the output connection $\mathbf{W}_y$ with the least-square algorithm (最小二乘法) to match the target output, and the output is fed back to the network through $\mathbf{W}_{fb}$.$$\tau \frac{d\mathbf{r}}{dt} = -\mathbf{r}(t)+f(\mathbf{W}_r\mathbf{r}(t)+\mathbf{W}_x\mathbf{x}(t)+\mathbf{W}_{fb}y(t)+\mathbf{b}_r)$$$$y(t)=\mathbf{W}_y^T\mathbf{r}(t)$$ Extracting that, we get $$\tau \frac{d\mathbf{r}}{dt} = -\mathbf{r}(t)+f([\mathbf{W}_r+\mathbf{W}_{fb}\mathbf{W}_y^T]\mathbf{r}(t)+\mathbf{W}_x\mathbf{x}(t)+\mathbf{b}_r)$$
 
# Questions
- How do scientists ==EXAM== RNN's dynamic? By eyes? with hand-made models? or with ANN?[^1]

# Interesting Things to be Reminded



[^1]:Mante, V., Sussillo, D., Shenoy, K.V., and Newsome, W.T. (2013). Context- dependent computation by recurrent dynamics in prefrontal cortex. Nature 503, 78–84 [links](http://refhub.elsevier.com/S0896-6273(20)30705-4/sref110)
