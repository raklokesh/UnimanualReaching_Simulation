# UnimanualReaching_Simulation
Simulation of reaching with one hand in a straight line.

**Reaching Task**
1. The hand directly controls a cursor and the goal is to move to a target state i.e. (position, velocity) = (8,0)
2. The hand chooses one of the three acceleration actions  (-1, 0, 1) at each step of movement.
3. At each step the action is chosen in a epsilon-greedy manner and recevies a reward
4. Reward of 100 is given upon reaching the target state, else a reward of 0 is awarded on each step.

**Experiment Protocol**
_Training_
Each 'learner' participates in an experiment and learns by repeating reaching movement for a set number of trials (episodes). A policy is created here based on the state-action values.
_Post-test_
After the training, the learnt policy is put to test to see if it leads to a succesfull reach. If the reach is succesfull then the learner has learnt the right policy. 

**Parametric Testing**
Simulations were run for various combinations of exploration (epsilon = 0, 0.1, 0.5, 0.9, 1) and number of training episodes (episodes = 100, 500 ,1000) to find the most optimal training environement. 
100 learners (experiments) were tested for each combination of parameters.
The best combination of parameters will lead to highest proportion of successfull learners (experiments which lead to succesfull reach in the post test). 

**Results**
1. There are several possible policies for succesfull learning. Evolution of states for two of those policies are shown in the example plots.
2. Parametric testing revealed that epsilon = 0.5 and episodes = 1000 lead to most number of succesfull learning experiments (100%). Generally, epsilon of 0.5 performed the best and epsilon = 0 was by far the worst.