# Incident Response & Business Continuity Simulation

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Framework: NIST SP 800-61](https://img.shields.io/badge/Framework-NIST%20SP%20800--61-blue.svg)](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)
[![Domain: IT Operations](https://img.shields.io/badge/Domain-IT%20Operations-success.svg)]()

A comprehensive, tabletop Incident Response (IR) and Business Continuity Plan (BCP) simulation based on a ransomware attack scenario. 

This repository demonstrates the operational steps, recovery metrics (RTO/RPO), and post-incident analysis required to manage a severe enterprise cyber-attack. It serves as a practical portfolio artifact for IT Operations and GRC roles, showing how to translate theoretical frameworks into actionable, crisis-ready documentation.

## 📖 The Scenario: Project NovaCorp

**Company:** NovaCorp (Fictional FinTech managing 50,000 active users)
**Date:** Thursday, 14:00 UTC
**Attack Vector:** A phishing email bypassed the spam filter. An employee downloaded a malicious attachment, allowing threat actors to deploy ransomware across the primary data center.

**Current Impact:**
- Core banking web portal is offline.
- Customer database is encrypted.
- Backups are intact, but the restoration process has never been tested.

**The Goal:**
Execute the Incident Response Playbook, calculate the financial and operational impact, restore services within the agreed **RTO (Recovery Time Objective)**, and document the **Root Cause Analysis (RCA)**.

## 📂 Repository Structure

The simulation is broken down into four distinct phases, mirroring the NIST Incident Response Lifecycle.

| File | Description |
| :--- | :--- |
| **[00_Scenario_Overview.md](./00_Scenario_Overview.md)** | Sets the stage, defines the fictional company, the attack vector, and the initial crisis state. |
| **[01_Business_Impact_Analysis.md](./01_Business_Impact_Analysis.md)** | Defines the **RTO** and **RPO** for critical assets. Includes the "Crisis Point" decision matrix. |
| **[02_Incident_Response_Playbook.md](./02_Incident_Response_Playbook.md)** | A step-by-step NIST-aligned playbook covering Detection, Containment, Eradication, and Recovery. |
| **[03_Post_Incident_Review.md](./03_Post_Incident_Review.md)** | A formal Root Cause Analysis (RCA) using the "5 Whys" methodology, plus a plan for corrective actions. |

## 🔑 Key Concepts Demonstrated

### 1. RTO vs. RPO
- **RTO (Recovery Time Objective):** The maximum acceptable time that a system can be offline. In this simulation, the Core Banking Portal has an RTO of **2 hours**.
- **RPO (Recovery Point Objective):** The maximum acceptable amount of data loss measured in time. The Core Banking Portal has an RPO of **15 minutes**.

### 2. The "Crisis Point" Decision
At 16:00 UTC, the Incident Commander discovers that the backup restoration for the Customer Database will take **6 hours**, exceeding its **4-hour RTO**. The team must decide: restore an older backup (breaching RPO) or wait for the latest backup (breaching RTO). This tests high-pressure decision-making and trade-off analysis.

### 3. Root Cause Analysis (The 5 Whys)
The Post-Incident Review uses the "5 Whys" technique to move beyond the immediate trigger (phishing) and identify systemic failures, such as a **flat network architecture** and a lack of **EDR (Endpoint Detection and Response)**.

## 🚀 How to Use This Repository

1. **Read the Overview:** Start with `00_Scenario_Overview.md` to understand the context.
2. **Review the BIA:** Look at `01_Business_Impact_Analysis.md` to see how recovery priorities are set.
3. **Walk the Playbook:** Follow `02_Incident_Response_Playbook.md` to see the operational steps.
4. **Analyze the RCA:** Finally, read `03_Post_Incident_Review.md` to see how the organization learns from the failure.

## 🎯 Target Audience & Purpose

- **IT Managers & SysAdmins:** Looking for a template to build their own Incident Response plans.
- **GRC Analysts:** Needing a practical example of Business Continuity and Disaster Recovery (BCP/DR) documentation.
- **Hiring Managers:** Reviewing this repository as evidence of practical IT Operations, risk assessment, and crisis management skills.

## 📝 License & Disclaimer

This project is shared for educational and portfolio purposes under the **CC BY 4.0** license.

**Disclaimer:** This is a simulation based on a fictional scenario. It is a tabletop exercise designed to demonstrate process design and analytical thinking. It is not legal advice and does not represent a real company's operations.