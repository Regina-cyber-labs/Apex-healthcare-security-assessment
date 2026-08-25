# Apex Healthcare Solutions — Security Assessment

## TS Academy Cybersecurity Capstone Project | Group 35

**Project Title:** From Vulnerability To Compliance: Securing Legacy Systems
**Organization:** Apex Healthcare Solutions (Simulated Legacy Healthcare Environment)  
**Assessment Environments:** Kioptrix and Metasploitable 2  
**Role:** Team Lead
**Capstone Grade:** 82%

---

##  Project Overview

As part of the TS Academy Cybersecurity Capstone Project, Group 35 conducted a security assessment of a simulated legacy healthcare environment representing **Apex Healthcare Solutions**.

The assessment was performed using two intentionally vulnerable systems, **Kioptrix** and **Metasploitable 2**, to identify weaknesses that could expose the organization to unauthorized access, remote code execution, privilege escalation, service disruption, and potential compromise of sensitive healthcare information.

The project went beyond simply identifying vulnerabilities. Our team assessed the potential likelihood and impact associated with each finding, determined the overall risk, recommended appropriate technical security controls, and developed Governance, Risk, and Compliance (GRC) policies to support the organization's long-term security posture.

The final deliverable was a professional **Security Assessment Report** containing the executive summary, vulnerability findings, risk assessment, recommended security controls, recommended GRC policies, and conclusion.

> **Note:** This project was completed in a controlled laboratory environment using intentionally vulnerable systems for educational and cybersecurity training purposes.

---

## Project Objectives

The primary objective of the assessment was to evaluate the security weaknesses present within the simulated legacy infrastructure and provide practical recommendations for reducing the associated risks.

The project objectives included:

- Identifying vulnerabilities present within the Kioptrix and Metasploitable 2 environments.
- Documenting the affected services and potential attacker goals associated with each vulnerability.
- Assessing the likelihood that each vulnerability could be successfully exploited.
- Evaluating the potential impact of successful exploitation on the organization's systems and information.
- Assigning an overall risk level to each identified vulnerability.
- Recommending security controls that address the underlying causes and potential consequences of the vulnerabilities.
- Developing GRC policies that support access security, authentication, patching, and ongoing vulnerability management.
- Communicating technical findings in a professional report suitable for organizational decision-making.

---

## Scenario: Apex Healthcare Solutions

Apex Healthcare Solutions was used as the simulated organization for this assessment.

Because the organization operates in a healthcare environment, the security of its systems and information is particularly important. A compromise of its infrastructure could affect the confidentiality, integrity, and availability of sensitive information and critical services.

The assessment therefore considered not only the technical nature of each vulnerability, but also the potential organizational consequences of successful exploitation.

Potential consequences considered during the assessment included:

- Unauthorized access to systems and services
- Remote code execution
- Root-level or administrative access
- Privilege escalation
- Disclosure or compromise of sensitive healthcare information
- Modification or deletion of critical system files
- Service interruption
- Installation of malicious software
- Lateral movement across the network
- Disruption of organizational operations

---

# Assessment Scope

The assessment focused on two intentionally vulnerable environments used during the cybersecurity training:

### 1. Kioptrix

The Kioptrix environment contained vulnerable services that allowed the team to investigate weaknesses associated with legacy Samba, Apache/mod_ssl, and OpenSSH services.

The following three vulnerabilities were identified:

- **Samba trans2open Buffer Overflow**
- **Apache mod_ssl OpenSSL Buffer Overflow**
- **OpenSSH Authentication Overflow**

### 2. Metasploitable 2

Metasploitable 2 provided additional vulnerable services and outdated software for assessment.

The following three vulnerabilities were identified:

- **OpenSSH 4.7p1**
- **Apache HTTP Server 2.2.8**
- **VSFTPD 2.3.4 Backdoor Vulnerability (CVE-2011-2523)**

A total of **six vulnerabilities** were documented across the two assessment environments.

---

# Assessment Approach

The project followed a structured security assessment approach that moved from vulnerability identification to risk evaluation and security recommendations.

### Vulnerability Identification

