# Cybersecurity: Intrusion Detection Findings

## Dataset
We utilized the **CICIDS2017** dataset. This dataset is widely recognized as a standard benchmark for Network Intrusion Detection Systems (NIDS). It contains benign behavior alongside common attacks (Brute Force, DoS, Web Attacks, Infiltration, Botnet) with realistic background traffic, making it ideal for testing model robustness under complex adversarial conditions.

## Experimental Setup
We tested a **three-agent ensemble with a disagreement-based override**. The primary supervised agents were tasked with identifying known attack vectors based on network flow features, while the secondary override layer monitored the Disagreement Signature to flag novel or obfuscated intrusions.

## Key Qualitative Findings

### The Decorrelation Paradox
Our primary finding in the cybersecurity domain was the observation of the **Decorrelation Paradox**. Traditional ensemble theory suggests that adding more diverse, decorrelated models improves overall system robustness. However, we found that under active evasion (where an attacker slightly modifies their behavior to avoid detection), adding more agents actually *reduced* robustness if their outputs were simply averaged.

Because the models were highly decorrelated, an attacker only needed to successfully trick *one* heavily weighted model to drag the ensemble's average below the detection threshold. 

### The Disagreement Solution
By transitioning from an averaging ensemble to our Disagreement Signature architecture, we reversed this vulnerability. When an attacker successfully evaded one agent but not the other, the resulting spike in the Disagreement Signature immediately triggered the unsupervised override. The architecture effectively turned the attacker's evasion attempt into the exact signal used to catch them.
