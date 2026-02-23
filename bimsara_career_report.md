**CAREER REPORT**
**Bimsara Gunarathna**
Software / DevOps Engineer  —  Deployment & Scalability Team
Enactor Ltd  |  August 2023 – February 2026


# Executive Summary

Bimsara Gunarathna joined Enactor in August 2023 as a Software/DevOps Engineer on the Deployment & Scalability team, based in Galle, Sri Lanka, reporting to Tech Lead Indika Thushara Semage. Over 2.5 years he progressed from general deployment support to owning major platform engineering work — most notably the Proxmox cloud provider integration into the Enactor Deployment Portal (EDP) and the AWS-to-Proxmox environment migration strategy. By February 2026 he had authored 5 of the 6 features in the EDP v1.0.250.243 release, owned two key Confluence knowledge pages, and earned peer code-review responsibilities, placing him firmly on a senior/tech-lead trajectory.

# Profile at a Glance

| Field | Detail |
| --- | --- |
| Full Name | Bimsara Gunarathna |
| Email | bimsara.gunarathna@enactor.co.uk |
| Team | Deployment & Scalability |
| Tech Lead | Indika Thushara Semage |
| Location | Galle, Sri Lanka |
| Tenure | August 2023 – February 2026 (active) |
| Current Level | Mid-level → Senior-track DevOps / Platform Engineer |
| Core Specialisations | Platform engineering, CI/CD, AWS & Proxmox infrastructure, Docker, EDP development |

# Team & Organisation

## Deployment & Scalability Team (Sri Lanka)
1. Indika Thushara Semage — Tech Lead
2. Bimsara Gunarathna — Software / DevOps Engineer
3. Karikaran Vettivel — Software Engineer
4. Nilucshan Siva — Associate Tech Lead (departing Feb 2026; Kubernetes SME)
5. Rohan Desilva — Software Engineer
6. Janaka Bandara — Manager / Infrastructure approvals
7. Surath Wijesinghe — Software Engineer
8. Chathuranga Nimantha — Software Engineer

## UK Stakeholders
1. Ben Munro Wild — Principal Architect (Modernisation Strategy, Proxmox reviews)
2. Lee Smith — Senior Engineer (authorisation codes for Proxmox integration DO-2461)
3. David Hall / John Wood — UK DevOps
4. Dinesh Jayasinghe — Environment operations (AWS-to-Proxmox migration coordination)

# Major Projects & Milestones

## 1. Proxmox Cloud Provider Integration (DO-2461)  —  Oct–Nov 2025
Bimsara's flagship deliverable. Extended the Enactor Deployment Portal to support Proxmox as a full cloud provider alongside AWS, enabling on-premises VM lifecycle management through the same portal UI and Ansible automation layer. The ticket progressed through Team Lead Approval → Technical Approval → Ready For Test → Closed. Lee Smith (UK) provided authorisation codes; Ben Munro Wild endorsed a future GitOps approach in a Confluence comment on the Modernisation Strategy Report.

## 2. EDP Release v1.0.250.243  —  Nov 2025
Bimsara authored 5 of the 6 documented features in this release:

| Ticket | Title | Type |
| --- | --- | --- |
| DO-2461 | Introduce Proxmox cloud provider support | Enhancement |
| DO-2451 | Set transaction_isolation = READ-COMMITTED for new DB deployments | Enhancement |
| DO-2412 | Implement health check for database containers | Enhancement |
| DO-2524 | Fix Ansible linux-deploy-suite skopeo installation error | Bug Fix |
| DO-2316 | Database Deployment Fails on First Attempt (Read Replica) | Bug Fix |

## 3. AWS-to-Proxmox EM Migration — Phase 1  (Nov 2025)
Authored the Confluence page "AWS to Proxmox EM Migration — Phase 1". Coordinated decommissioning of 161 manually-created VMs (EDIAPT-631), environment cleanup, and the Specsavers support environment implementation on Proxmox (EDIAPT-642). Dinesh Jayasinghe used the page as a reference document for environment handovers.

## 4. EDP Modernisation Strategy Report
Authored a Confluence page outlining the long-term modernisation roadmap for the Deployment Portal. Ben Munro Wild commented on it suggesting a GitOps approach as Phase 2 — indicating the document was taken seriously at architecture level.

## 5. Power BI Deployment Integration  —  Jul 2025
1. DO-2497: Deploy VM for Enactor Operational DB Access during Power BI Deployment
2. DO-2501 / CORP-5851: Fix Power BI Models missing from Deployment Dashboard
3. DO-2484: Add character length validation to Environment Identifier for BI Deployments

## 6. Database & Infrastructure Improvements  —  Dec 2024–Jul 2025
1. DO-2194: Fix RDS Deployment Status Incorrect in Pre-Prod and Prod
2. DO-2193: RDS Name Validation
3. DO-2172: Validate Compatible Platform Version when creating a topology
4. DO-2168: Improve DB deployments — stop RDS instance if read replica is associated
5. DO-2474: SQL error — Illegal mix of collations in MariaDB Docker Image

