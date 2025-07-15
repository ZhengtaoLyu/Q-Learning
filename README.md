# Cliff Walking Q-Learning Agent 🧠🏃

## 📌 Description  
This repository implements a Q-learning agent to solve the Cliff Walking grid-world problem, a classic environment in reinforcement learning.

本项目实现了一个 Q-learning 智能体，用以解决 Cliff Walking（悬崖行走）问题，是强化学习经典实验之一。

---

## 📊 Project Structure / 项目结构

| File | Description |
|------|-------------|
| `cliff_walking_q_learning.m` | Main training loop for Q-learning |
| `next_state.m` | Transition logic: from state & action to next state & reward |
| `plot_path.m` | Optional animation for each episode |
| `plot_stoch_pol.m` | Arrow-plot of the policy & most likely path |

---

## 🔁 Algorithm: Q-learning with ε-greedy

- Update Rule:  
   Q(s,a) \leftarrow Q(s,a) + \alpha \left[ R + \gamma \max_a Q(s',a) - Q(s,a) \right] 

- Policy:  
  ε-greedy (0.1): mostly exploit, sometimes explore

- Reward Design:  
  - Reaching goal: `-1`  
  - Walking step: `-1`  
  - Falling off cliff: `-100`

---

## 🔍 Parameters / 超参数设置

| Parameter | Value | Description |
|----------|--------|-------------|
| `alpha`  | 0.5    | Learning rate |
| `gamma`  | 1.0    | Discount factor |
| `epsilon`| 0.1    | Exploration rate |

---

## 📈 Outputs

- `Returns per Episode` plot
- Learned policy arrows (quiver)
- Shortest path visualization
- Optional animated path per episode

---

## 📚 Reference / 引用来源

- Sutton & Barto (2018). Reinforcement Learning: An Introduction (Ch. 6: Temporal-Difference Learning)  
  [[Online Book]](http://incompleteideas.net/book/the-book-2nd.html)

---

## ✅ To Run / 运行方式

```matlab
% In MATLAB:
cliff_walking_q_learning
