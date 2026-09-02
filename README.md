# entra-id-zerotrust-lab
Microsoft Entra ID Zero Trust, Conditional Access, and PIM implementation lab.
# Microsoft Entra ID Zero Trust & Identity Governance Architecture

## Project Overview
This project demonstrates the design, deployment, and auditing of an enterprise Zero Trust identity architecture using **Microsoft Entra ID (Azure AD)**. The environment enforces Least Privilege Access, Just-In-Time (JIT) role activation, and strict Conditional Access rules.

## Key Technical Implementations

### 1. Identity Baseline & Licensing
* Created custom security groups (`SG-Finance-Users`, `SG-IT-Admins`, `SG-HR-Department`).
* Assigned **Microsoft Entra ID P2** licensing to enable advanced Conditional Access and Identity Governance features.

### 2. Zero Trust Policy Enforcement (`CAP-Enforce-MFA-AllUsers`)
* **Scope:** Enforced Multi-Factor Authentication (MFA) across **All Cloud Apps** for **All Users**.
* **Trusted Network:** Configured Named Locations with trusted corporate IP ranges (`HQ-Trusted-Network`).
* **Resiliency & Safety:** Configured explicit policy exclusions for Break-Glass Emergency Admin accounts (`bg-admin`) to prevent tenant lockout.

### 3. Privileged Identity Management (PIM)
* Deployed Just-In-Time (JIT) role governance for Tier-1 support staff (`jordan.lee`).
* Converted permanent administrative access into **Eligible** activation for the **User Administrator** role, requiring time-bound request justification.

### 4. Policy Simulation & Telemetry Analysis
* Tested policy rules using the **What If** simulation engine.
* Analyzed live interactive sign-in telemetry, evaluating initial authentication failure states (Sign-in Error Code `50126`) and Conditional Access evaluation stages.

## Environment & Tech Stack
* **Identity Provider:** Microsoft Entra ID (Azure AD)
* **Security Framework:** Zero Trust Access Architecture
* **Governance:** Microsoft Entra PIM
* **Telemetry & Monitoring:** Entra Sign-in Logs & Audit Logs

---
*Maintained by Lahad Ben Israel | Systems Analyst*
