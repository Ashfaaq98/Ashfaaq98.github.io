+++
title = "Technique Inference Engine (TIE) 🎯"
date = 2026-02-18T00:00:00+00:00
draft = false
summary = "Predicts associated MITRE ATT&CK® techniques from observed adversary behavior using WALS matrix factorization."
technologies = ["Python", "Machine Learning", "MITRE ATT&CK", "Matrix Factorization"]
+++

## 🎯 Project Overview

The **Technique Inference Engine (TIE)** is a powerful tool designed to help cyber defenders forecast an adversary's next steps. By analyzing previously observed MITRE ATT&CK® techniques, TIE predicts likely associated techniques that may not have been detected yet or are planned by the attacker.

This project is an extension of the [MITRE Center for Threat-Informed Defense (CTID) TIE project](https://github.com/center-for-threat-informed-defense/technique-inference-engine), adding trained models, evaluation scripts, and enhanced inference utilities.

---

### 🚀 Key Features

- **🧠 Predictive Modeling:** Uses Weighted Alternating Least Squares (WALS) matrix factorization to learn latent embeddings for threat reports and ATT&CK techniques.

- **📊 Co-occurrence Analysis:** Learns from technique co-occurrence data to identify patterns in adversary behavior.

- **🛠️ Comprehensive Utilities:** Includes scripts for training models with full hyperparameter search, evaluating performance, and running inference on new data.

---

### 🧪 How it Works

The engine maps observed behavior to the MITRE ATT&CK framework and uses recommendation system algorithms to suggest the most probable "next" or "missing" techniques. This allows SOC analysts and threat hunters to:
- Fill gaps in visibility.
- Anticipate attacker maneuvers.
- Prioritize defensive telemetry.

---

### 🔗 Explore the Repository

- **GitHub Repository:** [Ashfaaq98/TIE](https://github.com/Ashfaaq98/TIE)

---
