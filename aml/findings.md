# Anti-Money Laundering (AML): Findings

## Dataset
We utilized the **Elliptic Transaction Dataset**. This is the industry-standard benchmark for financial crime on blockchain/ledger networks. It maps a massive graph of real-world transactions, explicitly labeling nodes as licit or illicit. We chose this dataset because its highly obfuscated, graph-based laundering topologies provide a rigorous test for any transaction monitoring system.

## Experimental Setup
We deployed the **three-agent ensemble with disagreement-based override**. The architecture consisted of dual-stream supervised agents evaluating local transaction features and extended neighborhood graph structures, coupled with an unsupervised topological circuit breaker mapping the manifold of normal banking behaviors.

## Key Qualitative Findings

### Curing Alert Fatigue
Legacy AML systems rely heavily on rigid rulesets, resulting in massive False Positive Rates that overwhelm compliance teams. Our testing proved that the Disagreement Ensemble drastically reduces this noise. Because the unsupervised override layer only fires when there is both structural anomaly *and* high disagreement between the primary agents, it acts as an incredibly strict filter.

### Unsupervised Detection of Novel Typologies
The system successfully identified advanced laundering networks without ever being trained on them. By training the final layer exclusively on legitimate transactions, the system flagged illicit flows purely based on their geometric deviation from normal banking behavior, proving the efficacy of the unsupervised calibration theorem in financial compliance.
