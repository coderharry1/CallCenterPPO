# 📞 Optimising Call Centre Operations with Reinforcement Learning (PPO)

**University of Adelaide – Master’s Final Year Project**  
*Supervisor: Dr. Wathsala Karunarathne*  

---

## 🚀 Project Overview  

Traditional call centre routing systems rely on **static, rule-based allocation**, often leading to:  
- ⏳ Longer wait times  
- ❌ Lower first-call resolution rates  
- 😡 Declining customer satisfaction  

This project builds a **Reinforcement Learning (RL)**-based solution using **Proximal Policy Optimisation (PPO)** to dynamically assign calls to agents. Unlike static rules, the RL agent continuously adapts to:  
- Real-time queue conditions  
- Agent expertise and availability  
- Call complexity and topic variation  

---

## 🔑 Key Results  

✅ **18% improvement** in customer satisfaction  
✅ **15% increase** in first-call resolution rates  
✅ Average wait time reduced to **54.5s** (vs. 67s baseline)  
✅ Maintained strong performance during **peak call loads**  
✅ Achieved improvements **without extra staffing costs**  

⚡ *This proves reinforcement learning can optimise large-scale service systems in the real world.*  

---

## 🛠️ Technical Stack  

- **Languages:** Python (Pandas, NumPy, Scikit-learn)  
- **RL Frameworks:** PyTorch, Stable Baselines3  
- **Simulation:** Custom **OpenAI Gym environment** (CallCenterEnv)  
- **Visualisation:** Matplotlib, Seaborn  
- **Data:** 10,000+ historical call centre records (ModifiedCallCenter.xlsx)  

---

## 🧠 Methodology  

1. **Data Engineering**  
   - Cleaned 10k+ call logs  
   - Engineered features: *Call Congestion Index, Hourly Call Trends, Agent Performance Tiers*  

2. **Environment Design**  
   - Built a custom **Gym-compatible environment** simulating queue lengths, call topics, and agent efficiency  

3. **Reward Function**  
   - Balanced **wait time, resolution success, satisfaction scores, agent-topic match**  

4. **PPO Agent Training**  
   - Actor-Critic networks (2×256 units, ReLU)  
   - Trained for **200+ episodes**  
   - Tuned hyperparameters (γ=0.99, λ=0.95, ε=0.2, lr=3e-4)  

5. **Evaluation**  
   - Benchmarked against rule-based routing  
   - Tested across peak hours & topic complexities  

---

## 📊 Performance Summary  

| Metric                        | Baseline | PPO Agent | Δ Improvement |
|-------------------------------|----------|-----------|---------------|
| Avg Wait Time (sec)           | 67       | **54.5**  | ↓ 19% |
| First Call Resolution (FCR)   | 0.63     | **0.73**  | +15% |
| Customer Satisfaction (1–5)   | 2.5      | **2.95**  | +18% |
| 90th Percentile Wait (sec)    | 140      | **111**   | ↓ 21% |

---
## 📈 Key Visuals  
![Wait Time Reduction](<img width="347" height="185" alt="Screenshot 2025-08-25 at 11 41 55 AM" src="https://github.com/user-attachments/assets/afeae65d-8016-4894-92dd-ece1955dad53" />
)  
![Agent Satisfaction Heatmap](<img width="317" height="213" alt="Screenshot 2025-08-25 at 11 44 35 AM" src="https://github.com/user-attachments/assets/8a607289-1a9a-47bd-9f1e-10142ef68842" />
)  

## 🌍 Business Impact  

- **Customer Experience** → Faster response + higher satisfaction → stronger retention.  
- **Operational Efficiency** → Better agent allocation without new hires.  
- **Scalability** → PPO adapts to real-time spikes (weekends, seasonal campaigns).  
- **Transferability** → Approach generalises to *banking hotlines, healthcare helplines, and IT service desks*.  

---

## 📂 Repository Structure  

```
├── CallCenterPPO.ipynb      # Full training + evaluation notebook
├── environment.py           # Custom OpenAI Gym call centre environment
├── data/
│   └── ModifiedCallCenter.xlsx   # Call centre dataset
├── results/
│   ├── training_rewards.png
│   ├── wait_time_reduction.png
│   └── agent_heatmap.png
└── README.md                # This file
```

---

## ▶️ How to Run  

```bash
# Clone repo
git clone https://github.com/coderharry1/CallCenterPPO.git
cd CallCenterPPO

# Install dependencies
pip install -r requirements.txt

# Run PPO training
python CallCenterPPO.ipynb
```

---

## 📌 Future Directions  

- Add **customer segmentation** for personalised routing  
- Deploy prototype in **cloud-native environments (AWS / GCP)**  
- Extend to **multi-agent reinforcement learning** for distributed call centres  

---

## 🙏 Acknowledgements  

Special thanks to **Dr. Wathsala Karunarathne** for her guidance in reinforcement learning and optimisation, and to the University of Adelaide’s **School of Mathematical Sciences** for academic support.  
---

## 🔗 Links  
👉 Explore the full code + training logs here: [CallCenterPPO.ipynb](https://github.com/coderharry1/CallCenterPPO/blob/main/CallCenterPPO.ipynb)
