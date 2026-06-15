# Dynamic Consensus Routing: A Dual-Layer Compliance Architecture

This document outlines the conceptual methodology powering our proprietary Anti-Money Laundering (AML) machine learning system. Designed to meet the stringent explainability and robustness requirements of Model Risk Management (MRM) teams, the architecture resolves the persistent challenge of zero-day evasion while minimizing operational noise.

## The Paradigm: Dynamic Consensus Routing

Legacy compliance engines rely predominantly on monolithic models or static rule-sets, leaving them vulnerable to out-of-distribution events and novel laundering typologies. Our solution pivots to a structural paradigm known as **Dynamic Consensus Routing**. This framework operates across three distinct phases to provide a highly explainable, low-noise safety net.

### Phase 1: Heterogeneous Feature Mapping

The foundation of the architecture relies on the deployment of multiple primary analytical agents. Rather than utilizing homogenous models that evaluate the exact same feature spaces, our agents are intentionally designed to map fundamentally different geometric and temporal aspects of a transaction:

*   **Primary Agent A** evaluates macroscopic transaction flows, establishing a generalized baseline of standard behavioral norms for a given entity.
*   **Primary Agent B** maps microscopic interaction sequences, monitoring immediate, localized transactional velocities independent of long-term history.

By evaluating distinct facets of the data, the primary layer builds a comprehensive and multifaceted initial risk profile.

### Phase 2: Out-of-Distribution Detection

In standard operating conditions, the heterogeneous primary agents will align on a confident assessment of a transaction's legitimacy. However, when the system encounters novel, complex, or out-of-distribution events that defy historical patterns—such as a zero-day obfuscation attempt—the primary agents will naturally fail to align. 

The architecture automatically monitors the state of these assessments. When it detects a breakdown in consensus between the primary agents, it flags the transaction as an out-of-distribution anomaly that requires elevated scrutiny.

### Phase 3: The Unsupervised Circuit Breaker

Once a breakdown in consensus is detected, the anomalous transaction is immediately routed away from the primary supervised layer and sent to a dedicated secondary evaluation layer. 

This secondary layer is completely unsupervised and trained exclusively on the baseline manifold of normal, licit banking behavior. It does not rely on historical labels of illicit activity. If this secondary layer determines that the transaction's behavioral profile deviates significantly from normal baseline behavior, it triggers a **"Circuit Breaker" override**.

## Conclusion

By structuring the compliance engine around Dynamic Consensus Routing, the architecture ensures that novel laundering typologies that successfully bypass standard supervised models are caught by the unsupervised safety net. Crucially, because the Circuit Breaker only fires when consensus breaks down *and* an unsupervised anomaly is detected, it acts as a highly calibrated, low-noise mechanism, protecting the institution from alert fatigue.