The team examined the vulnerable environments and documented security weaknesses associated with exposed services and legacy software.

### Vulnerability Analysis

Each finding was reviewed to understand:

- The affected service
- The nature of the vulnerability
- The potential attacker goal
- The potential consequences of successful exploitation

### Risk Assessment

The identified vulnerabilities were evaluated according to:

- **Likelihood** — the probability that the vulnerability could be successfully exploited.
- **Impact** — the potential consequences to the organization's systems, information, and operations.
- **Overall Risk** — the resulting level of risk based on the assessed likelihood and impact.

The assessment used Medium and High likelihood classifications where appropriate. Although the likelihood differed between findings, the final assessment identified significant potential impacts across the vulnerabilities.

### Security Controls

Controls were recommended based on the causes and potential consequences of each vulnerability.

The recommendations included measures such as:

- Security patching and software upgrades
- Access restrictions
- Least privilege
- Network segmentation
- Firewall restrictions
- Multi-Factor Authentication where appropriate
- Vulnerability scanning
- Security monitoring
- Removal or disabling of unnecessary services

### GRC Policies

Four policies were developed to provide an organizational framework for managing the identified risks:

1. Access Control Policy
2. Password Policy
3. Patch Management Policy
4. Vulnerability Management Policy

---

# Vulnerability Findings

The assessment identified six vulnerabilities across Kioptrix and Metasploitable 2.

## Kioptrix Vulnerabilities

### 1. Samba trans2open Buffer Overflow

**Affected Service:** Samba smbd  
**Port:** 139

The Samba trans2open Buffer Overflow is a vulnerability caused by improper handling of excessively long input strings.

Successful exploitation could allow an attacker to achieve **remote code execution and obtain root-level access** on the affected system.

Because root-level access provides extensive control over the compromised system, this was identified as the **highest-priority vulnerability** in the assessment.

Potential consequences include:

- Unauthorized administrative control
- Execution of arbitrary commands and code
- Modification or deletion of critical system files
- Disabling security mechanisms
- Installation of malicious software
- Potential access to sensitive information
- Potential lateral movement to other systems

### 2. Apache mod_ssl OpenSSL Buffer Overflow

**Affected Service:** Apache/mod_ssl

This vulnerability involves a buffer overflow associated with the Apache mod_ssl/OpenSSL implementation in the vulnerable environment.

Successful exploitation could potentially allow an attacker to execute arbitrary code on the affected system, resulting in system compromise and unauthorized access.

The assessment considered the potential impact on the confidentiality, integrity, and availability of the affected system.

### 3. OpenSSH Authentication Overflow

**Affected Service:** OpenSSH

The OpenSSH Authentication Overflow represents a security weakness affecting the authentication service.

Successful exploitation could potentially result in unauthorized access or compromise of the affected system.

The vulnerability was assessed with a **Medium likelihood** and **High impact**, reflecting the potential consequences of successful exploitation while recognizing that exploitation may depend on specific conditions.

---

# Metasploitable 2 Vulnerabilities

### 4. OpenSSH 4.7p1

**Affected Service:** SSH

OpenSSH 4.7p1 is an outdated version of the OpenSSH service present in the Metasploitable 2 environment.

Running outdated software increases exposure to known security weaknesses and can provide attackers with opportunities to compromise remote administration services.

Potential consequences include:

- Unauthorized access
- Compromise of user accounts
- Privilege escalation
- Remote system compromise
- Further movement within the network

### 5. Apache HTTP Server 2.2.8

**Affected Service:** Apache HTTP Server

Apache HTTP Server 2.2.8 is an outdated version of the web server software.

The use of outdated software increases the organization's exposure to publicly known vulnerabilities and exploitation techniques.

Successful exploitation of weaknesses affecting the web server could result in unauthorized access, service disruption, or further compromise of the affected system.

### 6. VSFTPD 2.3.4 Backdoor Vulnerability

**Affected Service:** VSFTPD  
**Protocol:** FTP  
**Port:** 21  
**CVE:** CVE-2011-2523

The VSFTPD 2.3.4 Backdoor Vulnerability is associated with a malicious backdoor introduced into a compromised distribution of the VSFTPD software.

