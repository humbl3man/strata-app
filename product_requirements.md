# 🏠 Strata – Product Requirements Document

**Version:** 1.0  
**Author:** Konstantin  
**Date:** 2025-07-15

---

## 📌 1. Purpose

**Strata** is a simple, modern SaaS platform for small to mid-sized homeowner associations (HOAs) to manage residents, dues, documents, and communication — without bloated enterprise software or third-party property managers.

The goal is to help volunteer-run HOAs operate more efficiently with minimal tech knowledge, at an affordable price.

---

## 🎯 2. Target Users

**Primary Users:**

- HOA board members (President, Treasurer, Secretary, etc.)
- Residents/homeowners

**User Segments:**

- Small to mid-sized HOAs (20–150 units)
- Mostly self-managed
- Located in the U.S., with monthly or quarterly dues

---

## 🧩 3. Key Features (MVP Scope)

### 3.1 Resident Management

- Add/edit/remove homeowners
- View list of residents with unit/address, name, email
- Assign board roles (President, Treasurer, etc.)

### 3.2 Dues & Payments

- Define dues frequency (monthly, quarterly)
- Enable online payments via Stripe (ACH & credit card)
- View payment history per homeowner
- Send automated email reminders for upcoming and late payments
- Board members can export payment history as CSV

### 3.3 Document Library

- Upload and categorize documents (PDF, DOCX)
- Organize by folder or type (CC&Rs, Budgets, Meeting Minutes)
- Access controlled by role (e.g., resident vs. board-only)

### 3.4 Announcements

- Board members can post announcements
- Optional email broadcast when announcement is posted
- Basic WYSIWYG editor for formatting

---

## 🧠 4. Out of Scope (for MVP)

These features may be added in later phases:

- Voting & surveys
- Violation logging
- Maintenance request tracking
- SMS messaging
- Full accounting features
- Tenant (non-owner) support

---

## 🛠️ 5. Technical Requirements

| Area         | Tooling                        |
| ------------ | ------------------------------ |
| Frontend     | SvelteKit or Next.js           |
| Backend      | Supabase or Postgres + Drizzle |
| Auth         | Lucia or Clerk/Auth.js         |
| File Storage | Supabase Storage or S3         |
| Payments     | Stripe (ACH + card support)    |
| Emails       | Resend or Postmark             |
| Hosting      | Vercel / Render / Railway      |

---

## 👥 6. User Roles

### 6.1 Resident

- View personal payment history
- View documents and announcements
- Update contact info

### 6.2 Board Member

- All resident privileges
- Add/edit residents
- Manage dues
- Post announcements
- Upload documents
- View/export payment reports

---

## 📊 7. Success Metrics

| Goal         | Metric                           |
| ------------ | -------------------------------- |
| Adoption     | 10 paying HOAs in first 3 months |
| Retention    | 90% of HOAs use platform monthly |
| Activation   | Time-to-first-payment < 5 days   |
| Support Load | <2 support tickets per HOA/month |

---

## 📆 8. Timeline (60-Day MVP Plan)

| Week | Deliverable                                     |
| ---- | ----------------------------------------------- |
| 1    | Mockups, project structure, Supabase setup      |
| 2    | Auth + basic user roles                         |
| 3    | Resident directory CRUD                         |
| 4    | Document upload and list view                   |
| 5    | Stripe payment integration + testing            |
| 6    | Email reminder system                           |
| 7    | Announcements + UI polish                       |
| 8    | Landing page, Stripe subscriptions, launch beta |

---

## 🚧 9. Known Risks

- HOAs vary in how they operate — flexibility will be key
- Legal compliance (e.g., e-payment laws, document retention) varies by state
- Residents may resist new tech if they’re older / less tech-savvy

---
