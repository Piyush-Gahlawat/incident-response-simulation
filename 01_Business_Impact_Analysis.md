# Business Impact Analysis (BIA) & Recovery Objectives

*During a crisis, IT Operations must prioritize restoration based on business impact. This document defines the Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO) for NovaCorp's critical assets.*

## Asset Priority Matrix

| System / Asset | Business Function | Impact of Downtime | **RTO** (Max time offline) | **RPO** (Max data loss) | Priority Tier |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Core Banking Portal** | Customer transactions | Severe (Revenue loss, reputational damage) | **2 Hours** | **15 Minutes** | **P1 (Critical)** |
| **Customer Database** | Identity verification | Severe (Regulatory breach, fraud risk) | **4 Hours** | **1 Hour** | **P1 (Critical)** |
| **Email Exchange** | Internal comms | High (Stalled operations) | **8 Hours** | **4 Hours** | **P2 (High)** |
| **HR / Payroll System** | Employee salaries | Low (Can be delayed) | **48 Hours** | **24 Hours** | **P3 (Medium)** |

## 🔴 The Crisis Point
*At 16:00 UTC, the Incident Commander (IT Ops Manager) discovers that the backup restoration for the Customer Database is taking longer than expected. The RTO is 4 hours, but the restoration will take 6 hours.*

**Decision Required:** Do we restore an older, 24-hour-old backup (breaching RPO by 23 hours), or wait 6 hours for the latest backup (breaching RTO by 2 hours)? 
*(Note: In this scenario, the Incident Commander decides to restore the 24-hour-old backup to get the business back online, and manually reconciles the lost transactions via the payment gateway API).*