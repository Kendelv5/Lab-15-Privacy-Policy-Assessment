# 📄 GRC Lab: Privacy Policy Risk & Compliance Assessments

## 🎯 Executive Summary
This project evaluates the public-facing privacy policies of two distinct organizations to identify compliance gaps, regulatory exposure, and inherent operational risks. The analysis maps policy language against major regulatory frameworks, including **GLBA, TCPA, CCPA/CPRA, GDPR, and PDPO**, demonstrating practical application of Governance, Risk, and Compliance (GRC) methodologies.

## 🛠️ Methodology
Each policy was evaluated using a standard 5-step GRC workflow:
1. **Scope & Regulatory Mapping:** Identifying applicable legal frameworks based on geography and industry.
2. **Data Inventory & Classification:** Evaluating how clearly collected data is categorized.
3. **Third-Party & Vendor Management Review:** Assessing data-sharing protocols and processor requirements.
4. **Consent & Data Subject Rights (DSR) Evaluation:** Verifying mechanisms for opt-outs, deletion, and access.
5. **Security Safeguards Review:** Checking for documented technical and administrative controls.

---

## 🏢 Assessment 1: Veracity Insurance Solutions
**Sector:** Insurance & Financial Services  
**Compliance Rating:** 🔴 2.5 / 5 (Needs Immediate Remediation)  

### 🚩 Key Risk Findings
* **Critical Risk (TCPA Violation):** The SMS consent clause explicitly lists an entirely different entity ("Insurance Canopy") rather than Veracity. This copy-paste error invalidates the consent, exposing the company to massive per-text regulatory fines under the Telephone Consumer Protection Act.
* **High Risk (CCPA Non-Compliance):** The policy actively acknowledges the use of Facebook Pixel and Google AdWords for retargeting, yet completely omits US state privacy rights. It lacks the legally mandated "Do Not Sell or Share My Personal Information" opt-out mechanism for California residents.
* **Medium Risk (GLBA Ambiguity):** Fails to provide a direct internal opt-out for sharing Non-Public Information (NPI) with third-party marketers, instead relying on external ad-network links.
* **Low Risk (Vague Classification):** Uses blanket terms for data collection without defining specific categories of PII or NPI, violating modern data transparency standards.

---

## 🌍 Assessment 2: G2A Capital Group
**Sector:** Global Digital Marketplace  
**Compliance Rating:** 🟢 4.5 / 5 (Mature, with Inherent Risks)  

### 🛡️ Maturity Highlights
* **Strong TPRM:** Mandates external processors sign Data Processing Agreements (DPAs), undergo SOC 2 / ISO 27001 audits, and adhere to a strict 24-hour breach notification SLA.
* **Explicit Cryptographic Standards:** Clearly documents the use of AES-256 for data at rest, TLS/SSL for data in transit, and bcrypt/PBKDF2 for password hashing.
* **Accurate Regulatory Mapping:** Successfully delegates Data Controllers based on precise global jurisdictions (US, EU, Hong Kong) and anticipates upcoming CPRA amendments.

### ⚠️ Inherent & Residual Risks
* **High Risk (Peer-to-Peer Data Transfer):** To execute sales, buyer PII is shared directly with independent, unvetted third-party sellers. Because sellers act as independent controllers, G2A loses technical oversight of how that data is stored or protected downstream.
* **Medium Risk (Unstructured AI Data Retention):** Customer support logs involving AI chatbots (Stanley Bot) are retained for 6 years. Despite warnings not to input sensitive data, the lack of automated Data Loss Prevention (DLP) scrubbers creates a risk of storing highly regulated, special-category PII in unstructured logs.
* **Medium Risk (Cross-Border Data Transfers):** Acknowledges that EU data processed on US cloud infrastructure is subject to the US CLOUD Act, creating ongoing scrutiny under EU Schrems II rulings despite the use of Standard Contractual Clauses (SCCs).
