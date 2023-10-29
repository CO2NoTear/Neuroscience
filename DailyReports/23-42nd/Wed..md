# Main Job
- Read Primer, try to implement RNN

# What Have been Learnt
## Analyzing ANN
- ANN is not easy to interpret, in order to facilitate the side-by-side comparison, the same **==dimensionality reduction tool==** (e.g. PCA, etc.) which is commonly used for biological neural recordings should be used on ANNs' signals for visualizing and analyzing.
- To find the causal relationship from neurons to behaviors, an arbitrary set of neurons is to be **inactivated or lesioned** for a short time period, so that connections of selected two groups (the inactivated neurons, and the normal ones) can be lesioned to understand the reasons.

### Similarity Comparison
1. Calculating dissimilarity matrix for each network itself, and then calculating the correlation between the two dissimilarity matrices, higher correlation corresponds to more similar representations.
	- The dissimilarity matrix is D-by-D, with different inputs-outputs tuple correspondence. The result should indicate that input samples for the same category have more similar representations for each other, and more dissimilar to the samples in other categories.
2. Using linear regression to fit the responds of two networks:$$\mathbf{R}_2 \approx \mathbf{WR}_1 $$The performance of the linear regression is the similarity between two networks.
## Complex Tuning
Gradient ascent to find the best input as parameter to maximize the neuron activation.

## Dynamical system analysis
Find stable state $\mathbf{r}_{ss}$ such that the difference at $\mathbf{r}_{ss}$, $\mathbf{F}(\mathbf{r}_{ss})=0$. This stable state suggests how network store memories, accumulate information, transition between discrete states, etc.

## Objectives, network architectures, and training
ANN solutions are similar to an evolutionary in biology, which links environments to functions in biological organisms.
Doing ANN can help explaining the evolution path.

# Questions


# Interesting Things to be Reminded



[^1]:footnote here.
