# System Design Projects

A portfolio of system analysis and design work — covering stakeholder analysis, SDLC selection, architecture patterns, and full technical documentation.

Built as part of my Systems Design coursework and personal practice.

---

## Purpose

This repository showcases my end-to-end system design process. Each project demonstrates the full lifecycle of system analysis and design — from identifying stakeholders and mapping system components, to selecting an SDLC model, designing the architecture, and documenting the final solution.

The goal is to build a transparent, growing body of work that reflects how I think about systems: structured, evidence-based, and grounded in real business constraints.

---

## Projects

| # | Project | Focus | SDLC Model | Architecture | Status |
|---|---|---|---|---|---|
| 1 | [Crusty Muse Bakery](./projects/01-crusty-muse-bakery/) | Online ordering system for a small bakery | Agile | 2-Tier (Client-Server) | ✅ Complete |
| 2 | [Digital Transformation Strategy](./projects/02-digital-transformation-retail/) | Cloud-based unified commerce platform for a 50-store apparel retailer | Agile | Cloud SaaS (API-first, Unified Commerce) | ✅ Complete |

---

## Skills Demonstrated

- **Stakeholder Analysis** — Identifying stakeholders, their roles, and their system interactions
- **System Components Mapping** — Documenting inputs, processes, and outputs for each use case
- **SDLC Selection** — Choosing and justifying the right software development lifecycle model
- **Architecture Design** — Designing and documenting system architecture with clear flow explanations
- **Requirements Engineering** — Writing functional and non-functional requirements tied to stakeholder needs
- **Alternative Evaluation** — Weighted scoring for vendor and platform selection
- **Feasibility & Risk Analysis** — Technical, economic, operational feasibility and risk mitigation
- **Technical Documentation** — Writing structured, decision-focused project summaries
- **Diagramming** — Process flows, DFDs, ERDs, and UML diagrams

---

## Repository Structure

```
system-design-projects/
├── README.md
├── assets/
│   └── system-design-cover.png
└── projects/
    ├── 01-crusty-muse-bakery/
    │   ├── README.md
    │   ├── system-architecture-diagram.png
    │   └── Final_Project_Bakery_Shop.docx
    └── 02-digital-transformation-retail/
        ├── README.md
        ├── process-flow-omnichannel.png
        ├── context-dfd.png
        ├── level0-dfd.png
        ├── uml-use-case.png
        └── Final_Project_Report.pdf
```

---

## How to Navigate

- Start with the **Projects** table above.
- Click into any project folder to view its full design documentation.
- Each project folder contains:
  - A `README.md` with the full analysis
  - Architecture diagrams (PNG)
  - Source documents (DOCX / PDF)

---

## Author

**Andre Philip Nyanjahia**  
Full-Stack Systems Architect | Data Strategist

