# Phishing Email Analysis — VitalCare Health Solutions (September 2025)

This repository contains the executive report and artifacts from a phishing email investigation for **VitalCare Health Solutions**, a healthcare provider supporting 500+ hospitals.

## Overview
A deceptive email impersonated VitalCare’s security team and urged recipients to “verify” credentials within 24 hours. Authentication checks (**SPF, DKIM, DMARC**) failed. The message contained a malicious URL and an executable attachment designed for credential theft and potential malware delivery. **Severity: High** due to account compromise risk, HIPAA exposure, service disruption, and reputational damage.  
*Source: Executive report included in this repo.* 

## Objectives & Scope
- Give leadership a clear, non-technical summary of the incident and risk.
- Analyze headers (SPF/DKIM/DMARC), body content, attachments, and embedded URLs/domains.

## Methodology
- Header review → spoofing confirmed  
- IOC analysis → malicious URL/IPs + `Invoice_12345.exe`  
- Passive lookups (WHOIS/infra) → masked ownership and suspect infra likely spun up to bypass defenses

## Key Findings
- **Impersonation & urgency** tactics  
- **Mail auth failures** (SPF/DKIM/DMARC)  
- **Malicious infrastructure** (URL/IPs) and **.exe attachment**

## Impact Assessment
- Credential theft → potential lateral movement  
- Malware risk  
- Possible HIPAA non-compliance and operational disruption  
- Reputational harm

## Mitigation & Recommendations
- Block associated domain(s) and hash across email/network/endpoint
- Quarantine email copies; notify staff and reinforce phishing awareness
- Enforce DMARC “reject”; run regular phishing simulations
- Tighten email filters to flag executables
- Share threat intelligence with industry partners

## Repo Structure
- `Executive Report for Phishing Email Analysis.pdf` — full executive report
- `images/` — optional screenshots (headers, IOC lookups, etc.)
- `README.md` — this document

---

**Let’s connect:**  
LinkedIn: https://www.linkedin.com/in/kiridi-david/  
Tags: #Amdari #10Alytics #CyberSecurity #Phishing #IncidentResponse #EmailSecurity
