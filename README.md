<div align="center">

![Deskwise](./assets/banners/banner-readme.svg)
[![Latest Release](https://img.shields.io/github/v/release/xenexstudio/Deskwise-updates?style=flat-square&color=2D6A4F&label=Latest)](https://github.com/xenexstudio/Deskwise-updates/releases/latest)

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-2D6A4F?style=flat-square&logo=windows&logoColor=white)](https://github.com/xenexstudio/Deskwise-updates/releases/latest)
[![License](https://img.shields.io/badge/License-Proprietary-1B4332?style=flat-square)](./LICENSE)

*A secure, offline-first school administration ecosystem — desktop app + web portal — purpose-built for Indian schools.*

[**Download**](https://github.com/xenexstudio/Deskwise-updates/releases/latest) · [Features](./docs/FEATURES.md) · [Installation](./docs/INSTALL.md) · [Pricing](./docs/PRICING.md)

</div>

---

> [!IMPORTANT]
> **A hardware-linked license key is required to run Deskwise.**
> Contact [deskwise.xenex@gmail.com](mailto:deskwise.xenex@gmail.com) or visit the website to get started.

---

## Key Highlights

### 🔒 Security & Data Privacy

- **AES-256 encrypted database** via SQLCipher — all data encrypted at rest
- **bcrypt password hashing** for local authentication
- **Hardware-bound licensing** — license keys are HMAC-signed and device-locked
- **Clock tamper detection** — prevents license manipulation
- **Remote device deactivation** — de-authorize devices from the cloud
- **Encrypted backups** — backup files are AES-256 encrypted with random IV
- **90-day audit trail** — every data change traced with user and timestamp via `audit_logs`
- **Granular role-based permissions** — 50+ permission keys, unique role constraints, JSON-driven

### 🌐 Offline-First & Cloud Architecture

- **Works completely offline** — no internet dependency for daily operations
- **Local SQLite database** encrypted with SQLCipher
- **Optional Supabase cloud sync** — push/pull data when connected
- **Conflict resolution** — timestamp-based sync with local-pending-change awareness
- **60-second connectivity detection** — auto-switches between online/offline modes
- **Per-row sync tracking** — every table has `is_synced` status
- **Pre-sync encrypted backups** — auto-backup before each sync cycle

### 📊 Comprehensive Academic Management

- **Full grading system** — configurable grade scales (A+, A, B, etc.) with GPA point mapping
- **GPA & CGPA** — configurable calculation (credit-weighted or unweighted, include/exclude optional subjects)
- **Marks entry & tabulation** — live calculation with lock/snapshot workflow
- **8 marksheet templates** — modern, visual, professional, print-ready, elegant, compact, classic, certificate
- **Transfer Certificate (TC)** templates — formal, modern, simple, professional
- **Character Certificate (CC)** templates — formal, classic, modern, elegant, professional
- **Promotion rules engine** — configurable pass/fail criteria, dynamic remark templates
- **Academic calendar events** — schedule and manage key academic dates

### 💰 Finance & Fee Management

- **Fee categories & invoices** — define fee structures, generate invoices
- **Payment tracking** — record and reconcile transactions
- **Scholarship management** — assign discounts and scholarships
- **Student credit/wallet system** — prepaid credit balance with transaction log
- **Expense tracking** — categories, expenses, asset register
- **Other income** — non-fee income tracking
- **Bulk billing** — generate invoices for entire classes or sections
- **Manual discount thresholds** — configurable approval-based discount limits with escalation

### 🚌 Transport & GPS

- **Vehicle fleet management** — register and track buses
- **Route & stop management** — define bus stops with GPS coordinates
- **Live GPS tracking** — real-time vehicle positions on interactive offline map
- **Route mapping** — polyline rendering with Google Polyline Algorithm
- **Geofencing** — configurable geo-radius for stop detection
- **Student assignment** — per-student bus and stop assignment

### 👥 Student & Staff Management

- **Complete student lifecycle** — admission, attendance, academics, fee records, exit
- **Student photo & document management** — encrypted image storage, document uploads
- **Bulk import/export** — CSV/Excel student data import/export
- **Staff directory** — employee records with assignment tracking
- **Staff web access** — invite staff to web portal with role-based access
- **Leave management** — staff leave requests and approval workflow
- **My Class (web)** — class teachers can view and edit student details inline

### 📋 Attendance

- **Daily attendance tracking** — student and staff with JSON-based records
- **GPS-verified staff attendance** — location-tagged clock-in via desktop app
- **Web attendance marking** — class teachers mark student attendance via web portal
- **Attendance reports** — configurable summaries and trend charts
- **Working days calculation** — auto-compute present/absent/working days per period

### ✅ Multi-Step Approval Workflow

- **Configurable multi-step approval rules** — define approver chains, step order
- **Threshold-based routing** — auto-route based on amount, type, or role
- **Delegation & escalation** — forward to next approver in chain
- **Decision tracking** — before/after change preview on every request
- **Covered actions:**
  - Student / staff deletion
  - Salary changes
  - Transport edits & deletions
  - Discount thresholds & scholarship approvals
  - Grading scale & GPA settings changes
  - Promotion rule & execution changes
  - Academic calendar events
- **Complete audit trail** — who requested, who approved/rejected, what changed

### 📱 Three-Tier Web Portal

- **Principal Dashboard** — KPIs, charts, attendance trends, finance analytics, recent activity
- **Staff Portal** — mark attendance, enter marks, manage my class, approvals, notices
- **Parent Portal** — view progress, fees, attendance (with Nepali calendar), exam results
- **Role-gated routes** — every page checked against granular 50+ permission set
- **Separate parent auth** — symbol-number-based login, no Supabase Auth needed

### 📋 Notices & Announcements

- **Full CRUD** — create, edit, pin/unpin, soft-delete with categories
- **Category system** — General, Holiday, Event, Academic, Urgent (color-coded)
- **Pinned notices** — stick to top of feed
- **Audit trail** — all mutations logged
- **Web & desktop** — visible across both platforms

### 🛡️ Role & Permission System

- **Role hierarchy:** `owner` > `developer` > `principal` > `admin` > `vice_principal` > `accountant` > `coordinator` > `staff`
- **Unique roles** — admin, vice_principal, accountant, coordinator (one per school)
- **50+ granular permission keys** stored as JSON in `school_roles`
- **Route-level gating** — every web route checked against permission map
- **Full bypass** — `owner` and `developer` roles skip permission checks
- **Staff enrichment** — class teacher flags, grade/section assignments auto-resolved on login

### 📡 Cloud Sync

- **Supabase-powered sync** — PostgreSQL backend with Row Level Security
- **Bidirectional sync** — push local changes, pull remote changes
- **File/media sync** — photos and documents synced to Supabase Storage
- **Sync management dashboard** — monitor sync status, force sync, view logs
- **Sync logs table** — full history of sync operations per school

### 🔧 Additional Features

- **Live CCTV viewing** — RTSP stream integration for school security cameras
- **Template-based document engine** — customizable PDF layouts for marksheets, certificates
- **Role-based dashboards** — personalized views for every role
- **Notifications** — role-targeted in-app alerts and web notifications
- **Activity log** — admin activities stored in Firebase Firestore
- **Lost & Found** — item tracking across web portal
- **ID Cards** — admit cards and school ID card generation

---

## 📸 Screenshots

*Drop your screenshots here — I'll list the filenames you need at the end.*

| Dashboard | Finance | Registry |
|:---:|:---:|:---:|
| ![Dashboard](assets/screenshots/dashboard.png) | ![Finance](assets/screenshots/finance.png) | ![Registry](assets/screenshots/registry.png) |

| Grading & Academics | Transport | Reports |
|:---:|:---:|:---:|
| ![Academics](assets/screenshots/grading.png) | ![Transport](assets/screenshots/transport.png) | ![Reports](assets/screenshots/report.png) |

| Attendance | CCTV | Settings |
|:---:|:---:|:---:|
| ![Attendance](assets/screenshots/attendance.png) | ![CCTV](assets/screenshots/cctv.png) | ![Settings](assets/screenshots/settings.png) |

> *Screenshots are placeholders. Replace with actual captures following the naming convention above.*

---

## 🌐 Web Portal

Deskwise includes a companion **Next.js web application** that extends the desktop app to browsers — enabling staff, principals, and parents to access key features from any device.

### Staff Portal (`/staff/*`)

| Page | Description | Permission |
|------|-------------|------------|
| **Dashboard** | Own attendance, pending leaves, assigned subjects, class overview | — |
| **My Class** | Student list with inline editor (roll no, DOB, blood group, address, etc.) | Class teacher only |
| **Student Attendance** | Mark Present/Absent/Late/Holiday per student, bulk actions, save | `student_attendance` |
| **Marks Entry** | Enter and manage exam marks | `aca_exams` |
| **Attendance** | View and mark own attendance | — |
| **Leave** | Apply for leave | — |
| **Approvals** | Review and decide on approval requests assigned to you | `_approve_any` |
| **Notices** | View school announcements | — |
| **Notifications** | Role-targeted alerts | — |
| **Lost & Found** | Track found items | — |
| **Settings** | Profile and preferences | — |

### Principal Portal (`/principal/*`)

| Page | Description | Permission |
|------|-------------|------------|
| **Dashboard** | KPIs, 6-month finance trend, attendance donut, students by grade, staff breakdown, grade/subject performance, 14-day attendance trend | — |
| **School Info** | View/edit school details | — |
| **Students** | Full student management | `reg_admission` |
| **Attendance** | Student attendance overview | `student_attendance` |
| **Staff Attendance** | Staff attendance overview | `staff_attendance` |
| **Academic** | Subjects by grade, staff list, grade scores | `aca_exams` |
| **Exams** | Exam setup and management | `exam_setup` |
| **Finance** | Fee management, invoices, transactions | `finance` |
| **Approvals** | Full approval center (same engine as staff) | `_approve_any` |
| **Notices** | Create, edit, pin, delete announcements | — |
| **Notifications** | Compose and send notifications | — |
| **Staff Access** | Assign web roles, invite staff, revoke access | `manage_staff_web_access` |
| **Leave Requests** | View and manage staff leave requests | — |
| **My Attendance** | Mark own attendance | — |
| **Leave** | Apply for leave | — |
| **Activities** | Admin activity audit log (Firebase) | — |
| **ID Cards** | Admit cards and ID card generation | `admit_cards` |
| **Lost & Found** | Item tracking | — |
| **Settings** | Profile, security, general, academic, notification, ID card settings | `settings` (some) |

### Parent Portal (`/parent/*`)

| Tab | Description |
|-----|-------------|
| **Overview** | Student info card, guardian details, quick stats (symbol no, blood group, bus stop) |
| **Fees** | Outstanding/total billed/scholarship, invoice detail lines, payment history, filters |
| **Attendance** | Summary cards + Nepali (BS) calendar grid with status-colored day cells |
| **Progress** | Exam results: percentage, grade, rank, GPA, subject-wise marks with grade letters |

### Admin Portal (`/admin/*`)

| Page | Description |
|------|-------------|
| **Dashboard** | Xenex Studio admin: schools, licenses, sync status at a glance |
| **Schools** | Manage registered schools, license assignment, feature overrides |
| **Devices** | Device registry and remote deactivation |
| **Onboarding** | School onboarding requests and approval |
| **Plan Features** | Per-plan feature configuration |
| **Sync Logs** | Cross-school sync operation logs |
| **Data Browser** | Raw table inspection and developer tools |
| **Contact Messages** | Website contact form submissions |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Desktop Framework** | Flutter (Dart) — desktop-first |
| **Web Framework** | Next.js (React) — responsive web portal |
| **Local Database** | SQLite via `sqflite_common_ffi` |
| **Database Encryption** | SQLCipher (AES-256) via `sqlcipher_library_windows` |
| **Cloud Backend** | Supabase (PostgreSQL + Auth + Storage + RPC) |
| **Desktop State** | Provider |
| **Auth (Web)** | Supabase Auth (staff/principal) + Custom RPC (parent) |
| **PDF Generation** | `pdf` + `printing` packages (desktop) |
| **Charts** | `fl_chart` (desktop), Recharts (web) |
| **Secure Storage** | `flutter_secure_storage` |
| **Encryption** | `dbcrypt` (bcrypt), `encrypt` (AES-256), `crypto` (HMAC/SHA-256) |
| **Sync** | Custom bidirectional sync engine |
| **Maps** | `flutter_map` + OpenStreetMap |
| **Audit** | `audit_logs` table (Supabase) + Firebase Firestore (admin activities) |
| **Notifications** | Firebase Cloud Messaging |

---

## System Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                    Deskwise Desktop App                        │
├──────────────────────────────────────────────────────────────┤
│                        Flutter / Dart                          │
├──────────────┬───────────────────────────┬────────────────────┤
│  Local Mode  │    Sync Engine            │  Online Mode       │
│  (Offline)   │  (Bidirectional Push/Pull)│  (Connected)       │
├──────────────┴───────────────────────────┴────────────────────┤
│              SQLCipher Encrypted SQLite                        │
│              (AES-256 at rest)                                 │
├──────────────────────────────────────────────────────────────┤
│                    Windows 10 / 11 (64-bit)                    │
└─────────────────────────┬────────────────────────────────────┘
                          │ Sync (Supabase REST)
                          ▼
┌──────────────────────────────────────────────────────────────┐
│                       Supabase Cloud                          │
├──────────────────────────────────────────────────────────────┤
│  PostgreSQL DB  │  Auth  │  Storage  │  RPC / Edge Functions │
└─────────────────────────┬────────────────────────────────────┘
                          │ PostgreSQL (same schema)
                          ▼
┌──────────────────────────────────────────────────────────────┐
│                 Deskwise Web Portal (Next.js)                  │
├──────────────────────────────────────────────────────────────┤
│                   React / Next.js 14 (App Router)              │
├──────────────┬───────────────────┬───────────┬───────────────┤
│  /principal  │    /staff         │  /parent  │  /admin       │
│  (Principal) │  (Staff Portal)   │(Parent)   │ (Xenex Admin) │
└──────────────┴───────────────────┴───────────┴───────────────┘
```
```

---

## 📦 Current Release — v2.0.6+25

| Property | Details |
| :--- | :--- |
| **Version** | `v2.0.6+25` · Stable |
| **Platform** | Windows 10 / 11 (64-bit) |
| **Framework** | Flutter |
| **Database** | SQLite + SQLCipher (AES-256) |
| **Cloud** | Supabase |
| **Released** | May 2026 |

**What's new in v2.0.6:**
- 🛡️ **Security Hardening:** Enhanced license verification and fail-closed security guards.
- 📉 **Due Report Stability:** Fixed critical crashes during PDF exports and added diagnostic auditing.
- 🎨 **UI Polish:** Improved sidebar behavior in Fee Billing and streamlined print workflows.
- 🚀 **Performance:** General stability refinements across all core modules.

[→ Full release notes](https://github.com/xenexstudio/Deskwise-updates/releases/latest)

---

## Module Overview

### Core Desktop Modules

| Module | Description |
|--------|-------------|
| **Auth** | License activation, login (offline + Supabase), device registration |
| **Dashboard** | Main overview with key metrics, secondary dashboard for CCTV/GPS/updates |
| **Students** | Full student lifecycle management — admission, records, documents, exit |
| **Staff** | Employee records, assignments, qualifications, contracts |
| **Academic** | Subjects, grading scales, tabulation, GPA/CGPA, promotion rules |
| **Exams** | Exam scheduling, marks entry, results, report cards |
| **Attendance** | Student & staff daily attendance with GPS verification |
| **Finance** | Fees, invoices, transactions, scholarships, expenses, assets, wallet |
| **Transport** | Vehicle fleet, routes, live GPS tracking, geofencing |
| **Reports** | PDF marksheets (8 styles), TC (4 styles), CC (5 styles) |
| **Settings** | School config, roles/permissions, document templates, GPA policy |
| **Sync** | Cloud data synchronization with Supabase |
| **Approvals** | Multi-step approval workflow engine |
| **Leave** | Staff leave management |
| **CCTV** | Live camera streaming via RTSP |

### Web Portal Modules

| Module | Description |
|--------|-------------|
| **Principal Dashboard** | KPIs, charts, analytics, activity feed |
| **Staff Portal** | My class, attendance marking, marks entry, approvals, notices |
| **Parent Portal** | Overview, fees, attendance (BS calendar), progress/exam results |
| **Approval Center** | Multi-step approval with before/after preview (web) |
| **Notices** | Full CRUD with categories, pinning, soft-delete |
| **Notifications** | Role-targeted in-app alerts and push notifications |
| **Staff Access** | Role assignment, invites, revoke web access |
| **Activities** | Admin activity audit log |
| **School Settings** | Profile, security, academic, ID card settings |
| **ID Cards** | Admit cards and school ID cards |
| **Lost & Found** | Item tracking |
| **Admin Panel** | School management, device registry, onboarding, licenses, sync logs |

---

## ⚡ Quick Start

```text
1. Download  →  deskwise_v2.0.6+25.zip from Releases
2. Extract   →  to C:\Program Files\Deskwise
3. Launch    →  deskwise.exe
4. Activate  →  enter your license key from Xenex
5. Configure →  school name, grades, fee structure, staff
```

[→ Full installation guide](./docs/INSTALL.md)

---

## 📚 Documentation

| Doc | Description |
| :--- | :--- |
| [📋 Features](./docs/FEATURES.md) | Full module breakdown and roadmap |
| [📥 Installation](./docs/INSTALL.md) | Setup, activation, updates, backup |
| [💰 Pricing](./docs/PRICING.md) | Plans from Foundation to Enterprise |
| [🔒 Security Policy](./SECURITY.md) | Encryption, licensing, vulnerability reporting |

---

## 🎯 Why Deskwise?

| Feature | Deskwise | Typical alternatives |
| :--- | :---: | :---: |
| Works without internet | ✅ Full offline | ❌ Cloud-only |
| AES-256 local encryption | ✅ Hardware-bound key | ❌ Unencrypted |
| Hardware-linked license | ✅ Built-in | ❌ Rarely available |
| CCTV integration | ✅ DVR + IP cameras | ❌ Not available |
| GPS transport tracking | ✅ Offline map | ⚠️ Paid add-on |
| Certificate templates | ✅ 9 templates | ⚠️ 1–2 basic |
| Payroll accuracy | ✅ Attendance-linked | ❌ Manual |
| Silent auto-updates | ✅ Over-the-air | ❌ Manual reinstall |

---

## Licensing & Plans

| Feature | Basic | Medium | Premium |
|---------|-------|--------|---------|
| Core school management | ✅ | ✅ | ✅ |
| Students & staff limit | Limited | Extended | Unlimited |
| Custom branding colors | ❌ | ✅ | ✅ |
| Template layouts | Standard | All | All + Custom |
| Cloud sync | ✅ | ✅ | ✅ |
| Max devices | Per plan | Per plan | Per plan |
| Priority support | ❌ | ❌ | ✅ |

---

## Database

42 tables organized across 16 schema files, covering all school operations from admissions to alumni, fully encrypted with SQLCipher AES-256.

---

## 📞 Contact

| Channel | Information |
| :--- | :--- |
| 📧 **Email** | [deskwise.xenex@gmail.com](mailto:deskwise.xenex@gmail.com) |

---

<div align="center">

*© 2024–2026 Xenex · Built for Indian schools, for Indian education*

</div>
