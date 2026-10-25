# 🐦 Flappy Bird AI using Deep Q-Learning (DQN)

A reinforcement learning project where an AI agent learns to play **Flappy Bird** using a **Deep Q-Network (DQN)** implemented with **PyTorch** and **Gymnasium**.

## 🚀 Features

- Deep Q-Network (DQN)
- Experience Replay
- Target Network
- Epsilon-Greedy Exploration
- Automatic model saving
- Training and testing modes
- Flappy Bird Gymnasium environment

## 🧠 How It Works

The AI agent interacts with the Flappy Bird environment and learns which action to take:

- **0** → No Flap
- **1** → Flap

During training, experiences are stored in replay memory. Random batches of previous experiences are then used to train the neural network.

The agent gradually reduces random exploration using epsilon decay and learns to select actions that maximize its total reward.

## 🛠️ Technologies Used

- Python
- PyTorch
- Gymnasium
- Flappy Bird Gymnasium
- PyYAML
- Pygame

## 📂 Project Structure

```text
flappybird_rl/
│
├── agent.py               # DQN agent and training logic
├── dqn.py                 # Deep Q-Network architecture
├── experience_replay.py   # Experience replay memory
├── game_flappy_bird.py    # Manual Flappy Bird environment
├── parameters.yaml        # Hyperparameters
└── README.md
```

## ⚙️ Hyperparameters

The training configuration is stored in `parameters.yaml`.

Some of the main parameters include:

- Learning Rate: `0.001`
- Discount Factor (Gamma): `0.99`
- Initial Epsilon: `1.0`
- Minimum Epsilon: `0.05`
- Epsilon Decay: `0.9995`
- Replay Memory Size: `100000`
- Mini Batch Size: `32`

## ▶️ Train the Agent

Run:

```bash
python agent.py flappybirdv0 --train
```

## 🎮 Test the Trained Agent

After training, run:

```bash
python agent.py flappybirdv0
```

The trained model will be loaded and the Flappy Bird environment will be rendered.

## 📈 Learning Process

The agent learns by:

1. Observing the current game state.
2. Selecting an action using epsilon-greedy exploration.
3. Performing the action.
4. Receiving a reward and next state.
5. Storing the experience in replay memory.
6. Sampling previous experiences.
7. Updating the DQN using the calculated Q-values.
8. Periodically synchronizing the target network.

## 🎯 Goal

The goal of this project is to understand and implement **Deep Reinforcement Learning** by training an AI agent to improve its Flappy Bird gameplay through experience.

## 👨‍💻 Author

**Aparesh Mondal**

BE – Artificial Intelligence & Machine Learning  
RR Institute of Technology, Bengaluru