# JIRA Project Coverage (150+ Tickets)

| Project | Focus Area | Representative Tickets |
| --- | --- | --- |
| DO | EDP feature development & DevOps | DO-2461, 2451, 2412, 2524, 2316, 2526, 2521, 2513 |
| EDIAPT | Infrastructure, Proxmox environments, CI/CD | EDIAPT-656, 642, 631, 606, 373, 803 |
| CORP | Corporate infra, customer environments | CORP-6415, 6198, 6134, 6057, 5882, 6014 |
| SDI | Standard Docker Images, CVE remediation | SDI-571, 570, 567, 546 |
| EDAT | EoD & DevOps ad-hoc | EDAT-54 (Harrods), EDAT-60 (Jenkins) |
| RT | Release team bugs, CVE tracking | RT-1265 (Tomcat CVE-2025-24813) |
| INS | Product installers | INS-455, INS-404 |
| ENCR | Change control | ENCR-579 |
| PLAT | Core platform (reviewer) | PLAT-26026 |

# Customer Engagement

| Customer | Region | Engagement Summary |
| --- | --- | --- |
| Harrods | UK | EDAT-54: 2.7.525 build deploy; EDIAPT-606: RC2.295.1569 upgrade |
| Frasers | UK | CORP-6134: Docker version upgrade advisory |
| The Works | UK | CORP-6258: High memory utilisation on live worker node |
| Specsavers | UK/Global | EDIAPT-642: Proxmox support environment implementation |
| Magasin du Nord | Denmark | DO-2521: Routing issue for device serial number configuration |
| Leroy Merlin | France | DO-2507: RC delivery; K8s environment adoption work |
| Macys | USA | Kubernetes adoption support (via Nilucshan's K8s initiative) |
| PH Mexico | Mexico | Domain/HTTPS certificate troubleshooting (Jan–Feb 2025) |
| CTAC | TBC | EDIAPT-714: Presales environment creation |

# CI/CD & Jenkins Work

1. EDIAPT-656: Investigated and resolved Test Configuration 2_7_1784 Pipeline Job Failure (Feb 2026)
2. EDIAPT-803: Reviewed Jenkins SCDT Docker image update to v2.541.2 LTS with JDK 21 (Feb 2026)
3. CORP-6141: Resolved Jenkins Agent Service startup failure on Windows
4. CORP-6057: Fixed 'Create Platform Branch and Pipelines' job to correctly generate release jobs
5. DO-2429: Investigated and resolved 'Create Platform Branch off' job regression
6. DO-2526: Authored Functional Specification for Prod Artifact & Docker Cleanup Process
7. May 2024: Collaborated with David Hall (UK) on Jenkins optimisation; documented findings

# Security & Compliance

1. RT-1265 / SDI-570: Coordinated Apache Tomcat upgrade to 9.0.99+ for CVE-2025-24813
2. SDI-567: Tomcat 9.0.107 vulnerability upgrade
3. CORP-6014: Added Trivy report generation option to Platform Release Pipeline
4. EDIAPT-787: Participated in FOREGENIX Penetration Test Questionnaire (Feb 2026)
5. CORP-5882: Resolved IAM role permission gap — added s3:GetBucketLocation to EDP AssumeRole policy

# Confluence Documentation

| Page Title | Space | Notes |
| --- | --- | --- |
| EDP Modernisation Strategy Report | bimsara.gunarathna (personal) | Ben Munro Wild commented advocating GitOps as Phase 2 |
| AWS to Proxmox EM Migration — Phase 1 | bimsara.gunarathna (personal) | Used by Dinesh Jayasinghe for environment handover coordination |
| EDP Release Notes v1.0.250.243 (contributor) | Enactor — Development (owned by indika.semage) | 5 of 6 features attributed to Bimsara |
| Release config-4_3 (contributor) | Enactor — Development (owned by karikaran.vettivel) | Referenced as contributor |

Indika Semage explicitly requested Bimsara update the EDP user manual to document the Proxmox implementation (Nov 2025, still pending as of Feb 2026).

# Training & Development

| Date | Event | Notes |
| --- | --- | --- |
| Aug 2023 | Infrastructure Deployment Process Training | Onboarding training on EDP and Enactor deployment model |
| May 2024 | Jenkins Optimisation Workshop | With David Hall (UK); findings documented |
| Aug 2025 | Spec Review — RFC-3 File Repository for Settlement Files | With Indika Semage; cross-functional design input |
| Oct 2025 | DO-2461 Implementation Review | With Karikaran Vettivel prior to Proxmox PR merge |
| Jan 2026 | Proxmox Disk Usage Review | With Ben Munro Wild |
| Feb 2026 | AWS Cost Optimisation Review | Suggested adding Rohan Desilva to the session |
| Feb 2026 | Kubernetes Deployment Training — Session 1 | Organised by Nilucshan Siva; Minikube, K8s manifests, AWS EKS |

# Technical Environment

## Workstation (Feb 2026)
1. OS: Ubuntu 22.04.5 LTS, Kernel 6.8.0-59-generic (HWE), dual-boot Windows 11 Pro
2. HW: HP ProBook 450 G9 — Intel i7-1255U (10 cores), 32 GB RAM, Lexar NM620 2 TB NVMe
3. Known issue: Realtek RTL8852BE WiFi poor Linux driver support; laptop replacement requested

## Technology Stack

| Category | Technologies |
| --- | --- |
| CI/CD | Jenkins (Docker agents, LTS, JDK 21 review) |
| Containers | Docker, Docker Swarm, MariaDB containers, ARM64 multi-arch builds |
| Cloud | AWS (EC2, IAM, S3, RDS, ECR), Proxmox (on-prem virtualisation) |
| Automation | Ansible, Enactor Deployment Portal (EDP) |
| Monitoring & Security | Zabbix, Trivy vulnerability scanning |
| Database | MariaDB, AWS RDS (multi-AZ, read replicas) |
| BI | Power BI integration |
| Version Control | Git, SVN (legacy) |
| Tooling | Jira, Confluence, Slack (#deployment-and-scalability-team), Google Meet |

# Outstanding Items (Feb 2026)

| Ticket / Task | Status | Notes |
| --- | --- | --- |
| EDIAPT-201 — Trigger initial platform broadcasts from EDP | In Review (28+ days) | Needs follow-up |
| EDIAPT-659 — Branch off Product Installers for gamma2 | In Review (28+ days) | Needs follow-up |
| EDP User Manual — Proxmox section | Pending | Requested by Indika Semage (Nov 2025) |
| EDIAPT-714 — CTAC presales environment | Unassigned | Upcoming task |
| Laptop replacement | Pending approval | Requested to Janaka Bandara & Nishantha Abeywardena |
| Kubernetes Training — Sessions 2+ | Scheduled | Session 1 completed Feb 23, 2026 |
| Proxmox 161-VM cleanup & data centre migration | In progress | DevOps team initiative, Feb 2026 |

# Career Assessment

## Current Level
Mid-level DevOps / Platform Engineer. Trajectory: SE II → Senior within 6–12 months based on current output.

## Evidence of Senior-Track Progression
1. End-to-end ownership of major platform feature (Proxmox integration)
2. Documentation authored at architecture level (Modernisation Strategy commented on by principal architect)
3. Peer code-review responsibilities (Karikaran requesting reviews)
4. Highest individual feature contribution in EDP v1.0.250.243 release (5 of 6)
5. Proactively contributes to team process improvements and cost optimisation
6. Participating in external security audits (FOREGENIX pentest questionnaire)

## Core Strengths
1. Deep EDP product ownership — both feature development and infrastructure layer
2. Strong CI/CD expertise: Jenkins, Ansible, Docker pipeline management
3. Dual AWS + Proxmox cloud competency
4. Reliable delivery on tier-1 retail customer deployments (Harrods, Frasers, The Works)
5. Technical writing and knowledge management

## Growth Areas
1. Kubernetes — actively training; K8s with Leroy Merlin and Macys is the natural next area
2. GitOps tooling (Argo CD / Flux) — Ben Munro Wild's recommended Phase 2 direction
3. Formal tech-lead responsibilities — code review and approval workflows are the next step

# Career Timeline

| Period | Key Event |
| --- | --- |
| Aug 2023 | Joined Enactor; completed infrastructure deployment process training |
| May 2024 | Jenkins optimisation project with David Hall (UK); findings documented |
| Dec 2024 | EDP DB/RDS stability improvements (DO-2168, 2172, 2193, 2194) |
| Jul 2025 | Power BI deployment integration; MariaDB collation fix |
| Aug–Sep 2025 | Trivy security pipeline; identity server Ubuntu upgrade; Frasers & The Works support |
| Oct 2025 | DO-2461 implementation review; Proxmox SSH access & environment investigations |
| Nov 2025 | EDP v1.0.250.243 released (5 Bimsara features); Proxmox migration Phase 1 doc published |
| Dec 2025 | Specsavers Proxmox environment deployment |
| Jan 2026 | Proxmox disk usage review with Ben Munro Wild; Harrods upgrade |
| Feb 2026 | Kubernetes training; AWS Cost Optimisation review; Jenkins LTS review; FOREGENIX audit |

---

*Report compiled from Enactor Gmail inbox (bimsara.gunarathna@enactor.co.uk) — JIRA notifications, Confluence mentions, meeting invites, and internal communications spanning August 2023 to February 2026. For internal use only.*
