# Expert Decision Replay Platform (EDRP)

> An enterprise-grade decision intelligence and audit management platform that captures, evaluates, reviews, and replays organizational decisions, so institutional knowledge stays preserved, auditable, and accessible across teams.

**Internship Project:** Developed as part of the **Infosys Springboard Virtual Internship 7.0**.

---

## Table of Contents

- [Overview](#overview)
- [Core Capabilities](#core-capabilities)
- [Project Milestones](#project-milestones)
- [User Roles](#user-roles)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Author](#author)

---

## Overview

Organizations make important decisions every day, but the reasoning behind them is often lost. EDRP solves this by providing a structured way to document decisions, compare alternatives, route them through approval chains, and replay how each decision evolved over time, all backed by tamper-evident audit logs and AI-assisted search.

## Core Capabilities

| Capability | Description |
|---|---|
| **Structured Decision Capture** | Standardized templates ensure context, risks, and alternatives are documented upfront. |
| **Historical Replay & Versioning** | Full visibility into how decisions evolved and why specific choices were made. |
| **Enterprise Security & Compliance** | Role-based access control, tamper-evident audit logs, and secure authentication flows. |
| **Intelligent Knowledge Retrieval** | Instant lookup of past decisions with AI-assisted querying. |
| **Multi-Channel Alerts** | Coordinated in-app notifications and email updates keep stakeholders aligned. |

## Project Milestones

### Milestone 1: Core Architecture, Database Design & Secure Authentication
- Designed the complete relational database schema covering users, roles, teams, decisions, alternatives, reviews, replays, attachments, discussion threads, meeting notes, notifications, activity logs, support tickets, and system settings.
- Built a secure authentication system with cryptographic password hashing, access token management, and persistent multi-day sessions.
- Developed a multi-step onboarding workflow with real-time 6-digit email verification before account activation.
- Implemented automatic role-based ID generation with unique prefixes for Administrators, Managers, Reviewers, and Employees.
- Created an administrative approval pipeline where new accounts are reviewed before gaining access.
- Structured the backend API with modular service and repository layers.

### Milestone 2: Decision Lifecycle, Alternative Analysis & Team Collaboration
- Built the end-to-end decision lifecycle: **Draft → Under Review → Approved / Rejected → Archived**.
- Developed the Alternative Analysis engine to compare options by pros, cons, financial estimates, risk ratings, feasibility scores, and a designated recommendation.
- Added document attachments and file uploads for technical specifications, architecture diagrams, and project sheets.
- Added meeting notes and collaborative discussion threads linked directly to decisions.
- Created a centralized Knowledge Repository with multi-parameter search, category filters, tag navigation, and instant retrieval.
- Built an in-app notification center with real-time status alerts, unread counts, and priority badges.

### Milestone 3: Audit Trail, Replay Engine, Multi-Tier Approvals & Role Dashboards
- Engineered an append-only audit logging system that records actor identity, action type, entity details, IP address, client environment, and timestamp.
- Implemented before-and-after change detection to track every modification across all entities.
- Built configurable multi-tier approval chains with sequential reviews, change requests, rejection explanations, and final sign-offs.
- Created the interactive **Decision Replay Engine**, which takes snapshot versions of a decision and lets stakeholders step through its full history.
- Designed four role-specific workspaces (see [User Roles](#user-roles)).
- Added administrative system settings and an in-app support ticketing system.

### Milestone 4: AI Decision Intelligence, Search & Advanced Notification System
- Integrated an AI Knowledge Assistant using retrieval-augmented generation (RAG) to analyze historical decisions and answer organizational queries.
- Built automated AI decision summaries, risk-factor evaluations, and recommendation insights.
- Implemented automated, branded HTML email notifications for account approvals, role changes, status updates, password changes, and review outcomes.
- Added a deliverability filter that detects simulated or test email addresses and skips sending to them, preventing bounce-back notices.
- Built system analytics covering decision completion rates, review turnaround times, approval trends, and team productivity.
- Developed automated backup management and administrative data export.

## User Roles

| Role | Workspace Features |
|---|---|
| **Administrator** | User approvals, platform health, global audit trails, and security settings. |
| **Manager** | Team-level decisions, financial impact tracking, and escalation routing. |
| **Reviewer** | Evaluation queues, alternative comparisons, and one-click review actions. |
| **Employee** | Drafting decisions, tracking submissions, and managing assigned tasks. |

## Project Structure

```
.
├── EDRP UI/            # UI designs and assets
├── backend/            # Backend API (services, repositories, routes)
├── database/           # Database schema and scripts
├── docker/             # Docker configuration
├── docs/               # Project documentation
├── frontend/           # Frontend application
├── .env.example        # Sample environment variables
├── Dockerfile.backend
└── Dockerfile.frontend
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/akhila-kothapalli/Expert_Decision_Replay_Platform.git
   cd Expert_Decision_Replay_Platform
   ```

2. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   Open `.env` and fill in your own values (database credentials, secret keys, email settings, AI API key). Never commit your real `.env` file.

3. **Run the application**

   Follow the setup steps in the `docs/` folder, or build with the provided Dockerfiles.

## Author

**Akhila Kothapalli**
Infosys Springboard Virtual Internship 7.0

GitHub: [@akhila-kothapalli](https://github.com/akhila-kothapalli)
