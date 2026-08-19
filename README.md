HAFI-FL
Federated Learning for AI-Native 6G Edge Networks

> A simulation-based Federated Learning framework designed to study model training under heterogeneous data, unreliable clients, network constraints, mobility and limited communication in 6G edge environments.


In traditional Federated Learning, clients train locally and send model updates to a central server.

Real 6G edge networks are more challenging because clients can have:

- Different / non-IID data
- Limited bandwidth
- Variable latency
- Dropouts and unreliable connections
- Mobility and handovers
- Different update quality
- Communication constraints

**HAFI-FL** addresses these challenges by combining **client intelligence, network awareness, hierarchical aggregation and communication-efficient updates**.

---

Architecture

```text
             Global Aggregator
                     ▲
                     │
             Regional Aggregator
                     ▲
                     │
                Edge Nodes
                     ▲
                     │
        ┌────────────┼────────────┐
        │            │            │
     Client 1     Client 2    Client N
        │            │            │
        └────────────┼────────────┘
                     ▼
               Local Training
                     │
                     ▼
               HAFI Analysis
          ┌──────────┼──────────┐
          │          │          │
      Reputation  Diversity  Scheduling
          │          │          │
          └──────────┼──────────┘
                     ▼
             Edge Filtering
                     │
                     ▼
            Top-K Compression
                     │
                     ▼
              Network Delivery
                     │
                     ▼
           Hierarchical Aggregation
                     │
                     ▼
                Global Model

```
---
HAFI-FL studies whether these factors can be jointly considered during:

- Client selection
- Model aggregation
- Update filtering
- Communication
- Edge-level coordination

The main objective is to achieve a better balance between **accuracy, communication efficiency and network reliability**.

---

Experimental Setup

| Parameter | Configuration |
|---|---|
| Dataset | MNIST |
| Clients | 20 |
| Communication Rounds | 20 |
| Data Distribution | Non-IID |
| Dirichlet α | 0.18 |
| Model | MLP |
| Model Architecture | 784 → 128 → 10 |
| Local Epochs | 1 |
| Batch Size | 64 |
| Evaluation | Multi-seed, Ablation & Stress Testing |

---

Algorithms Compared

The framework compares HAFI-FL against established Federated Learning approaches:

- **FedAvg** – Standard federated averaging
- **FedProx** – Handles client heterogeneity using proximal regularization
- **Personalized-FL** – Allows client-specific adaptation
- **Median** – Robust aggregation baseline
- **Trimmed Mean** – Robust aggregation baseline
- **HAFI-FL** – Proposed framework
- **HAFI-FL + Top-K** – Communication-efficient HAFI variant

---



### Two Main Comparison Modes

**Aggregation-only experiment**

```text
Same clients
     ↓
Different aggregation algorithms
     ↓
Compare learning behavior
```

