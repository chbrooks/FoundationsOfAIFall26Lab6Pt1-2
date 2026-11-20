### Lab 6, part 1. MDPs and Q-learning

#### Due Dec 8, 11:59pm. 

To submit, add your answers here as a PDF.

**Value iteration**

1. Set the battery level to 7 and reset value iteration. Predict: after one sweep, which cells will have a positive (green) value? Press Sweep once and check. Then sweep up to 8 times and describe how the green region grows. What does one sweep mean in terms of how many moves ahead the drone is looking?
2. Press Run to convergence. Record the sweep where the policy stopped changing and the sweep where value iteration converged. Why could you stop early and still have the optimal policy? What would you risk by stopping early in general?
3. Predict: will γ = 0.99 need more or fewer sweeps than γ = 0.95? Check, and explain the difference using what γ does to each update.

**Policy iteration**

4. Starting from Fly straight at the hiker, how many evaluations does policy iteration need? Starting from Always fly north? Compare these with the number of value iteration sweeps. Why does policy iteration need so few rounds, and what does each round cost?

**Battery is part of the state**

5. Look at column 3, row 5 (two cells east of base). Step through battery levels 1 to 7 and record the best move and value at each. Explain why the best move changes. What would go wrong if the state were position alone?
6. The charging pad shows the same value at every battery level. Why?

**Discounting**

7. Compare γ = 0.6, 0.8, 0.95 and 0.99. Does the route change? Does the value at base change? How can the values change while the policy stays the same?

**Wind and Rewards**
8. Set wind slip to 0, then 0.3, then 0.5. For each, record the optimal drone's success rate and what it does at base. At what point does the drone refuse to fly, and why? 
9. Predict: what happens if the crash reward is −100 instead of −20? Check. Then try −5. What does this say about how reward design sets the drone's attitude to risk? 
10. Set the reward per move to 0, then to −1. Does the route change? With γ below 1, why might a per-move cost matter less than you expect?

**Q-learning**

11. Press Fly one flight a few times. After each flight, which Q-values changed, and how many? Does a flight that crashes teach the drone anything useful? What?

12. Keep flying (use +100 flights and then single flights) until the first flight that reaches the hiker. In the Q-values view, how many triangles anywhere on the map are positive? Why only that many? 

**Exploration and coverage**

13. Reset, then add 3,000 flights. Record the learned policy's value at base and the optimal value. Then go to Fly a mission: how does the learned drone's success rate compare with the optimal drone's?

14. Predict: what happens with ε = 0? Reset, set ε to 0, and add 3,000 flights. Compare with the previous question.  Use the Visits view to explain the difference.
15. With flights starting at base, open the Visits view at battery 7. The stats line shows how many states were ever visited. Why are some states never visited, no matter how long you train? Does it matter that the drone never learns good moves there?
16. Switch Each flight starts to In a random state, reset, and add 3,000 flights. Now every state gets visited. Yet the value at base may be lower than in question 18. Compare the number of moves in the stats line and explain why.

**Learning rate and noise** 

17. With the default wind, compare α = 0.1 and α = 0.5 after 3,000 flights each. Watch the value chart as you train. What happens with the larger α, and why?
18. Set wind slip to 0 and repeat α = 0.5. Explain why a large learning rate is fine without wind but harmful with it.
Turn on Halve ε every 1,000 flights and train again. What happens to the training success rate? What is the trade-off?

19. Value iteration converged in about 60 sweeps. Q-learning needed thousands of flights and tens of thousands of moves to get close. What did value iteration have that Q-learning did not? For a real rescue drone, why might that be unavailable?