🌟 CustomAlign-RLHF

A lightweight, end-to-end RLHF pipeline for aligning language models using custom datasets.

CustomAlign-RLHF provides a simplified and modular implementation of Reinforcement Learning from Human Feedback (RLHF), enabling developers and researchers to align LLMs using their own domain-specific data.
The project covers the full pipeline: Supervised Fine-Tuning (SFT) → Reward Modeling → PPO Policy Optimization, similar to how modern aligned models like ChatGPT are trained.

🚀 Features

Custom Dataset Support — Train LLMs using your own instruction and preference data.

Supervised Fine-Tuning (SFT) — Teach base models task-specific behavior.

Reward Model Training — Learn human preferences using pairwise comparison data.

PPO-based RL Optimization — Align model behavior with rewards using TRL.

Modular Codebase — SFT, reward modeling, and RL steps separated for clarity.

Lightweight & Accessible — Works on Kaggle/Colab with small models.

🛠️ Tech Stack

Python

HuggingFace Transformers

HuggingFace Datasets

TRL (for PPO training)

PyTorch

📁 Project Structure
CustomAlign-RLHF/
│
├── SFT/                   # Supervised fine-tuning scripts
├── rewardModeling/        # Reward model training scripts
├── policyOptimization/    # PPO alignment training
├── assets/                # Images/diagrams used in README
├── Judger/                # Preference pair evaluator (if included)
├── LICENSE
└── README.md

📘 RLHF Pipeline Overview
1️⃣ Supervised Fine-Tuning (SFT)

Train the base model on your instruction-response dataset to give meaningful outputs.

2️⃣ Reward Modeling

Train a model to score which response humans prefer using comparison pairs.

3️⃣ PPO Policy Optimization

Use the reward model to guide the policy model in producing more aligned responses.

📊 Example Use Cases

Domain-specific chatbots

Legal, medical, retail, or educational AI assistants

Safety-aligned LLM experiments

Learning + research on RLHF workflows

Fine-tuning small LLMs on custom instructions

▶️ Getting Started

Clone the repository:

git clone https://github.com/deepak109patel/CustomAlign-RLHF.git
cd CustomAlign-RLHF


Install dependencies:

pip install -r requirements.txt


Run SFT training:

python SFT/train_sft.py


Train reward model:

python rewardModeling/train_reward_model.py


Run PPO alignment:

python policyOptimization/train_ppo.py

📑 Dataset Format
SFT Dataset
{
  "prompt": "Explain overfitting in ML.",
  "response": "Overfitting occurs when a model learns noise instead of general patterns..."
}

Reward Modeling Dataset
{
  "prompt": "Write a short poem.",
  "response_a": "...",
  "response_b": "...",
  "chosen": "b"
}

🤝 Contributing

Contributions, issues, and suggestions are welcome.
Feel free to open a PR!

📄 License

This project is licensed under the MIT License.
