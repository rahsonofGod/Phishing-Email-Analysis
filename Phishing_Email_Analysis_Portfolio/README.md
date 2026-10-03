# Phishing Email Analysis & Incident Response Lab

## Overview
This portfolio project demonstrates an end-to-end SOC investigation of a **simulated phishing email**. It covers initial triage, email-header authentication, sender/domain and URL analysis, attachment triage, IOC extraction, MITRE ATT&CK mapping, verdict/severity, and response recommendations.

**Safety:** All publishable indicators in the evidence files use reserved documentation domains/IP space. The walkthrough artwork is illustrative; treat its displayed reputation counts/details as visual examples, not live threat-intelligence findings.

## Scenario
A user reports an urgent email impersonating Microsoft Account Support. The message asks the recipient to verify their account and includes an unexpected ZIP attachment. As the SOC analyst, you determine whether the message is malicious and document the evidence and response.

## Investigation Workflow
1. Initial email triage
2. Header analysis: From, Reply-To, Return-Path, Received, Message-ID
3. SPF/DKIM/DMARC review
4. Sender/domain analysis
5. URL analysis without directly visiting the destination
6. Attachment triage and hashing in an isolated environment
7. IOC extraction
8. MITRE ATT&CK mapping
9. Verdict and severity
10. Containment and remediation

## Key Findings
- Brand impersonation and look-alike spelling
- Urgency designed to pressure the recipient
- Simulated SPF, DKIM and DMARC failures
- Credential-verification lure
- Unexpected archive attachment
- Multiple indicators suitable for SIEM/email-gateway hunting

## Verdict
**Malicious (simulated) - High severity.**

Rationale: the scenario combines impersonation, failed authentication, a credential-phishing lure and an unexpected attachment. Severity is a lab assessment, not a live production incident rating.

## Recommended Response
- Quarantine/remove the message from mailboxes.
- Search mail telemetry for matching sender/domain/subject/URL indicators.
- Block confirmed malicious indicators at appropriate controls.
- Determine whether recipients clicked the link or opened the attachment.
- Reset credentials and revoke sessions if account compromise is confirmed.
- Investigate endpoints if execution is suspected or confirmed.
- Document the incident and tune detections.

## Repository Structure
- `email_sample/` - safe simulated raw email
- `screenshots/` - visual walkthrough
- `IOC/` - IOC CSV
- `mitre/` - ATT&CK mapping
- `report/` - professional SOC investigation report

## Skills Demonstrated
Email security • phishing analysis • header analysis • SPF/DKIM/DMARC • IOC extraction • threat-intelligence workflow • MITRE ATT&CK • incident response • SOC reporting

## CV Summary
Conducted an end-to-end simulated phishing investigation, analysing email headers and authentication results, extracting IOCs, triaging suspicious URLs/attachments, mapping activity to MITRE ATT&CK, and producing containment/remediation recommendations and a professional SOC report.
