# Shared Architecture Overview: The Disagreement Signature

## Conceptual Methodology

In traditional machine learning ensembles, multiple models (agents) process data, and their outputs are combined via voting, averaging, or stacking to produce a final prediction. While this reduces variance, it often fails in adversarial environments where novel attacks or regime shifts cause all supervised models to confidently make the wrong prediction (False Negatives).

Our architecture introduces a structural paradigm shift: treating the **variance between agents** as a primary feature itself. 

### 1. Heterogeneous Agents
We deploy multiple primary agents designed to be fundamentally heterogeneous. Instead of training multiple similar models on the same data, each agent maps a distinct geometric or temporal property of the environment. For example:
* **Agent A** maps smooth, long-term historical structural relationships.
* **Agent B** maps fast-paced, short-term sequential actions.

### 2. The Disagreement Signature
Because the agents are tracking different data manifolds, their probability outputs will naturally diverge during complex, out-of-distribution events. We calculate the statistical divergence between these predictions, known as the **Disagreement Signature**.

### 3. The Unsupervised Override (Circuit Breaker)
If the primary agents both predict a "safe" or "negative" state, but their Disagreement Signature spikes significantly above a historical baseline, the system flags an uncertainty event. This spike is evaluated by a final, completely unsupervised layer trained exclusively on normal behavior. 

If both the disagreement is high and the unsupervised energy breaches its threshold, the system fires a "Circuit Breaker" override. This catches novel, unseen anomalies that successfully bypassed the supervised agents, acting as a highly calibrated safety net.
