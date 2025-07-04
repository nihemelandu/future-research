## 📦 Research Plan: Causal Dynamics Between Customer Behavior and Supply Chain Operations

### 🧭 Overview

This research aims to investigate the **bidirectional relationship** between algorithmic customer interactions and supply chain operations. Specifically, it explores how **digital experiences and demand signals** influence procurement, inventory, and fulfillment—and how those operational realities, in turn, shape **customer experience and satisfaction**.

The end goal is to improve **decision quality** and **operational efficiency** in complex, dynamic supply chain environments using robust causal reasoning and system modeling.

---

### 🎯 Research Objectives

- Determine whether changes in customer behavior **cause** operational impacts, or are merely correlated.
- Evaluate whether improvements in supply chain performance **lead to** measurable gains in customer satisfaction or loyalty.
- Model and simulate feedback loops between demand-side behaviors and supply-side constraints.
- Inform **intervention design** that aligns customer-facing decisions with operational capabilities.

---

### 🧩 Research Scope

#### 🔍 Domain Focus

To make this work tractable and actionable, the research will focus on a well-defined domain:

- **Industry selection**: Retail, e-commerce, or manufacturing (TBD)
- **Customer behavior metrics**:
  - Purchasing patterns
  - Complaint or return rates
  - Channel preferences
  - Conversion & churn
- **Operational performance metrics**:
  - Inventory turnover
  - Fulfillment accuracy
  - Delivery time & reliability
  - Flexibility and cost efficiency
- **Significance threshold**:  
  Not all statistically significant effects are **operationally meaningful**—this research will prioritize interventions with **practical impact**.

---

### 🛠️ Methodology

To address the causal questions at the heart of this work, a hybrid approach will be employed, drawing from structural models, quasi-experiments, causal machine learning, and simulation.

---

#### 🧠 1. Structural Causal Models (SCM)

SCMs will serve as the **core reasoning framework** for this research:

- **Causal DAGs (Directed Acyclic Graphs)** to explicitly express assumptions
- **Structural Equations** to model data-generating processes
- **do-Calculus** to derive valid interventional estimands
- **Identification analysis**: Determine whether effects of interest can be identified from available data
- **Toolkits**: [`DoWhy`](https://github.com/py-why/dowhy), [`DAGitty`](http://www.dagitty.net/), `causalgraphicalmodels`, `Ananke`

SCMs provide conceptual rigor and clarity in defining what can (and cannot) be learned from observational data.

---

#### 🧪 2. Quasi-Experimental Designs

To estimate causal effects from historical or operational data without randomization:

- **Interrupted Time Series (ITS)**
- **Synthetic Control Methods**
- **Stepped-Wedge Rollout Designs**
- **Panel Event Study Designs**
- **Difference-in-Differences (DiD)**
- **Regression Discontinuity / Kink Designs**
- **Propensity Score Matching / Weighting**

These methods leverage **natural experiments, system rollouts, shocks, or thresholds**—common in supply chain and digital environments.

---

#### 🤖 3. Causal Machine Learning

To handle high-dimensional data, discover treatment heterogeneity, and support complex modeling:

- **Causal Forests** (e.g., Generalized Random Forests)
- **Double Machine Learning (DML)**
- **Meta-learners**: S-learner, T-learner, X-learner
- **Uplift Modeling** for individual-level intervention targeting

**Toolkits**: `EconML`, `CausalML`, `scikit-uplift`, `DoWhy + sklearn`

These methods enable estimation at **scale**, with interpretability and flexibility.

---

#### 🧪 4. Simulation Modeling

Simulation will be used to model dynamics that are hard to capture empirically:

- **System Dynamics Models**: Capture stock-flow relationships and feedback loops (e.g., inventory → lead times → customer abandonment)
- **Agent-Based Models (ABM)**: Represent decision-making by individual customers, suppliers, or fulfillment centers
- **Scenario Testing**: Examine the effects of hypothetical interventions (e.g., algorithmic changes or new delivery policies)

Simulation allows us to **stress-test** causally-informed strategies in synthetic but realistic environments.

---

### 📏 Evaluation Strategy

#### 🔬 Simulation Validation

- **Historical backtesting**: Compare simulation outcomes to observed behavior
- **Face validity**: Are dynamics reasonable to domain experts?
- **Sensitivity analysis**: Explore robustness of outcomes to model assumptions

#### 📈 Empirical Evaluation

- **Causal identification**: Are estimated effects statistically and practically valid?
- **Operational interpretability**: Do findings align with stakeholder understanding?
- **Counterfactual testing**: Can the models answer "what-if" questions reliably?

---

### 🔄 Future Directions

- Model **algorithmic feedback loops**, e.g., recommender systems affecting demand patterns, which then affect fulfillment capabilities.
- Extend to **omnichannel environments** where customer behavior spans physical and digital touchpoints.
- Explore real-time adaptive decision systems combining causal inference with online learning or reinforcement learning.

---
