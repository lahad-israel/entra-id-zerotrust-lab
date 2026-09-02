# entra-id-zerotrust-lab
Microsoft Entra ID Zero Trust, Conditional Access, and PIM implementation lab.
# Microsoft Entra ID Zero Trust & Identity Governance Architecture

## Project Overview
This project demonstrates the design, deployment, and auditing of an enterprise Zero Trust identity architecture using **Microsoft Entra ID (Azure AD)**. The environment enforces Least Privilege Access, Just-In-Time (JIT) role activation, and strict Conditional Access rules.

## Key Technical Implementations

### 1. Identity Baseline & Licensing
* Created custom security groups (`SG-Finance-Users`, `SG-IT-Admins`, `SG-HR-Department`).
* Assigned **Microsoft Entra ID P2** licensing to enable advanced Conditional Access and Identity Governance features.

<img width="1360" height="927" alt="Screenshot 2026-09-01 at 8 49 23 PM" src="https://github.com/user-attachments/assets/412a8780-0995-4398-8748-d102e977218a" />

<img width="1360" height="927" alt="Screenshot 2026-09-01 at 8 48 41 PM" src="https://github.com/user-attachments/assets/8635076b-c955-4b24-9032-9ff96b2edb4f" />



### 2. Zero Trust Policy Enforcement (`CAP-Enforce-MFA-AllUsers`)
* **Scope:** Enforced Multi-Factor Authentication (MFA) across **All Cloud Apps** for **All Users**.
* **Trusted Network:** Configured Named Locations with trusted corporate IP ranges (`HQ-Trusted-Network`).
* **Resiliency & Safety:** Configured explicit policy exclusions for Break-Glass Emergency Admin accounts (`bg-admin`) to prevent tenant lockout.

### 3. Privileged Identity Management (PIM)
* Deployed Just-In-Time (JIT) role governance for Tier-1 support staff (`jordan.lee`).
* Converted permanent administrative access into **Eligible** activation for the **User Administrator** role, requiring time-bound request justification.

  <img width="1360" height="927" alt="Screenshot 2026-09-01 at 10 52 21 PM" src="https://github.com/user-attachments/assets/ee8f612b-3580-43af-8b22-9a0c04762787" />


### 4. Policy Simulation & Telemetry Analysis
* Tested policy rules using the **What If** simulation engine.
* Analyzed live interactive sign-in telemetry, evaluating initial authentication failure states (Sign-in Error Code `50126`) and Conditional Access evaluation stages.

<img width="1360" height="973" alt="Screenshot 2026-09-01 at 10 57 33 PM" src="https://github.com/user-attachments/assets/7638adf8-ee06-423e-9613-38765337058d" />

<img width="1360" height="927" alt="Screenshot 2026-09-01 at 10 47 18 PM" src="https://github.com/user-attachments/assets/d8bd801d-9786-43e7-bf89-2836c514d19b" />


## Environment & Tech Stack
* **Identity Provider:** Microsoft Entra ID (Azure AD)
* **Security Framework:** Zero Trust Access Architecture
* **Governance:** Microsoft Entra PIM
* **Telemetry & Monitoring:** Entra Sign-in Logs & Audit Logs

---
*Maintained by Lahad Ben Israel | Systems Analyst*
