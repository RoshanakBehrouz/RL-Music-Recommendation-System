# 🎵 Music Recommendation System with Q-Learning

This repository contains a Python-based music recommendation system that leverages **Q-Learning**, a fundamental algorithm in reinforcement learning. The system simulates user feedback to train an agent that learns to recommend music genres effectively, aiming to maximize user satisfaction over time.

---

## 🌟 Features

- **🎓 Q-Learning Agent**: Learns optimal recommendation policies over time.
- **👤 Simulated User Profiles**: Includes various user types (e.g., *Pop Lover*, *Rock Enthusiast*) with distinct preferences.
- **⚙️ Dynamic Training**: Trains over multiple episodes using feedback to improve recommendations.
- **🎲 Epsilon-Greedy Policy**: Balances exploration and exploitation for effective learning.
- **📈 Performance Visualization**:
  - Learned Q-Table Heatmap
  - Average Reward Over Time
  - Epsilon Decay Curve
  - Action (Genre) Distribution
- **📋 Policy Output**: Displays learned policies and detailed Q-values.
- **📊 Comparative Analysis**: Compare learning outcomes for different user profiles.

---

## 🧠 How It Works

The system models music recommendation as a **reinforcement learning** problem:

- **Agent**: `MusicRecommendationAgent` selects music genres.
- **Environment**: Simulated user returns a reward after each recommendation.
- **States**: Current genre (or context) the agent is in.
- **Actions**: Recommending a genre.
- **Rewards**: Feedback for recommendation (e.g., `+10` for liked, `-5` for skipped).
- **Q-Table**: A lookup table for expected future rewards, updated using the Q-learning formula:

## 
$$ Q(s, a) ← Q(s, a) + α [ r + γ max_a' Q(s', a') − Q(s, a) ] $$


Where:

- `Q(s, a)` = current Q-value  
- `α` = learning rate  
- `γ` = discount factor  
- `r` = reward  
- `s'` = next state  
- `a'` = next action

Through repeated interactions, the agent learns which recommendations yield higher cumulative rewards.

---

## 🚀 Installation

1. **Clone the Repository**:

git clone https://github.com/RoshanakBehrouz/RL-Music-Recommendation-System.git
cd your-repo-name


2. **Install Dependencies**:
pip install numpy matplotlib seaborn pandas

3.**Run the Notebook**:
jupyter notebook "RLFinal.ipynb"

## Usage
Run all cells in the notebook.

The main() function will:

Train a general agent.

Train agents on specific user profiles.

Generate and display visualizations.

Print learned policies and sample recommendations.

## Output Visualizations
Q-Table Heatmap: Learned Q-values for each state-action pair.

Reward Curve: Tracks average reward across episodes.

Epsilon Decay: Shows shift from exploration to exploitation.

Action Distribution: Frequency of genre recommendations.

## 💡 Future Enhancements
🔌 Real User Data: Integrate Spotify API or similar for live data.

🧠 Richer State Representation: Add user mood, time of day, and history.

🚀 Advanced RL Algorithms: Implement Deep Q-Networks (DQNs).

🖥 Web Interface: Build a front-end to interact with the agent.

💬 Custom Rewards: Base rewards on user engagement (likes, skips, etc).



