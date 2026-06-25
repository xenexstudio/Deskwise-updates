<div align="center">

![Deskwise](./assets/banners/banner-readme.svg)

[![Latest Release](https://img.shields.io/github/v/release/Trehive/stusync-patches?style=flat-square&color=2D6A4F&label=Latest)](https://github.com/Trehive/stusync-patches/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-2D6A4F?style=flat-square&logo=windows&logoColor=white)](https://github.com/Trehive/stusync-patches/releases/latest)
[![License](https://img.shields.io/badge/License-Proprietary-1B4332?style=flat-square)](./LICENSE)

*A secure, offline-first desktop application for comprehensive school administration in the Indian subcontinent.*

[**Download**](https://github.com/Trehive/stusync-patches/releases/latest) · [Features](./docs/FEATURES.md) · [Installation](./docs/INSTALL.md) · [Pricing](./docs/PRICING.md)

</div>

---

> [!IMPORTANT]
> **A hardware-linked license key is required to run Deskwise.**
> Contact [deskwise@xenex.dev](mailto:deskwise@xenex.dev) or visit the website to get started.

---

## Key Highlights

### 🔒 Security & Data Privacy

- **AES-256 encrypted database** via SQLCipher — all data encrypted at rest
- **bcrypt password hashing** for local authentication
- **Hardware-bound licensing** — license keys are HMAC-signed and device-locked
- **Clock tamper detection** — prevents license manipulation
- **Remote device deactivation** — de-authorize devices from the cloud
- **Encrypted backups** — backup files are AES-256 encrypted with random IV
- **Audit logging** — every data change traced with user and timestamp
- **Multi-tier permissions** — owner, principal, admin, staff with granular JSON permissions

### 🌐 Offline-First Architecture

- **Works completely offline** — no internet dependency for daily operations
- **Local SQLite database** encrypted with SQLCipher
- **Optional Supabase cloud sync** — push/pull data when connected
- **Conflict resolution** — timestamp-based sync with local-pending-change awareness
- **60-second connectivity detection** — auto-switches between online/offline modes
- **Pre-sync encrypted backups** — auto-backup before each sync cycle

### 📊 Comprehensive Academic Management

- **Full grading system** — configurable grade scales (A+, A, B, etc.) with GPA point mapping
- **GPA & CGPA** — configurable calculation (credit-weighted or unweighted, include/exclude optional subjects)
- **Marks entry & tabulation** — live calculation with lock/snapshot workflow
- **8 marksheet templates** — modern, visual, professional, print-ready, elegant, compact, classic, certificate
- **Transfer Certificate (TC)** templates — formal, modern, simple, professional
- **Character Certificate (CC)** templates — formal, classic, modern, elegant, professional
- **Promotion rules engine** — configurable pass/fail criteria, dynamic remark templates

### 💰 Finance & Fee Management

- **Fee categories & invoices** — define fee structures, generate invoices
- **Payment tracking** — record and reconcile transactions
- **Scholarship management** — assign discounts and scholarships
- **Student credit/wallet system** — prepaid credit balance with transaction log
- **Expense tracking** — categories, expenses, asset register
- **Other income** — non-fee income tracking
- **Bulk billing** — generate invoices for entire classes or sections
- **Manual discount thresholds** — configurable approval-based discount limits

### 🚌 Transport Module

- **Vehicle fleet management** — register and track buses
- **Route & stop management** — define bus stops with GPS coordinates
- **Live GPS tracking** — real-time vehicle positions on interactive map
- **Route mapping** — polyline rendering with Google Polyline Algorithm
- **Geofencing** — configurable geo-radius for stop detection

### 👥 Student & Staff Management

- **Complete student lifecycle** — admission, attendance, academics, fee records, exit
- **Student photo & document management** — encrypted image storage, document uploads
- **Bulk import/export** — CSV/Excel student data import
- **Staff directory** — employee records with assignment tracking
- **Staff web access** — invite staff to web portal with role-based access
- **Leave management** — staff leave requests and approval workflow

### 📋 Attendance

- **Daily attendance tracking** — student and staff with JSON-based records
- **GPS-verified staff attendance** — location-tagged clock-in
- **Attendance reports** — configurable attendance summaries
- **Working days calculation** — auto-compute present/absent/working days

### ✅ Approval Workflow

- **Configurable multi-step approval rules** — chain of approvers
- **Threshold-based approvals** — auto-route based on amount/type
- **Delegation & escalation** — forward or escalate approval requests
- **Complete audit trail** — who requested, who approved, when

### 📡 Cloud Sync

- **Supabase-powered sync** — PostgreSQL backend with Row Level Security
- **Bidirectional sync** — push local changes, pull remote changes
- **Per-row sync tracking** — every table has `is_synced` status
- **File/media sync** — photos and documents synced to Supabase Storage
- **Sync management dashboard** — monitor sync status, force sync, view logs
- **Role-gated sync** — only authorized roles can trigger data sync

### 🔧 Additional Features

- **Live CCTV viewing** — RTSP stream integration for school security cameras
- **Template-based document engine** — customizable PDF layouts for marksheets, certificates
- **Multiple display formats** — marks-only, GPA-only, or both on report cards
- **Role-based dashboards** — personalized views for owner, principal, admin, staff
- **Audit logs** — track all data modifications with user attribution
- **In-app notification system** — role-targeted alerts

---

## 📸 Screenshots

*Drop your screenshots here — I'll list the filenames you need at the end.*

| Dashboard | Finance | Registry |
|:---:|:---:|:---:|
| ![Dashboard](assets/screenshots/dashboard.png) | ![Finance](assets/screenshots/finance.png) | ![Registry](assets/screenshots/registry.png) |

| Academics | Transport | Reports |
|:---:|:---:|:---:|
| ![Academics](assets/screenshots/academics.png) | ![Transport](assets/screenshots/transport.png) | ![Reports](assets/screenshots/reports.png) |

| Attendance | CCTV | Cloud Sync |
|:---:|:---:|:---:|
| ![Attendance](assets/screenshots/attendance.png) | ![CCTV](assets/screenshots/cctv.png) | ![Cloud Sync](assets/screenshots/cloud-sync.png) |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | Flutter (Dart) — desktop-first |
| **Local Database** | SQLite via `sqflite_common_ffi` |
| **Database Encryption** | SQLCipher (AES-256) via `sqlcipher_library_windows` |
| **Cloud Backend** | Supabase (PostgreSQL + Auth + Storage + RPC) |
| **State Management** | Provider |
| **PDF Generation** | `pdf` + `printing` packages |
| **Charts** | `fl_chart` |
| **Secure Storage** | `flutter_secure_storage` |
| **Encryption** | `dbcrypt` (bcrypt), `encrypt` (AES-256), `crypto` (HMAC/SHA-256) |
| **Sync** | Custom bidirectional sync engine |
| **Maps** | `flutter_map` + OpenStreetMap |

---

## System Architecture

```
┌──────────────────────────────────────────────────────────┐
│                     Deskwise Desktop App                   │
├──────────────────────────────────────────────────────────┤
│                    Flutter / Dart                          │
├──────────────┬───────────────────────────┬────────────────┤
│  Local Mode  │    Sync Engine            │  Online Mode   │
│  (Offline)   │  (Bidirectional Push/Pull)│  (Connected)   │
├──────────────┴───────────────────────────┴────────────────┤
│              SQLCipher Encrypted SQLite                    │
│              (AES-256 at rest)                             │
├──────────────────────────────────────────────────────────┤
│                   Windows / macOS                          │
└──────────────────────────────────────────────────────────┘
                        ↕ Sync
┌──────────────────────────────────────────────────────────┐
│                    Supabase Cloud                          │
├──────────────────────────────────────────────────────────┤
│  PostgreSQL DB  │  Auth  │  Storage  │  Edge Functions   │
└──────────────────────────────────────────────────────────┘
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

[→ Full release notes](https://github.com/Trehive/stusync-patches/releases/latest)

---

## Module Overview

| Module | Description |
|--------|-------------|
| **Auth** | License activation, login (offline + Supabase), device registration |
| **Dashboard** | Main overview with key metrics, secondary dashboard for CCTV/GPS/updates |
| **Students** | Full student lifecycle management |
| **Staff** | Employee records, assignments, web access |
| **Academic** | Subjects, grading, tabulation, GPA/CGPA |
| **Exams** | Exam scheduling, marks entry, results, reports |
| **Attendance** | Student & staff daily attendance with GPS verification |
| **Finance** | Fees, invoices, transactions, scholarships, expenses, assets |
| **Transport** | Vehicle fleet, routes, live GPS tracking |
| **Reports** | PDF marksheets (8 styles), TC, Character Certificates |
| **Settings** | School config, roles/permissions, document templates, GPA policy |
| **Sync** | Cloud data synchronization with Supabase |
| **Approvals** | Multi-step approval workflow engine |
| **Leave** | Staff leave management |
| **CCTV** | Live camera streaming via RTSP |

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
| 📧 **Email** | [deskwise@xenex.dev](mailto:deskwise@xenex.dev) |

---

<div align="center">

*© 2024–2026 Xenex · Built for Indian schools, for Indian education*

</div>
