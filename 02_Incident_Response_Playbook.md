# Incident Response Playbook (NIST SP 800-61)

*This playbook follows the NIST Incident Response Lifecycle to contain the ransomware attack and restore operations.*

## Phase 1: Preparation & Detection
- [ ] Alert triggered by monitoring (Portal offline).
- [ ] Incident Commander (IT Manager) assigned.
- [ ] War Room (Bridge Call) established with Legal, HR, and Communications.

## Phase 2: Containment
- [ ] **Isolate the network:** Disconnect the primary data center from the internet to prevent lateral movement.
- [ ] **Disable compromised accounts:** Revoke access for the employee whose account was phished.
- [ ] **Preserve evidence:** Snapshot the infected servers before wiping them.

## Phase 3: Eradication & Recovery
- [ ] Identify the ransomware strain and check for decryptors (e.g., No More Ransom Project).
- [ ] Rebuild infected servers from a known good state.
- [ ] Restore the Customer Database from backups (Priority P1).
- [ ] Restore the Core Banking Portal (Priority P1).

## Phase 4: Post-Incident Activity
- [ ] Conduct a Root Cause Analysis (RCA).
- [ ] Update the Business Continuity Plan based on lessons learned.
- [ ] Notify affected customers and regulators (if PII was exfiltrated).