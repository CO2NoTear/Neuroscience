# Terms
- connectome
> a matrix that represents all possible pairwise anatomical connections between neural elements

- connectomics
> 联结主义学派

- track tracing
> 神经元束追踪（一种用来示踪的技术）

- characteristic path length
> The length of the shortest path between 2 selected nodes.

- clustering coefficient
> 聚类系数，衡量邻居节点成为团的

- preferential attachment
> new nodes added to another node $j$ with a **probability** that is proportional to the **degree** of $j$

# Emergence of Neuroscience
## 1. Development of Networks
[[Watts and Strogatz's Work|Watts and Strogatz]] developed the "small-world" network theory for big natural network.
## 2. Evolution of Methods in Visualizing Brain Network
- Tract tracing
- MRI
- etc.
# Graph Theory
## Small-world
>[!NOTE]- Watts-Strogatz "small-world"
> ![[Watts and Strogatz's Work]]
## Scale-free Network
> [!Note]- Barabási–Albert model
> - Preference attachment
> Adding notes to the network with the strategy of connecting new nodes to a node based on the **degree** of that existing node.
> 	-*richer get richer*
> - power-law distribution
> The **degree** of the network (referring to the degree distribution among all the nodes) follows the **power-law distribution**
> For any node in the BA-model, the probability of the degree of that point equaling to a natural number $k$ is proportionated with a (negative) **power** of $k$:
> $$ P(k) \propto \frac{1}{k^\gamma} \ \mbox{ where }\gamma>0 $$
> Mostly, $\gamma$ is around 2...3
## Modularity
>[!Note]- Modules the sub-network
>Big real-world network can be nearly decomposed into subsets with highly interconnected nodes in each subset, meanwhile the connectivity between nodes in different subsets are week. These subsets are called **Modules**, and the quantifier of connectivity in the **modules** is called **Moduarity**

## Motifs (less important)
>[!help]- Topological Motifs of a Network
> More at Chap. 8, which is not involved in initial plan of the learning.

## Interesting properties
- Complex network are fairly resilient to random attack, but are much more vulnerable to a targeted attack that aiming at **hub nodes** with high degree.

# Space, Time and Topology
- Purely topology don't exist in space, or space (web) and time (sonnets).
	- Semantic web, World Wide Web, Shakespeare's sonnets.
- Biological network are particularly embedded in **spatial** dimensions and are dynamically active over **time**. ==**Brain**== is one of them.
	- Brain network analysis use 5 dimensions: ==3(space)+1(time)+1(topology).==
- Topology is constrained with spatial built plan in real world.
	- CPU circuit design is a good example of that.
- **Topology** of a network has a **important influence on the ==functional==** dynamics that emerge from interactions between nodes over time.
- 