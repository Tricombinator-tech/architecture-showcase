# Multi-Agent Heterogeneous Ensembles for AML & Financial Crime Detection

## Executive Overview
This repository documents the research methodologies, benchmark performance, and architectural paradigms of our proprietary, multi-agent predictive framework. This architecture was developed and tested across multiple domains, with this repository focusing on its application to the dual problems of alert fatigue and evasion vulnerability in transaction monitoring.

Rather than relying on homogenous models or simple rule-based ensembles, our approach leverages a **heterogeneous multi-agent system** that derives an explicit uncertainty metric from agent disagreement. This "disagreement signature" acts as an automated, real-time circuit breaker to protect operational efficiency and capture sophisticated laundering typologies.

---

## Validated Domain & Core Benchmarks

### Anti-Money Laundering (AML) & Transaction Monitoring
* **Benchmark Dataset:** Elliptic Transaction Graph Dataset (Strict Out-of-Sample Split)
* **Core Result:** On out-of-sample Elliptic data, the architecture's override layer achieved a 1.87% false positive rate and 50.92% precision, flagging 27.98% of illicit transactions missed by primary detection, functioning as a low-noise second-pass layer. The ~98% relative reduction in false-positive volume reflects this override layer's own alert efficiency, not overall system recall.

---

## Repository Purpose & Deployment Infrastructure
This repository functions strictly as a public documentation portal for our quantitative research findings. To protect our underlying intellectual property and trade secrets, the production source code, model weights, and hyperparameter configurations remain classified.

This repository documents research findings and methodology. Source code, model internals, and tuning details are not published here. We're open to discussing proof-of-concept collaborations, blinded benchmark tests on partner data, or licensing discussions.

For live proof-of-concept testing, blinded dataset stress-tests, or licensing inquiries, please contact our core team directly.

**Contact:** business@tricombinator.com | tricombinator.com
