# 🌐 Network Analysis of User Participation and Upvote Distribution in r/datascience

**Author:** Faizan Waheed  
**Email:** fawaheed@iu.edu  
**Institution:** Indiana University Bloomington  
**Date:** March 2025  

---

## 📘 Overview

This project explores **user participation and recognition patterns** in the `r/datascience` subreddit through network analysis.  
Two networks were constructed to capture different aspects of user behavior:

1. **Participation Network** – Represents how users interact with subreddit flairs (Discussion, Projects, ML, AI, and Coding) through posts and comments.  
2. **Upvote Network** – Maps how recognition (via upvotes) is distributed among users across the same flairs.

The analysis reveals a distinction between **engagement and influence** — while users participate in multiple topics, **upvotes tend to cluster within specific technical domains**, showing that recognition is specialization-driven.

The full academic report is included as:  
📄 **Project Report.pdf**

---

## 🎯 Objectives

- Construct two networks (Participation & Upvote) using data from `r/datascience`.  
- Analyze structural properties such as **modularity, assortativity, degree, and conductance**.  
- Identify which flairs act as hubs for engagement vs. influence.  
- Compare participation and recognition to reveal community behavior patterns.  
- Visualize and interpret user-flair interactions using **Gephi**.

---

## 🧠 Data Collection

**Source:** Reddit API accessed via **PRAW (Python Reddit API Wrapper)**  
**Timeframe:** January 2025  
**Subreddit:** `r/datascience`

Two datasets were collected:
- **Comment Participation Dataset:** Posts/comments across 5 main flairs  
- **Upvote Distribution Dataset:** Upvotes received by users per flair

Each dataset was cleaned, aggregated, and exported as **CSV files** containing:
- Node attributes (users, flairs)
- Edge relationships (participation or upvote links)

All data collection complied with Reddit’s API Terms of Service and excluded any personal user identifiers.

---

## 🧩 Methodology

### 🕸 Network Construction
- **Nodes:** Users + Flairs  
- **Edges:** Represent user participation or received upvotes under a specific flair  
- **Attributes:** 
  - For Participation Network → Posts & Comments  
  - For Upvote Network → Total Upvotes  

### 🧮 Analysis Metrics
- **Degree Centrality** – Measures cross-flair engagement  
- **Betweenness Centrality** – Identifies influential hubs  
- **Modularity & NMI (Normalized Mutual Information)** – Evaluate community separation  
- **Assortativity & Conductance** – Assess within-flair interaction strength  

### 🧰 Tools & Libraries
- `Python 3.10+`
- `PRAW`
- `pandas`, `networkx`, `numpy`
- `matplotlib`
- `Gephi` (for visualization)

---

## 📊 Key Findings

### 1. **Participation Network**
- **Nodes:** 222 (217 users + 5 flairs)  
- **Density:** 0.0102 → Sparse but interconnected  
- **Modularity:** 0.668 → Distinct but overlapping topic groups  
- **Key Hubs:** **Projects** and **AI** — major bridges across flairs  

**Insights:**
- Users often engage in at least **two different flairs**.  
- Projects & AI drive **cross-topic discussions**, fostering interdisciplinary exchange.  
- Communities are primarily flair-based but not isolated.

---

### 2. **Upvote Network**
- **Nodes:** 233 (including users who received upvotes but didn’t comment)  
- **Density:** 0.0092 → More selective engagement  
- **Modularity:** 0.712 → Highly distinct recognition communities  
- **Key Hubs:** **ML** and **Coding** — dominate in upvote influence  

**Insights:**
- Recognition (upvotes) is **more concentrated** and flair-specific.  
- Technical content (ML, Coding) gains the most visibility and appreciation.  
- Upvotes tend to remain within the same flair community.

---

### 3. **Participation vs. Recognition Comparison**

| Metric | Participation Network | Upvote Network | Insight |
|--------|-----------------------|----------------|----------|
| Modularity | 0.668 | **0.712** | Recognition is more specialized |
| NMI (Flair Alignment) | 0.845 | **0.880** | Upvotes align more with flair categories |
| Assortativity | 0.720 | **0.801** | Upvotes are more flair-confined |
| Avg. Degree | 2.252 | 2.146 | Users comment across more flairs than they get upvotes from |
| Conductance | 0.132 | **0.088** | Upvote communities are more isolated |
| Central Nodes | AI, Projects | **ML, Coding** | Engagement vs. recognition divide |

---

## 🔍 Conclusions

- **Participation ≠ Recognition**: Users actively engage across multiple flairs, but upvotes are concentrated in fewer, specialized domains.  
- **Engagement Bridges:** *AI* and *Projects* foster broad interaction.  
- **Recognition Drivers:** *ML* and *Coding* dominate visibility and influence.  
- **Community Segmentation:** Upvote-based communities are more distinct, reinforcing a specialization-driven recognition pattern.

---

## 💡 Recommendations

- **Encourage Cross-Flair Interaction:** Combine topics (e.g., “AI in ML Projects”) to connect technical and applied domains.  
- **Highlight Technical Content:** Since ML and Coding attract recognition, promote guides and tutorials in these areas.  
- **Monitor Upvote Concentration:** Ensure balanced visibility and prevent dominance by niche subgroups.  
- **Use Projects Flair Strategically:** Leverage it as a bridge for interdisciplinary discussion.

---


