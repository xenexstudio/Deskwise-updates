<div align="center">

![Deskwise Features](../assets/banners/banner-features.svg)

[← Back to README](../README.md) · [Installation](./INSTALL.md) · [Pricing](./PRICING.md)

</div>

---

## Core Modules

### 🎓 Registry — Student & Staff

Complete institutional records, always at your fingertips.

**Students**
- Full admission profiles — photos, guardian contacts, emergency info, document storage
- Digital admission forms and enrollment tracking
- Transfer requests and processing
- Live enrollment analytics by grade, gender, and section

**Staff**
- Qualification records, contracts, attendance history, leave tracking
- Role-based access tied to staff profiles

---

### 💰 Finance

Stop the leakage. Full visibility into every rupee.

- **Fee structure** — class-wise fee heads, custom configurations
- **Invoicing** — auto-generated bills and receipts on every payment
- **Scholarships** — automatic discounts and waiver management
- **Due alerts** — outstanding dues flagged automatically, no manual chasing
- **Expenses** — expenditure tracking, category-wise reports
- **Wallet system** — staff advances and salary deductions
- **Reports** — income/expenditure summaries, collection analytics

---

### 📚 Academics — Exams & Marks

From marks entry to printed certificates, fully automated.

- **Subjects** — per grade/section management, teacher assignments
- **Grading scales** — customizable GPA ranges, symbols, credit hours
- **Marks entry** — bulk CSV import, per-student or class-wise entry
- **Report cards** — auto-generated marksheets with GPA calculation
- **Exam schedules** — timetables, seating plans, admit cards
- **Certificates** — 9 professionally designed templates (TC, character, bonafide, and more), PDF export in one click

---

### 👨‍💼 Staff Management & Payroll

Payroll that trusts data, not memory.

- **Attendance** — daily mark-in/mark-out, class-wise trend charts
- **Leave management** — request workflow, approval tracking
- **Payroll** — automatic PL/LWP calculation from attendance data
- **Performance** — staff ranking and evaluation tracking
- Every calculation logged in the 90-day audit trail

---

### 🚌 Transport & GPS

Complete visibility over your fleet — even without internet.

- **Routes & stops** — define routes, assign pickup points
- **Fleet management** — bus assignment, capacity tracking
- **Student assignment** — per-student bus and stop records
- **Offline GPS map** — live fleet visualization using cached map tiles, no connectivity required

---

### 📷 CCTV & Dashboard

Bring your campus security into Deskwise.

- **Live camera feeds** — DVR and IP camera integration
- **Secondary dashboard** — multi-monitor support for reception/admin desks
- **Real-time stats** — live student count, today's attendance, collections at a glance

> [!NOTE]
> Deskwise provides the viewer interface only. Cameras and recording hardware remain the school's property and responsibility. No CCTV data is stored on Deskwise servers.

---

### ☁️ Cloud Sync

Offline-first — but smarter when you're online.

- **Offline-first** — full operations without internet, always
- **Smart sync** — only changed data is transmitted, not full snapshots
- **Conflict resolution** — last-write-wins with timestamp logic preserving data integrity
- **Multi-device** — sync across licensed devices on the same plan
- **Row-level security** — Supabase RLS ensures each school's data is fully isolated

---

### 🔒 Security & Licensing

Enterprise-grade protection for sensitive institutional data.

| Feature | Protection |
|---------|-----------|
| **SQLCipher** | AES-256 encrypted local database, hardware-bound key |
| **Hardware lock** | License tied to machine UUID — prevents unauthorized use |
| **Role-based access** | Principal, Admin, Staff — granular permission layers |
| **Audit trail** | 90-day log of every action, with timestamp and user identity |
| **Supabase RLS** | Cloud-side row-level security, no cross-school data access |
| **Encrypted sync** | All sync traffic encrypted end-to-end |

---

## Technical Specifications

| Property | Value |
|----------|-------|
| Platform | Windows 10 / 11 (64-bit) |
| Framework | Flutter |
| Database | SQLite + SQLCipher |
| Cloud backend | Supabase |
| Encryption | AES-256 |
| License | Hardware-bound per institution |
| Updates | Over-the-air, silent background patches |

---

## Roadmap

Features currently in development or planned:

| Feature | Status |
|---------|--------|
| Mobile app (Android & iOS) | 🔨 Coming soon |
| Parent portal (web dashboard) | 🎨 In design |
| GPS live tracking for parents | 🔨 In development |
| Automated absence alerts | 📋 Planned |
| AI-powered analytics & forecasting | 📋 Planned |
| Multi-school super-admin dashboard | 🗺️ Roadmap |

---

<div align="center">

[← Back to README](../README.md) · [Installation →](./INSTALL.md)

*© 2024–2026 Xenex*

</div>
