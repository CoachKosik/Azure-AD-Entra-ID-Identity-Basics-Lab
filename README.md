<p align="center">
  <img src="screenshots/identity_basics_banner.png" alt="Azure AD / Entra ID — Identity Basics Lab Banner" width="100%">
</p>

# 🔐 Project 1 — Microsoft Entra ID Identity Administration Basics  
**Core IAM Foundations — Users • Groups • RBAC • Least Privilege**

![Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-Identity_Management-blue?style=flat-square)
![RBAC](https://img.shields.io/badge/RBAC-Least_Privilege-blue?style=flat-square)
![Security](https://img.shields.io/badge/Access_Governance-Best_Practices-green?style=flat-square)

---

## 📚 Table of Contents
- [Objective](#objective)
- [Identity Architecture](#identity-architecture)
- [Users Created](#users-created)
- [Groups & Memberships](#groups--memberships)
- [RBAC Role Assignments](#rbac-role-assignments)
- [Least Privilege Justification](#least-privilege-justification)
- [Screenshots](#screenshots)
- [What I Learned](#what-i-learned)
- [Next Project](#next-project)
- [Repo Structure](#repo-structure)

---
<details open>
  <summary><h2 id="objective">
## 🎯 Objective</h2></summary>
This lab establishes **foundational identity administration skills** inside Microsoft Entra ID (Azure AD):

✔ Created & managed identities  
✔ Implemented role-based access control (RBAC)  
✔ Built security groups with least-privilege design  
✔ Assigned scoped directory roles—_not_ global roles  

This project mirrors real enterprise identity governance practices required for modern IAM analyst/admin roles.

---

## 🏗 Identity Architecture

| Component | Naming Standard | Purpose |
|----------|----------------|---------|
| Users | First + Last | Human identities only |
| Groups | `GG-*` | Role-based permissions |
| Roles | Scoped admin | No global admins |
| Admin Separation | YES | Enforced Segregation of Duties |

---

## 👤 Users Created

| User | Purpose |
|------|---------|
| Maverick Blaze | User admin duties |
| Nathan Dash | Password reset duties |
| Leah Vanta | Contractor — restricted |
| Dawsyn Echo | Contractor — restricted |
| Eddie Spark | Contractor — restricted |

---

## 👥 Groups & Memberships

| Group | Members | Purpose |
|-------|---------|---------|
| GG-Support-Agents | Maverick, Nathan | Internal Helpdesk |
| GG-Contractors | Leah, Dawsyn, Eddie | Restricted access |

---

## 🔐 RBAC Role Assignments

| User | Role | Reason |
|------|------|--------|
| Maverick Blaze | User Administrator | Needs to manage accounts |
| Nathan Dash | Password Administrator | Reset only |
| Contractors | None | No privileged access |

---

## 🛡 Least Privilege Justification

✔ **Segregation of Duties**  
No single user can create AND reset accounts  

✔ **Contractor No-Privilege Design**  
Controls insider risk surface  

✔ **Scoped admin roles only**  
➡ Matches CIS, ISO, and Microsoft Zero Trust guidance  

> _If a user doesn’t need it, they don’t get it._

---

## 📸 Screenshots

<details>
<summary><strong>👤 Users</strong></summary>

screenshots/
├─ users-list.png
</details> <details> <summary><strong>👥 Groups</strong></summary>
txt
Copy code
screenshots/
├─ groups-list.png
├─ support-agents-members.png
├─ contractors-members.png
</details> <details> <summary><strong>🛡 Role Assignments</strong></summary>
txt
Copy code
screenshots/
├─ mav-user-admin.png
├─ nate-password-admin.png
</details>
🧠 What I Learned
Entra ID identity structure & governance model

RBAC design and security justification

How to document IAM decisions for auditors

Why contractors must be isolated and scoped

▶️ Next Project
Project 2 — Enforce MFA for All Users
🔗 https://github.com/CoachKosik/azure-ad-mfa-enforcement

📂 Repo Structure
txt
Copy code
Azure-AD-Entra-ID-Identity-Basics-Lab/
│ README.md
└── screenshots/
    ├─ identity_basics_banner.png
    ├─ users-list.png
    ├─ groups-list.png
    ├─ support-agents-members.png
    ├─ contractors-members.png
    ├─ mav-user-admin.png
    ├─ nate-password-admin.png

---

## 🧠 What I Learned
- Entra ID identity structure & governance model  
- RBAC design and security justification  
- How to document IAM decisions for auditors  
- Why contractors must be isolated and scoped  

---

## ▶️ Next Project
**Project 2 — Enforce MFA for All Users**  
🔗 https://github.com/CoachKosik/azure-ad-mfa-enforcement

---

## 📂 Repo Structure
```txt
Azure-AD-Entra-ID-Identity-Basics-Lab/
│ README.md
└── screenshots/
    ├─ identity_basics_banner.png
    ├─ users-list.png
    ├─ groups-list.png
    ├─ support-agents-members.png
    ├─ contractors-members.png
    ├─ mav-user-admin.png
    ├─ nate-password-admin.png
