# **DoD Impact Levels (IL) Compliance Guide**

## **Purpose**
This document provides an overview of the **Department of Defense (DoD) Impact Levels (IL)**, outlining security requirements, classification criteria, and compliance considerations for cloud service providers (CSPs) operating in **DoD and FedRAMP environments**. It aligns with **NIST 800-53, CMMC, and Zero Trust security frameworks**.

---

## **What are DoD Impact Levels?**
DoD Impact Levels categorize the **sensitivity of government data** hosted in commercial cloud environments. They define the **security controls, encryption, and access requirements** necessary to protect **DoD mission-critical workloads**.

### **DoD Impact Levels Overview**
| **Impact Level** | **Data Classification** | **Security Requirements** |
|-----------------|----------------------|-------------------------|
| **IL2 (Public Data)** | Non-Controlled Unclassified Information (CUI), Public DoD Information | FedRAMP Moderate, Basic Security Controls |
| **IL4 (Controlled CUI)** | CUI, Mission-Critical DoD Data | FedRAMP Moderate + DoD-specific security requirements |
| **IL5 (National Security CUI)** | Higher sensitivity CUI, Mission-Critical Operations | FedRAMP High + DoD IL5-specific controls |
| **IL6 (Classified Data)** | Secret & Top Secret DoD Information | DoD-approved air-gapped classified cloud environments |

---

## **DoD Impact Level Security Controls**
Each **IL level** requires compliance with **specific security, access control, and encryption policies**:

### **1. Identity & Access Management (IAM)**
✅ **IL4+ requires CAC/PIV authentication & RBAC/ABAC**.
✅ **IL5+ mandates Zero Trust enforcement & Just-In-Time (JIT) access**.
✅ **IL6 enforces air-gapped authentication & classified personnel clearance**.

### **2. Data Security & Encryption**
✅ **FIPS 140-2/140-3 encryption required for IL4+ data-at-rest & in-transit**.
✅ **IL5+ mandates key management in DoD-controlled HSMs (AWS KMS, Azure Key Vault)**.
✅ **IL6 enforces NSA-approved cryptographic solutions for classified workloads**.

### **3. Network Security & Segmentation**
✅ **IL4 requires DoD-mandated cloud connectivity (DISA Cloud Access Points - CAPs)**.
✅ **IL5 mandates enclave-based security models & microsegmentation**.
✅ **IL6 operates in air-gapped, DoD-classified environments**.

### **4. Secure DevSecOps & Compliance Automation**
✅ **IL4+ requires compliance automation (AWS Config, Azure Policy, OpenSCAP)**.
✅ **IL5 mandates continuous monitoring & security audits (SIEM, SOAR, STIGs)**.
✅ **IL6 enforces classified development environments & strict CI/CD security policies**.

---

## **Mapping DoD Impact Levels to Cloud Security Frameworks**
| **Security Framework** | **IL4** | **IL5** | **IL6** |
|---------------------|------|------|------|
| **FedRAMP Baseline** | Moderate | High | Classified |
| **NIST 800-53 Rev 5** | Yes | Yes | Yes |
| **Zero Trust Model** | Yes | Yes | Yes |
| **CMMC Compliance** | Level 2+ | Level 3 | N/A |
| **Encryption (FIPS 140-2/140-3)** | Required | Required | NSA-Approved |
| **Access Control (CAC/PIV, MFA, RBAC/ABAC)** | Required | Required | Air-Gapped |

---

## **Tools & Technologies for DoD IL Compliance**
| **Category** | **Tools & Solutions** |
|-------------|-----------------------|
| **IAM & Access Control** | AWS IAM, Azure AD, Okta, Ping Identity, CAC/PIV Authentication |
| **Encryption & Key Management** | AWS KMS, Azure Key Vault, Google Cloud KMS, HashiCorp Vault |
| **SIEM & Continuous Monitoring** | Splunk, Azure Sentinel, Chronicle, AWS Security Hub |
| **DevSecOps & Compliance Automation** | Terraform, Ansible, AWS Config, Azure Policy, OpenSCAP |
| **Threat Detection & Response** | AWS GuardDuty, Azure Defender, CrowdStrike, MITRE ATT&CK |

---

## **Next Steps**
1. **Develop a DoD IL Compliance Roadmap** – Identify security gaps & remediation strategies.
2. **Automate Compliance & Risk Management** – Implement **security-as-code & automated monitoring**.
3. **Enhance Cloud Security Posture** – Enforce **Zero Trust & AI-driven threat intelligence**.
4. **Achieve IL4+ and DoD Readiness** – Map IL4+ controls to **FedRAMP, NIST 800-171, and CMMC Level 3+**.
