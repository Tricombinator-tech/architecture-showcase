# Multi-Agent Heterogeneous Ensembles for AML & Financial Crime Detection

## Executive Overview
This repository documents the research methodologies, benchmark performance, and architectural paradigms of our proprietary, multi-agent predictive framework. Designed for high-consequence enterprise banking environments, the system focuses heavily on solving the dual crises of **alert fatigue** (excessive false positives) and **evasion vulnerability** (undetected structurally masked flows) in transaction monitoring.

Rather than relying on homogenous models or simple rule-based ensembles, our approach leverages a **heterogeneous multi-agent system** that derives an explicit uncertainty metric from agent disagreement. This "disagreement signature" acts as an automated, real-time circuit breaker to protect operational efficiency and capture sophisticated laundering typologies.

---

## Validated Domain & Core Benchmarks

### Anti-Money Laundering (AML) & Transaction Monitoring
* **Benchmark Dataset:** Elliptic Transaction Graph Dataset (Strict Out-of-Sample Split)
* **Core Breakthrough:** Suppressed the False Positive Rate (FPR) to a definitive **1.87%**, unlocking a **~98% reduction** in manual compliance review overhead.

---

## Repository Purpose & Deployment Infrastructure
This repository functions strictly as a public documentation portal for our quantitative research findings. To protect our underlying intellectual property and trade secrets, the production source code, model weights, and hyperparameter configurations remain classified.

The complete framework is fully operational and packaged as a plug-and-play middleware API engineered to sit on top of core ledger systems. It can be deployed via:
1. **Secure Hosted API (SaaS):** Data is streamed to an isolated, GDPR-compliant EU cloud instance for real-time scoring.
2. **Encrypted On-Premise Containers:** Compiled, obfuscated binaries (Docker) deployed directly onto client infrastructure, ensuring zero data leakage.

For live proof-of-concept testing, blinded dataset stress-tests, or licensing inquiries, please contact our core team directly.

**Contact:** business@tricombinator.com | tricombinator.com
