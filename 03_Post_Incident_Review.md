# Post-Incident Review (PIR) & Root Cause Analysis

**Incident ID:** INC-2026-002
**Date:** 14 November 2026
**Author:** Piyush Gahlawat (IT Operations Manager)

## 1. Incident Summary
On 14 Nov 2026, NovaCorp suffered a ransomware attack via a phishing email. The attack encrypted the customer database and took the core banking portal offline for 6 hours. 

## 2. Root Cause Analysis (The 5 Whys)
1. **Why was the portal offline?** Because the web servers were encrypted by ransomware.
2. **Why were they encrypted?** Because an employee downloaded a malicious attachment.
3. **Why did the attachment execute?** Because the endpoint lacked modern EDR (Endpoint Detection and Response) blocking capabilities.
4. **Why did it spread to the database?** Because the database and web server shared the same network subnet (flat network architecture).
5. **Root Cause:** Inadequate network segmentation and a lack of next-generation endpoint protection.

## 3. What Went Well
- The backup restoration process worked, even though it was slower than the RTO.
- The Incident Commander successfully coordinated Legal and Communications within the first 30 minutes.

## 4. Areas for Improvement
- **Network Segmentation:** The DB and Web servers must be separated into different VLANs.
- **Backup Speed:** We need to move from tape backups to hot-site replication to meet the 1-hour RPO.
- **Phishing Training:** The employee who clicked the link had not completed security awareness training in 14 months.