# Main Job
- [x] Read about ToT
- [x] Watch ToT video
- [ ] Read new papers

# What Have been Learnt
- ToT evaluation: Multiple times of evaluation is preferred.
	1. Strategy 1. is done with LLM to reason about the given state to generate a scalar or ordered classification that approximately tells "good" or "bad" between states. To implement that reasoning, a "value prompt" is given to the LLM.
	2. Strategy 2. is to vote out the "good" state based on deliberately comparison in a "vote prompt". More like a step-wise self-consistency CoT.
- ToT searching: BFS for constrained searching space, and DFS for others. DFS backtracks when the evaluator deems a state as "impossible".
- According to the video: evaluators are reliable mainly because machine learning models are **==more capable with evaluating whether two things fit each other==** than generating a new things.
- The ToT actually implemented a new programming scheme to build a prompt algorithm with the LLM as a tool function $p(\mathit{x});$ 
# Questions
- What if the LLM consider that no possible solution exists in the searching tree nodes? Will it give up to give out an answer?

# Interesting Things to be Reminded



[^1]:footnote here.
