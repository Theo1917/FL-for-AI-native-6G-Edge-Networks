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
