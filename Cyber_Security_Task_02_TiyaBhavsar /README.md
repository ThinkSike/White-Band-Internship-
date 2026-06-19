# Cyber Security Task 02: CIA Triad & Risk Assessment

## Objective
The purpose of this task is to master the foundational principles of cybersecurity through the lens of the CIA Triad (Confidentiality, Integrity, and Availability) and apply proactive risk-modeling methodologies to protect an enterprise or academic ecosystem.

---

## 📐 Part A: Understanding the CIA Triad

The core tenets of information security—the CIA Triad—form the architectural benchmark used by practitioners to evaluate risks, secure data assets, and construct security controls.

### 1. Architectural Component Definitions
* **Confidentiality:**
  * *Definition:* Ensuring that sensitive data is shielded from unauthorized exposure, interception, or disclosure at rest, in transit, and in use.
  * *Importance:* Safeguards proprietary information, intellectual property, corporate secrets, and personally identifiable information (PII) from data breaches.
  * *Real-World Example:* Enforcing AES-256 bit end-to-end database encryption alongside strict Role-Based Access Controls (RBAC) to ensure only HR managers can read salary details.
* **Integrity:**
  * *Definition:* Guaranteeing that information remains accurate, authentic, and completely unaltered by unauthorized actors or system failures throughout its lifecycle.
  * *Importance:* Preserves trust in systemic computing states. If data integrity drops, transactions, legal records, and administrative logs become completely unreliable.
  * *Real-World Example:* Using cryptographic hashing functions (like SHA-256) to verify that an executable software update file has not been altered or embedded with a Trojan payload by an attacker.
* **Availability:**
  * *Definition:* Ensuring that authorized users have uninterrupted, reliable access to network resources, data channels, and hardware assets whenever required.
  * *Importance:* Downtime halts business operations, breaks Service Level Agreements (SLAs), and causes critical operational disruptions.
  * *Real-World Example:* Deploying high-availability load balancers, multi-region database replication, and scrubbing lines to mitigate massive Distributed Denial of Service (DDoS) traffic spikes.

### 2. CIA Triad Comparison Matrix
| Core Security Tenet | Objective Focus | Primary Threats | Technical Controls / Solutions |
| :--- | :--- | :--- | :--- |
| **Confidentiality** | Data Privacy & Secret Retention | Phishing, Eavesdropping, Man-in-the-Middle (MitM) | Encryption (AES), RBAC, Multi-Factor Authentication (MFA) |
| **Integrity** | Data Accuracy & Authenticity | Tampering, Code Injection, Unauthorized Commits | Cryptographic Hashes (SHA), Digital Signatures, Write-Once Storage |
| **Availability** | Resource Accessibility | DDoS Attacks, Hardware Failures, Ransomware Locks | Redundant Backups, Load Balancing, RAID, UPS Power Links |

---

## 🏢 Part B: Real-World Case Study (The Equifax Data Breach)

For this case study, the historic **2017 Equifax Data Breach** was analyzed to study structural vulnerabilities and defense failures.

### 1. Incident Chronicle (What Happened?)
In May 2017, threat actors successfully compromised the core network infrastructure of Equifax, one of the world's largest credit reporting bureaus. The initial entry vector was an unpatched, well-known vulnerability in the Apache Struts web framework (CVE-2017-5638). Although a patch had been publicly released by developers months prior, Equifax failed to identify and patch its internal web applications. Attackers exploited this opening to gain a foothold, move laterally through internal network zones, and locate unencrypted databases holding the records of approximately 147 million consumers.

### 2. Impact on the CIA Triad
The breach resulted in a severe, catastrophic compromise of **Confidentiality**. Massive quantities of deeply private customer data were permanently exposed to unauthorized criminal threat actors. This data included Social Security Numbers (SSNs), dates of birth, driver's license details, home physical addresses, and credit card numbers. Because the attackers quietly exfiltrated data rather than modifying it or disrupting the website, the Integrity and Availability tenets remained largely intact, making it a classic failure of Confidentiality controls.

### 3. Downstream Consequences and Incident Impact
* **Financial Loss:** Equifax was handed a historic global legal settlement penalty totaling up to \$700 million in fines, consumer compensation, and regulatory penalties.
* **Reputational Damage:** The company's brand valuation and stock index plummeted overnight, and leadership faced intense public and congressional scrutiny.
* **Long-Term Consumer Risk:** Because SSNs and birth dates cannot be easily changed like a password, the compromised data remains an active resource for identity theft and financial fraud networks indefinitely.

### 4. Remediation and Prevention Strategy
This incident could have been completely neutralized through proper asset management and vulnerability lifecycle policies:
* **Vulnerability & Patch Management:** Establishing automated scanning loops to instantly discover and deploy critical security patches within 24–48 hours of release.
* **Data-at-Rest Encryption Protocols:** Keeping consumer PII fully encrypted within database layers so that even if attackers bypass the perimeter, the stolen data is unreadable without the cryptographic key.
* **Network Segmentation:** Dividing the corporate intranet into isolated zones to block attackers from moving laterally from a public-facing web portal to internal databases.

---

## 📊 Part C: Risk Assessment Activity (Higher Education Context)

Below is a proactive security risk assessment modeling matrix designed for a university or college environment:

