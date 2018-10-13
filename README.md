# Recurrent-Deep-Q-Learning

# Introduction
Partially Observable Markov Decision Process (POMDP) is a generalization of Markov Decision Process where agent cannot observe 
the underlying state only an observation is available. Earlier methods suggests to maintain the belief (a pmf) over all the possible states which encodes the probability of being in each state. This quickly limits the size of the problem to which we can use this method. However, the paper [Playing Atari with Deep Reinforcement Learning](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf) presented an approach which uses last 4 observations as input to the learning 
algorithm to which can be seen as 4th order markov decision process. Many papers suggest that much performance can be obtained if we use more than last 4 frames but this is expensive from computational and storage point of view (experiece replay). Recurrent networks can be used to summarize what agent has seen in past observations. **In this project, I investgated this using a simple Partially Observable Environment and found that using an recurrent unit able to achieve much better performance than using some last k-frames.**

# Environment

Environment used was a 9x9 grid where *Red* colored blocks represents agent location in the grid. *Green* colored blocks are the goal points for agent. *Blue* colored blocks are the blocks which agent needs to avoid. A reward of +1 is given to agent when it eats *green* block. A reward of -1 is given to the agent when it eats *blue* block. Other movements results in zero.
Observation is the neigbouring cells of agent. Below figure describes the observation.

Underlying MDP             |  Observation to Agent          
:-------------------------:|:-------------------------:
![](https://raw.githubusercontent.com/mynkpl1998/Recurrent-Deep-Q-Learning/master/data/download%20(1).png)  |  ![](https://raw.githubusercontent.com/mynkpl1998/Recurrent-Deep-Q-Learning/master/data/download.png) 

# Algorithm

![](https://raw.githubusercontent.com/mynkpl1998/Recurrent-Deep-Q-Learning/master/data/algo.png)
