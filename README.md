# Recurrent-Deep-Q-Learning

# Introduction
Partially Observable Markov Decision Process (POMDP) is a generalization of Markov Decision Process where agent cannot observe 
the underlying state only an observation is available. Earlier methods suggests to maintain the belief (a pmf) over all the possible states which encodes the probability of being in each state. This quickly limits the size of the problem to which we can use this method. However, the paper [Playing Atari with Deep Reinforcement Learning](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf) presented an approach which uses last 4 observations as input to the learning 
algorithm to which can be seen as 4th order markov decision process. Many papers suggest that much performance can be obtained if we use more than last 4 frames but this is expensive from computational and storage point of view (experiece replay). Recurrent networks can be used to summarize what agent has seen in past observations. **In this project, I investgated this using a simple Partially Observable Environment and found that using an recurrent unit able to achieve much better performance than using some last k-frames.**
