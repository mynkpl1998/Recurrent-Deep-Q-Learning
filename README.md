# Recurrent-Deep-Q-Learning

# Introduction
Partially Observable Markov Decision Process (POMDP) is a generalization of Markov Decision Process where agent cannot observe 
the underlying state only an observation is available. Earlier methods suggests to maintain the belief (a pmf) over all the possible states which encodes the probability of being in each state. This quickly limits the size of the problem to which we can use this method. However, the paper [Playing Atari with Deep Reinforcement Learning(https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)
