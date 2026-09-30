# System Design Projects

A collection of system design projects covering stakeholder analysis, SDLC selection, architecture patterns, and full technical documentation. Built as part of my Systems Design coursework and personal practice.

---

## Purpose

This repository serves as a portfolio of my system design work. Each project demonstrates the full lifecycle of system analysis and design — from identifying stakeholders and system components to selecting an SDLC model, designing the architecture, and documenting the final solution.

---

## Projects

| # | Project | Focus | SDLC Model | Architecture | Status |
|---|---|---|---|---|---|
| 1 | Crusty Muse Bakery | Online ordering system for a small bakery | Agile | 2-Tier (Client-Server) | ✅ Complete |
| 2 | Coming soon | — | — | — | 🔄 In Progress |

---

## Skills Demonstrated

- **Stakeholder Analysis** — Identifying and documenting key stakeholders and their roles
- **System Components** — Mapping inputs, processes, and outputs for system use cases
- **SDLC Selection** — Choosing and justifying the right software development lifecycle model
- **Architecture Design** — Designing and documenting system architecture with flow explanations
- **Technical Documentation** — Writing clear, structured project summaries and design decisions
- **Diagramming** — Creating system architecture diagrams and flowcharts

---

## Repository Structure
system-design-projects/
├── README.md
├── assets/
│ └── system-design-cover.png
└── projects/
├── 01-crusty-muse-bakery/
│ ├── README.md
│ ├── system-architecture-diagram.png
│ └── Final_Project_Bakery_Shop.docx
└── 02-next-project/
└── ...

---

## Author

**Andre Philip Nyanjahia**
Full-Stack Systems Architect | Data Strategist
[GitHub](https://github.com/Andre-tech671) · [LinkedIn](https://linkedin.com/in/andre-nyanjahia-ab664228a)

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

The bakery needs a simple digital system that supports **20–30 orders per day**, is easy to maintain, and fits a small budget.

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

## Task 5: Project Summary

| Category | Details |
|---|---|
| **Business Problem** | Crusty Muse Bakery currently accepts orders only in person or by phone. This results in delays, manual mistakes, and lost sales because customers cannot order online. The bakery needs a simple digital system that allows customers to place orders online and helps staff track them easily. |
| **System Goal** | To provide a simple, mobile-friendly online ordering system where customers can browse items, add them to a cart, and place orders, while bakery staff can view and update order status. The system must be low-cost, easy to maintain, and support 20–30 orders per day. |
| **Technical Choices — SDLC Model** | **Agile** — allows the bakery to build the system in small parts and adjust it based on feedback. Requirements may change as the bakery tests what works best. Agile avoids expensive rework and supports small-budget, fast-iteration development. |
| **Technical Choices — Architecture Pattern** | **2-Tier (Client-Server)** — simple, cost-effective, and easy to maintain. The client (web browser) handles the UI, while the server manages business logic and the database. The traffic (20–30 orders/day) is small enough that a more complex 3-tier architecture is unnecessary. |

---

# Project 2: Coming Soon

This project is currently in progress. Check back soon for updates.

---

## License

This repository is for educational and portfolio purposes.

---

## Author

**Andre Philip Nyanjahia**
Full-Stack Systems Architect | Data Strategist
[GitHub](https://github.com/Andre-tech671) · [LinkedIn](https://linkedin.com/in/andre-nyanjahia-ab664228a)