[GitHub](https://github.com/Andre-tech671) · [LinkedIn](https://linkedin.com/in/andre-nyanjahia-ab664228a)

---

## License

This repository is for educational and portfolio purposes.

---

# Project 1: Crusty Muse Bakery — Basic System Design

![System Architecture Diagram](./projects/01-crusty-muse-bakery/system-architecture-diagram.png)

## Overview

A basic system analysis and design for **Crusty Muse Bakery**, a small bakery currently accepting orders only in person or by phone. The goal is to propose a simple, low-cost, mobile-friendly online ordering system.

---

## Business Problem

Crusty Muse Bakery currently accepts orders only in person or by phone. This results in:

- Delays during peak hours
- Manual order-taking mistakes
- Lost sales because customers cannot order online

The bakery needs a simple digital system that:

- Supports **20–30 orders per day**
- Is easy to maintain
- Fits a small budget

---

## System Goal

Provide a simple, mobile-friendly online ordering system where:

- **Customers** can browse items, add them to a cart, and place orders.
- **Bakery staff** can view incoming orders, prepare items, and update order status.
- **Managers/Owners** can oversee operations, check order volume, update prices, and manage product availability.
- **Payment Processor** handles secure online payment processing.

---

## Task 1: Basic System Analysis

### A. Key Stakeholders

| Stakeholder | Role |
|---|---|
| Customer | Views menu items, adds products to cart, places orders |
| Bakery Staff | Reviews new incoming orders, prepares items, updates order status |
| Bakery Manager/Owner | Oversees operations, checks order volume, updates prices, manages product availability |
| Payment Processor | Handles secure online payment processing for customer orders |

### B. System Components

| Use Case | Input | Process | Output |
|---|---|---|---|
| Status confirmation email to the customer | Customer email address + order status | System generates an email message and formats confirmation details | Confirmation email sent to the customer |

---

## Task 2: SDLC Model Selection

| Choice of SDLC Model | Reason |
|---|---|
| **Agile** | • Requirements may evolve as the bakery tests the online system.<br>• Agile allows quick updates (e.g., adding delivery, new menu items, coupons).<br>• The bakery is small, so frequent feedback cycles from staff and customers are feasible. |

---

## Task 3: System Architecture

The system follows a **2-Tier (Client-Server) Architecture**.

### Architecture Diagram

![System Architecture Diagram](./projects/01-crusty-muse-bakery/system-architecture-diagram.png)

### Explanation of Flow

1. **Customer** interacts with the **Website** (Frontend UI) via phone or laptop.
2. The **Website** sends requests to the **Server**.
3. The **Server** reads/writes data in the **Database** (Products, Orders, Customer Details).
4. The **Staff Dashboard** retrieves order information from the Server to view/update orders.

### Architecture Pattern Justification

| Aspect | Detail |
|---|---|
| **Pattern** | 2-Tier (Client-Server) |
| **Reason** | Simple, cost-effective, and easy to maintain — perfect for a small bakery. The client (web browser) handles the UI, while the server manages business logic and the database. |
| **Scalability** | The traffic (20–30 orders/day) is small enough that a more complex 3-tier architecture is unnecessary. |

---

## Task 4: Project Summary

| Category | Details |
|---|---|
| **Business Problem** | Crusty Muse Bakery currently accepts orders only in person or by phone. This results in delays, manual mistakes, and lost sales because customers cannot order online. The bakery needs a simple digital system that allows customers to place orders online and helps staff track them easily. |
| **System Goal** | To provide a simple, mobile-friendly online ordering system where customers can browse items, add them to a cart, and place orders, while bakery staff can view and update order status. The system must be low-cost, easy to maintain, and support 20–30 orders per day. |
| **Technical Choices — SDLC Model** | **Agile** — allows the bakery to build the system in small parts and adjust it based on feedback. Requirements may change as the bakery tests what works best. Agile avoids expensive rework and supports small-budget, fast-iteration development. |
| **Technical Choices — Architecture Pattern** | **2-Tier (Client-Server)** — simple, cost-effective, and easy to maintain. The client (web browser) handles the UI, while the server manages business logic and the database. The traffic (20–30 orders/day) is small enough that a more complex 3-tier architecture is unnecessary. |

---

# Project 2: Digital Transformation Strategy for a Mid-Sized Retail Chain

![Process Flow — Omnichannel Checkout](./projects/02-digital-transformation-retail/process-flow-omnichannel.png)

## Overview

A full systems analysis and digital transformation strategy for a **mid-sized apparel and accessories retailer** operating approximately **50 stores** and an e-commerce platform in the United States. The retailer faces outdated POS systems, fragmented data, and a suboptimal online experience — resulting in checkout delays, stockouts, inconsistent customer data, and lost sales.

The goal: propose a **cloud-based unified commerce platform** that consolidates data, automates inventory, delivers a seamless omnichannel experience, and prepares the retailer for expansion to **100+ stores** within two years.

---

## Business Problem

The retailer's current architecture is fragmented and on-premises:

- **POS:** Windows CE terminals with slow transaction processing (>5s) and outdated 2009 card reader drivers
- **E-commerce:** Magento 1.9 on a separate MySQL database (CLS >0.25, page load >2s on 4G)
- **Data:** On-premises SQL databases per store with nightly batch updates to HQ
- **Inventory:** Manual Excel-based processes

**Pain points:**

- Checkout delays reduce conversion rates
- Manual restocking causes stockouts and production delays
- Split email lists hinder targeted marketing
- No real-time inventory visibility
- No unified omnichannel experience

---

## System Goal

Deliver a cloud-based unified commerce platform that:

- Processes in-store sales in ≤5 seconds
- Provides real-time inventory decrement across all channels
- Exposes a 360° customer profile via API
- Supports Buy Online Pickup In-Store (BOPIS)
- Maintains ≥99.9% availability
- Scales to 3× holiday traffic without downtime

---

## Step I: Current System Assessment

### System Architecture Overview

The retailer operates a fragmented, largely on-premises environment. POS terminals run Windows CE with slow processing and outdated card reader drivers. E-commerce runs Magento 1.9 on a separate MySQL database with poor web performance. Data is stored in per-store SQL databases with nightly batch updates to HQ. Inventory is managed manually in Excel. The architecture lacks real-time integration, centralized data, and scalability.

### Pain-Points Matrix

| Pain Point | Impact | Root Cause |
|---|---|---|
| Checkout delays | Reduced conversion rates | Slow POS on Windows CE |
| Stockouts and delayed restocking | Lost sales, poor customer experience | Manual Excel-based inventory, no real-time visibility |
| Fragmented marketing and customer data | Ineffective campaigns, inconsistent CX | Split email lists, inconsistent data across Magento and store DBs |
| Slow e-commerce performance | High bounce rates, abandoned carts | Magento 1.9 on separate MySQL DB |
| Lack of omnichannel capabilities | Missed BOPIS and unified cart opportunities | Siloed systems, batch updates, no unified platform |

### Key Inefficiencies

- Manual CSV imports and duplicate data entry
- Inconsistent customer data across systems
- Slow POS and web interfaces
- No real-time inventory visibility
- Per-store databases and nightly batch updates block scaling
- No API-first integration

---

## Step II: Stakeholder Requirements

### Stakeholder Identification

| Stakeholder | Interests |
|---|---|
| Customers | Fast purchases, unified cart, real-time stock visibility |
| Store Staff | Reliable POS ≤5s, inventory visibility for quick lookups |
| Management | Single customer view, margin analytics, scalable growth |
| IT Team | Maintainability, security, compliance (API-first, GDPR) |

### Functional Requirements

| ID | Requirement | Justification |
|---|---|---|
| FR01 | Process in-store sales in ≤5s | Addresses checkout delays |
| FR02 | Real-time inventory decrement on any channel | Prevents stockouts, enables BOPIS |
| FR03 | 360° customer profile exposed via API | Enables personalized marketing |
| FR04 | Support BOPIS | Delivers omnichannel experience |

### Non-Functional Requirements

| ID | Requirement | Justification |
|---|---|---|
| NFR01 | System availability ≥99.9% | Reliable operations for all stakeholders |
| NFR02 | Page load <2s on 4G | Improves online experience |
| NFR03 | Scale to 3× holiday traffic | Supports peak demand and expansion |
| NFR04 | API-first, GDPR-compliant security | Aligns with IT priorities |

---

## Step III: Alternative Solution Evaluation

### Comparative Analysis

Weights: Functional fit 40%, scalability 20%, TCO 20%, implementation risk 10%, vendor viability 10%.

| Criteria | Weight | Salesforce + POS | Shopify Plus + Square | Custom Microservices |
|---|---|---|---|---|
| Functional fit | 40% | 9/10 → 3.6 | 8/10 → 3.2 | 9/10 → 3.6 |
| Scalability | 20% | 10/10 → 2.0 | 7/10 → 1.4 | 10/10 → 2.0 |
| Cost (Year 1) | 20% | $150k → 1.2 | $50k → 2.0 | $300k → 0.6 |
| Implementation risk | 10% | Risk 15 → 0.7 | Risk 10 → 0.9 | Risk 25 → 0.4 |
| Vendor viability | 10% | 10/10 → 1.0 | 9/10 → 0.9 | 6/10 → 0.6 |
| **Total** | **100%** | **8.5** | **8.4** | **7.2** |

### Recommended Solution

**Salesforce Commerce Cloud + POS (Tableau Retail)** — highest weighted score (8.5), strong functional fit and scalability, 6-month time to value, and enterprise-grade omnichannel support for 100+ stores.

### Trade-offs

- **Cost vs. scalability:** Salesforce costs more upfront but scales better.
- **Speed vs. customization:** Shopify deploys faster; Salesforce grows better.
- **Risk vs. control:** Custom microservices offer maximum control but high risk and negative NPV until year 4.

---

## Step IV: Feasibility and Risk Analysis

### Feasibility

- **Technical:** Cloud SaaS integrates via REST APIs; ETL migration from legacy SQL and Magento 1.9 is achievable with phased rollout.
- **Economic:** Positive NPV over 5 years; ROI from reduced stockouts and faster checkout.
- **Operational:** Staff upskilling feasible in 8 weeks; 9-month rollout aligns with seasonal cycles.

### Risk Register

| Risk | Probability | Impact | Score | Mitigation |
|---|---|---|---|---|
| Data migration loss | 3 | 4 | 12 | Two dry runs, checksum validation, rollback plan |
| Vendor outage | 2 | 5 | 10 | SLA 99.9%, offline POS mode, multi-region failover |
| User adoption resistance | 3 | 3 | 9 | Training, phased rollout, store champions |
| Integration complexity | 3 | 4 | 12 | API-first design, middleware, pilot in 5 stores |

### Mitigation Effectiveness

Dry runs and checksum validation protect data integrity. Vendor outage mitigations keep stores operational. Training and phased rollout reduce resistance. API-first design and a pilot reduce integration complexity. Together they keep the project on the 9-month timeline.

---

## Step V: Visualizations and Roadmap

### Artifacts

- **Process flow** for omnichannel checkout
- **Context diagram** (Level 0 DFD)
- **Level 0 DFD** (decomposed)
- **UML use case diagram** for the unified commerce system

### Results — How the Solution Addresses Pain Points

| Pain Point | Solution |
|---|---|
| Checkout delays | Modern POS ≤5s |
| Stockouts | Real-time inventory + automated reordering |
| Marketing fragmentation | 360° customer profile |
| Poor online experience | Page load <2s, unified cart, BOPIS |
| Limited scalability | Cloud platform scales to 100+ stores and 3× holiday traffic |

### Implementation Roadmap (9 Months)

| Milestone | Timeline | Description |
|---|---|---|
| Discovery & vendor selection | Month 1 | Finalize requirements, select Salesforce |
| Data migration planning & API design | Month 2 | Integration design, cloud setup |
| POS pilot in 5 stores | Month 3 | Test POS, inventory sync, checkout speed |
| E-commerce integration | Month 4 | Connect Magento replacement |
| Data migration dry run 1 | Month 5 | Validate data integrity, rollback |
| Data migration dry run 2 & BOPIS pilot | Month 6 | Second dry run; BOPIS pilot |
| Full POS rollout to 50 stores | Month 7 | Chain-wide deployment; staff training |
| Omnichannel features rollout | Month 8 | Unified cart, real-time inventory, 360° view |
| Performance tuning & security audit | Month 9 | Scale testing, GDPR, hypercare, expansion readiness |

---

## Author

**Andre Philip Nyanjahia**  
Full-Stack Systems Architect | Data Strategist

[GitHub](https://github.com/Andre-tech671) · [LinkedIn](https://linkedin.com/in/andre-nyanjahia-ab664228a)

---

## License

This repository is for educational and portfolio purposes.
