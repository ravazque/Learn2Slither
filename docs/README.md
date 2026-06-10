*This project has been created as part of the 42 curriculum by ravazque.*

---

## Description

Learn2Slither is a **reinforcement learning** project: a snake agent that teaches itself to play through trial and error, using **Q-learning**.

The environment is a 10×10 board with a snake of initial length 3, two green apples (eating one grows the snake and gives a positive reward) and one red apple (shrinking it). The snake dies when it hits a wall, its own body, or when its length drops to zero.

The defining constraint is the agent's perception: it only sees the **four lines radiating from its head** (up, down, left, right). That limited vision is encoded into a discrete state, and the agent learns the value of each (state, action) pair through the Bellman update, balancing exploration and exploitation with an epsilon-greedy policy.

The project includes:

- **`environment.py`** — the board, the snake and the game rules.
- **`interpreter.py`** — turns the cross-shaped vision into the agent's state.
- **`agent.py`** — the Q-learning logic (update rule, epsilon-greedy action selection).
- **`snake.py`** — the entry point: training sessions, evaluation mode and the graphical interface, with models saved and reloadable after 1, 10, 100 and 1000 sessions.
