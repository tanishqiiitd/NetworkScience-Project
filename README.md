# 📦 E-Commerce Optimization using Network Science

A graph-powered framework for intelligent product recommendation, pricing sensitivity analysis, and influence modeling — using the Amazon Co-Purchasing Network.

---

## 🧠 Project Overview

This project applies **network science techniques** to enhance e-commerce intelligence. Using the **Amazon0601 co-purchasing dataset (SNAP)**, we build graph models to deliver 5 key modules:

### 🚀 Deliverables

1. **Product Bundle Generator**  
   Uses **Louvain community detection** to cluster frequently co-purchased products for upselling and co-marketing.

2. **Sensitivity Matrix via Influence Diffusion**  
   Models pricing ripple effects across the product network using:  
   `S = βA + βαA²`  
   where `A` is the adjacency matrix, and `β`, `α` are tunable influence weights.

3. **Fault-Tolerant Recommender System**  
   Identifies **backup recommendations** using 2-hop neighbors for the top 1000 high-degree products.

4. **Influence Simulation (Cascade Model)**  
   Runs a **probabilistic diffusion** from top betweenness centrality nodes to simulate viral marketing.

5. **Eigenvector Centrality-Based Product Ranking**  
   Ranks products by their recursive influence using eigenvector centrality. Visualizes top 20 influential products.

---

## 📂 Files

| File                             | Description |
|----------------------------------|-------------|
| `Database.txt`                  | Full SNAP dataset (Amazon0601) |
| `reduceddataset.txt`           | Pruned dataset for Louvain and influence analysis |
| `reduceddataset14k.txt`        | Small test graph for cascade simulation |
| `del1_community_bundle.py`     | Product bundle generator using Louvain clustering |
| `del2_sensitivity_matrix.py`   | Builds pricing sensitivity matrix |
| `del3_fault_tolerant_recommender.py` | Recommender failover using 2-hop centrality |
| `del4_cascade_simulation.py`   | Independent cascade model for influence spread |
| `del5_eigenvector_influence.py`| Eigenvector centrality and top influencer chart |
| `sensitivity_matrix.npz`       | Precomputed matrix from Deliverable 2 |
| `Mini Project NS_Group52.pdf`  | Final report (concepts, results, applications) |

---

## ⚙️ How to Run

Each deliverable code is in a jupyter notebook, just run them in a supported IDE.