Successful exploitation can provide unauthorized remote access to the affected system.

The vulnerability presents a significant security concern because an exposed FTP service combined with a known backdoor can provide attackers with a direct path toward system compromise.

---

# Risk Assessment

The risk assessment considered both the **likelihood of exploitation** and the **potential impact** of each vulnerability.

## Risk Factors Considered

### Likelihood

Likelihood represents how probable successful exploitation could be based on factors such as:

- Public availability of vulnerability information
- Availability of exploitation techniques
- Remote accessibility
- Required conditions for successful exploitation
- Exposure of the affected service

### Impact

Impact considers the potential consequences of successful exploitation, including:

- Confidentiality loss
- Integrity compromise
- Availability disruption
- Unauthorized access
- Privilege escalation
- Remote code execution
- System compromise
- Potential exposure of sensitive healthcare information

### Highest-Priority Finding

The **Samba trans2open Buffer Overflow** received particular attention because successful exploitation could result in remote code execution and **root-level privileges**.

This level of access could allow an attacker to take extensive control of the affected system and potentially use the compromised host as a starting point for further attacks.

---

# Recommended Security Controls

The recommended controls were developed to address the vulnerabilities and reduce both the likelihood and potential impact of exploitation.

## Samba trans2open Buffer Overflow

Recommended controls include:

- Upgrade Samba to a supported and secure version.
- Apply available security patches through a structured patch management process.
- Restrict access to SMB services using firewall rules and network segmentation.
- Apply the principle of least privilege.
- Disable unnecessary file-sharing services where they are not required.
- Perform regular vulnerability scanning and security monitoring.

These controls reduce exposure to the vulnerable Samba service and help prevent attackers from exploiting the vulnerability to gain remote code execution and root-level access.

## Apache mod_ssl OpenSSL Buffer Overflow

Recommended controls include:

- Upgrade the affected Apache and OpenSSL components.
- Apply relevant vendor security updates.
- Remove or disable vulnerable services where they are not required.
- Monitor exposed web services for suspicious activity.
- Conduct regular vulnerability assessments.

## OpenSSH Authentication Overflow

Recommended controls include:

- Upgrade OpenSSH to a supported version.
- Apply appropriate security patches.
- Restrict SSH access to authorized users and trusted systems.
- Apply strong authentication controls.
- Use least privilege for administrative accounts.
- Monitor SSH authentication activity.

## OpenSSH 4.7p1

Recommended controls include:

- Upgrade OpenSSH to a supported version.
- Apply security patches.
- Restrict SSH access through firewall rules.
- Enforce strong authentication.
- Apply least privilege to remote administration accounts.
- Monitor remote login activity.

## Apache HTTP Server 2.2.8

Recommended controls include:

- Upgrade the Apache HTTP Server to a supported version.
- Apply current security patches.
- Disable unnecessary modules and services.
- Restrict administrative access.
- Conduct regular vulnerability scanning.
- Monitor web server activity for suspicious behavior.

## VSFTPD 2.3.4 Backdoor Vulnerability

Recommended controls include:

- Remove the vulnerable VSFTPD version and replace it with a secure, maintained solution.
- Disable FTP if the service is not required.
- Restrict FTP access to authorized users and trusted systems.
- Apply strong authentication and MFA where feasible.
- Configure firewalls to limit FTP exposure.
- Monitor FTP activity and conduct regular vulnerability assessments.

---

# Recommended GRC Policies

Four GRC policies were recommended to provide a structured organizational approach to managing the identified vulnerabilities.

## 1. Access Control Policy

The Access Control Policy establishes how access to organizational systems and information is granted, reviewed, and removed.

The policy should be based on **Role-Based Access Control (RBAC)** and the **principle of least privilege**, ensuring that users only receive the access required for their responsibilities.

This policy supports the mitigation of vulnerabilities involving exposed network services and unauthorized access, including:

- Samba trans2open Buffer Overflow
- OpenSSH Authentication Overflow
- OpenSSH 4.7p1
- VSFTPD 2.3.4 Backdoor Vulnerability

---

## 2. Password Policy

