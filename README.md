# Intent Mapping for Risk Detection

---

## 🔐 Data Privacy Note

- All examples in this repository are **fully abstracted**.
- No real customer data, identifiers, or sensitive attributes are included.
- **This repository focuses exclusively on the methodology and thinking framework, not proprietary data.**

---

## ✅ Objective
This project demonstrates a **structured methodology** for converting raw transactional behaviour into:
- Fraud intent understanding
- Modus Operandi (MO) decomposition
- Actionable, controllable detection rules

The framework was developed in a fintech risk environment to help analysts move from **manual case reviews** to **repeatable hypothesis-driven rule creation**, without relying on sensitive data exposure.

---

## Problem Context
Fraud and mule accounts often evolve in **phases**:
- Dormancy
- Testing
- Cool-off
- Pilot runs
- Full-scale execution

Traditional rule systems detect isolated anomalies but fail to capture **behavioural progression over time**.  
This framework addresses that gap by focusing on **intent, sequence, and change in behaviour**, rather than single events.

---

## Framework Overview (4 Layers)

### 1️⃣ Case Review Abstraction
- Start with reviewed fraud accounts (data abstracted)
- Focus on **what changed** vs historical behavior
- Ignore absolute values; prioritize **patterns and transitions**

---

### 2️⃣ Raw Behaviour Decomposition
Break transactions into **primitive behavioral events**, such as:
- Dormancy breaks
- Burst credits
- Self FIFO loops
- ATM proxy cash-outs
- Unknown P2P inflows
- Device / SIM changes

At this stage, transactions are reduced to **behavioural signals**, not financial details.

---

### 3️⃣ Intent Mapping
Behavioral signals are grouped into **phases** to form an **Intent Map**.

Each phase answers:
- What was the likely intent?
- Was this testing, scaling, evasion, or execution?
- What is the next expected action?

This converts raw timelines into a **story of account behaviour**.

---

### 4️⃣ Rule & Hypothesis Creation
Each completed intent map produces:
- 1–2 detection hypotheses
- A structured rule definition:
  - Objective
  - Key flags (2–4)
  - Logic (relative, not static thresholds)
  - Expected detection behaviour
- Controllability assessment (false positives vs coverage)

This ensures every case review leads to **system-level learning**.

---

## 🧩 Key Concepts Used
- Intent-driven analysis (not anomaly-only)
- Phase-based behavior modeling
- Relative thresholds over static limits
- Human-in-the-loop risk design
- Precision-focused fraud detection

---

## Outcome & Impact
- Standardised how analysts convert cases into rules
- Reduced subjectivity in manual reviews
- Enabled weekly hypothesis generation as a formal process
- Improved detection precision by combining:
  - Inactivity + burst
  - FIFO + device change
  - Behaviour sequencing over time

## Why This Matters
This project demonstrates:
- How to think like a fraudster
- How to translate investigations into prevention
- How to design explainable, regulator-safe rules
- How to scale fraud learning across teams

This framework applies to:
- Fraud detection
- AML monitoring
- Trust & Safety systems
- Risk decision engines