| Asset Designation | Identified Threat Vector | Potential Operational Impact | Threat Probability | Impact Severity | Resulting Risk Level |
| :--- | :--- | :--- | :---: | :---: | :---: |
| **Student Academic Records** | Insider Threat / Database SQL Injection | Unauthorized grade modification, identity theft, or FERPA legal violations. | Medium | High | **High** |
| **Examination Data & Papers** | External Targeted Phishing / Compromise | Academic dishonesty, leaked midterms, and complete loss of institutional reputation. | High | High | **Critical** |
| **Official College Website** | Website Defacement / DDoS Flooding | Loss of communication channels during enrollment windows and brand damage. | High | Medium | **Medium** |
| **Faculty Personnel & HR Files** | Financial Ransomware Deployment | Complete encryption of payroll records, bank details, and employee contracts. | Medium | Critical | **High** |
| **Campus Network Infrastructure** | Unauthenticated Rogue Device Access | Malware spreading laterally across library labs, classroom computers, and research units. | High | High | **High** |

---

## 🔍 Part D: Threat Identification & Mitigations

An in-depth analysis of major infrastructure security threats alongside recommended technical solutions:

### 1. Insider Threat
* **Explanation:** A security risk originating from within the organization. This involves employees, contractors, or trusted partners who have legitimate credentials and network privileges but abuse them to steal data, alter configurations, or sabotage systems.
* **Mitigation Control:** Enforce the Principle of Least Privilege (PoLP) using strict Role-Based Access Controls (RBAC), and deploy User and Entity Behavior Analytics (UEBA) to log and flag anomalous file downloads.

### 2. Social Engineering
* **Explanation:** Manipulating human psychology rather than software code to trick individuals into breaking security protocols, revealing passwords, or granting unauthorized entry.
* **Mitigation Control:** Conduct continuous, mandatory simulated phishing tests and security awareness training, and establish strict corporate protocols for verifying out-of-band requests.

### 3. Unpatched Vulnerabilities
* **Explanation:** Known security flaws, bugs, or weaknesses within operating systems or third-party software applications for which a vendor has released a patch, but the organization has not yet installed it.
* **Mitigation Control:** Implement automated Vulnerability Assessment and Patch Management tools (e.g., Nessus, WSUS) to ensure all endpoint devices and servers run the latest secure software builds.

### 4. Poor Access Control
* **Explanation:** Weak security limits that fail to properly authenticate or authorize users, such as allowing shared administrative logins, using weak single-factor passwords, or failing to revoke access for terminated employees.
* **Mitigation Control:** Enforce mandatory Multi-Factor Authentication (MFA) across all endpoints, deploy Single Sign-On (SSO), and use automated identity auditing tools to track permissions.

---

## 🛠️ Part E: Security Recommendations & Safeguards

The strategic implementation plan for modern cybersecurity controls across an enterprise network:

### 1. Multi-Factor Authentication (MFA)
* *Justification:* Drastically reduces account takeover risks. Even if a threat actor steals a user's password through phishing or credential stuffing, they cannot access the account without the dynamic, time-sensitive verification code from an authenticator app or hardware token.

### 2. Security Awareness Training
* *Justification:* Strengthens human perimeter defenses. Educating staff on how to spot phishing cues, avoid unverified links, and maintain secure habits reduces the likelihood of a successful social engineering attack.

### 3. Regular Backups (The 3-2-1 Rule)
* *Justification:* The primary recovery defense against ransomware. Organizations should keep at least **three** copies of data, stored on **two** different media types, with **one** copy kept completely offline in an immutable storage container. If malware encrypts live systems, operations can be restored without paying a ransom.

---

## 🎛️ Part F: Mini Security Consultant Activity

### Formal Cybersecurity Posture Report
**To:** The Executive Board of Directors & College Leadership  
**From:** Cybersecurity Consultant Specialist  
**Subject:** Security Posture Improvement & Risk Mitigation Framework

#### 🛑 Top 5 Cybersecurity Risks Facing Our Campus
1. **Targeted Phishing Attacks on Faculty:** Criminal syndicates tricking payroll departments into rerouting financial resources or leaking exam material.
2. **Ransomware Disruptions to Learning Management Systems (LMS):** Enforced encryption of student dashboards and course materials, bringing virtual learning to a standstill.
3. **Unpatched Campus Server Vulnerabilities:** Public-facing enrollment servers running outdated code, making them easy targets for exploitation.
4. **Weak Password Hygiene and Lack of Uniform MFA:** Students and staff using easily guessed credentials without a second authentication layer.
5. **Rogue Guest Devices in the Dorm Intranet:** Unmanaged personal laptops introducing malware and spreading it to administrative subnets.

#### 🛠️ Top 5 Strategic Technical Recommendations
1. **Mandatory Sitewide MFA Mandate:** Enforce prompt, phishing-resistant Multi-Factor Authentication across all official college login portals.
2. **Automated Vulnerability Management Lifecycle:** Deploy centralized patching pipelines to ensure all university-managed software updates automatically.
3. **Network Segmentation via Virtual LANs (VLANs):** Completely isolate the student dorm Wi-Fi network from the core server zones holding financial and administrative data.
4. **Immutable Offline Backup Deployment:** Establish automated, air-gapped daily snapshot backups of critical student records and payroll registers.
5. **Continuous Phishing Simulation Training:** Provide quarterly security awareness exercises for all administrative staff and faculty members.

#### 📈 Expected Organizational Benefits
* **Reduced Attack Surface:** Eliminates over 90% of automated credential attacks and entry-level server exploits.
* **Regulatory and Legal Compliance:** Aligns institutional operations with data privacy standards, reducing the risk of costly regulatory penalties.
* **Business Continuity Resilience:** Ensures that even in a worst-case security incident, critical campus systems can be restored quickly from secure backups with minimal downtime.

---