The Password Policy establishes requirements for creating, managing, and protecting user credentials.

The policy should require strong and unique passwords, secure credential management, replacement of default credentials, and the use of **Multi-Factor Authentication (MFA)** where appropriate.

This policy primarily supports the protection of authentication mechanisms associated with:

- OpenSSH Authentication Overflow
- OpenSSH 4.7p1

---

## 3. Patch Management Policy

The Patch Management Policy establishes a formal process for identifying, testing, approving, and applying software updates and security patches.

This is particularly important because several vulnerabilities identified during the assessment were associated with outdated or vulnerable software.

The policy supports remediation of all six identified vulnerabilities:

- Samba trans2open Buffer Overflow
- Apache mod_ssl OpenSSL Buffer Overflow
- OpenSSH Authentication Overflow
- OpenSSH 4.7p1
- Apache HTTP Server 2.2.8
- VSFTPD 2.3.4 Backdoor Vulnerability

---

## 4. Vulnerability Management Policy

The Vulnerability Management Policy establishes an ongoing process for identifying, assessing, prioritizing, remediating, and monitoring security vulnerabilities.

Rather than addressing vulnerabilities only after an incident occurs, the policy provides a structured approach for continuously identifying weaknesses and prioritizing remediation based on organizational risk.

The policy applies broadly to all six vulnerabilities identified during the assessment and provides a framework for managing future vulnerabilities across the organization's infrastructure.

---

# My Role — Team Lead

I served as the **Team Lead for Group 35** during the TS Academy Cybersecurity Capstone Project.

My responsibilities included assigning & coordinating team activities, following up on assigned deliverables, reviewing submitted sections, resolving inconsistencies between team submissions, and helping consolidate the individual contributions into one professional security assessment report.

I also contributed to the development and review of the vulnerability findings, risk assessment, recommended security controls, GRC policies, executive summary, and final report.

The experience strengthened my ability to work collaboratively while translating technical cybersecurity findings into structured risk-based recommendations.

---

# Skills Demonstrated

Through this project, I strengthened my practical understanding of:

- Vulnerability Assessment
- Security Assessment
- Risk Assessment
- Vulnerability Analysis
- Security Controls
- Access Control
- Authentication Security
- Patch Management
- Vulnerability Management
- Governance, Risk & Compliance (GRC)
- Security Documentation
- Technical Report Writing
- Team Collaboration
- Team Leadership
- Communicating Technical Risks

---

# Project Deliverables

The final project deliverables included:

### Executive Summary
A high-level overview of the security assessment, key findings, major risks, and recommended improvements.

### Vulnerability Findings
Documentation of the six vulnerabilities identified across Kioptrix and Metasploitable 2, including affected services, descriptions, and potential attacker goals.

### Risk Assessment
Evaluation of vulnerability likelihood, impact, and overall risk.

### Recommended Security Controls
Practical technical measures designed to reduce the likelihood and impact of exploitation.

### Recommended GRC Policies
Four organizational policies covering access control, password security, patch management, and vulnerability management.

### Conclusion
A summary of the overall security posture and the importance of implementing the recommended controls and policies.

---

# Project Outcome

The completed assessment provided Apex Healthcare Solutions with a structured view of the security weaknesses present within its simulated legacy environment.

The project demonstrated how technical vulnerabilities can be translated into organizational risk and how technical controls can be supported by appropriate governance policies.

The final capstone project received a grade of:

## **82% — Very Good**

---

# Project Evidence

The final **Security Assessment Report** submitted to TS Academy serves as the primary evidence for this project.

The report contains the project's executive summary, vulnerability findings, risk assessment, recommended security controls, recommended GRC policies, conclusion, and project team information.

📄 **[View the Final Security Assessment Report](./Apex-Healthcare-Solutions-Security-Assessment.pdf)**

The report was submitted as the official Group 35 capstone deliverable to TS Academy.

---

# Disclaimer

This project was completed strictly for educational and cybersecurity training purposes in a controlled laboratory environment.

Kioptrix and Metasploitable 2 are intentionally vulnerable systems used for security training. No unauthorized testing or exploitation of real-world systems was performed as part of this project.
