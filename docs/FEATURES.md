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

- **Attendance** — daily mark-in/mark-out, class-wise trend charts, GPS-verified clock-in
- **Leave management** — request workflow, approval tracking
- **Payroll** — automatic PL/LWP calculation from attendance data
- **Performance** — staff ranking and evaluation tracking
- **Web access** — invite staff to web portal with role-based access
- **Class teacher management** — per-teacher grade/section assignment
- Every calculation logged in the 90-day audit trail

---

### 🚌 Transport & GPS

Complete visibility over your fleet — even without internet.

- **Routes & stops** — define routes, assign pickup points
- **Fleet management** — bus assignment, capacity tracking
- **Student assignment** — per-student bus and stop records
- **Offline GPS map** — live fleet visualization using cached map tiles, no connectivity required

---

### ✅ Multi-Step Approval Workflow

Configurable, auditable decisions for sensitive operations.

- **Multi-step chains** — define approver sequences with step order
- **Threshold-based routing** — auto-route requests based on amount, action type, or role
- **Before/after preview** — reviewers see exactly what changed before deciding
- **Covered actions:** student/staff deletion, salary changes, transport edits, discount thresholds, scholarship discounts, grading scale updates, promotion settings, calendar events
- **Escalation & forwarding** — requests progress through the chain automatically
- **Audit trail** — every decision logged with timestamp, actor, and remarks

---

### 🌐 Web Portal — Staff

Empower your team from any device.

- **My Class** — view and edit student details (roll no, DOB, address, blood group, etc.)
- **Student Attendance** — mark Present/Absent/Late/Holiday, bulk actions, save
- **Marks Entry** — enter and manage exam marks
- **Own Attendance** — view and mark daily attendance
- **Leave** — apply for leave
- **Approvals** — approve or reject requests assigned to you
- **Notices & Notifications** — stay informed
- **Dashboard** — personal KPIs, pending tasks, class overview

### 🌐 Web Portal — Principal

Full school oversight from the web.

- **Dashboard** — KPIs, finance trends, attendance analytics, grade/subject performance
- **Students** — manage admissions and records
- **Attendance** — student and staff attendance overview
- **Academic** — subjects by grade, staff list, grade scores
- **Exams & Finance** — exam setup and fee management
- **Approvals** — full approval center
- **Notices** — create, edit, pin, delete announcements
- **Staff Access** — assign web roles, invite, revoke
- **Leave Requests** — manage staff leave
- **Activities** — admin activity audit log
- **Settings** — profile, security, academic, ID card config

### 🌐 Web Portal — Parent

Stay connected to your child's education.

- **Overview** — student info, guardian details, quick stats
- **Fees** — invoices, payment history, outstanding amounts
- **Attendance** — summary cards + Nepali (BS) calendar grid
- **Progress** — exam results with percentages, grades, GPA, and rank

### 🛡️ Role-Based Permissions

Granular control over who can access what.

- **Role hierarchy:** owner → developer → principal → admin → vice_principal → accountant → coordinator → staff
- **50+ permission keys** stored as JSON in `school_roles`
- **Unique roles** — admin, vice_principal, accountant, coordinator (one per school)
- **Full-bypass roles** — owner and developer skip all checks
- **Route-level enforcement** — every web page verified against permission map
- **Staff enrichment** — class teacher flags, grade/section auto-resolved on login

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
| Platform | Windows 10 / 11 (64-bit) + Web (all browsers) |
| Desktop Framework | Flutter (Dart) |
| Web Framework | Next.js 14 (React) |
| Database | SQLite + SQLCipher (desktop), PostgreSQL / Supabase (cloud) |
| Cloud backend | Supabase (PostgreSQL + Auth + Storage + RPC) |
| Encryption | AES-256 (SQLCipher + backup files) |
| Auth (web) | Supabase Auth (staff/principal) + Custom RPC (parent) |
| License | Hardware-bound per institution |
| Updates | Over-the-air, silent background patches |

---

## Roadmap

Features currently in development or planned:

| Feature | Status |
|---------|--------|
| Mobile app (Android & iOS) | 🔨 Coming soon |
| GPS live tracking for parents | 🔨 In development |
| Automated absence alerts (SMS/email) | 📋 Planned |
| AI-powered analytics & forecasting | 📋 Planned |
| Multi-school super-admin dashboard | 🗺️ Roadmap |
| Online fee payments (parent portal) | 🎨 In design |
| Timetable & seating plan generator | 📋 Planned |
| Library management module | 🗺️ Roadmap |
| Hostel management module | 🗺️ Roadmap |

---

<div align="center">

[← Back to README](../README.md) · [Installation →](./INSTALL.md)

*© 2024–2026 Xenex*

</div>
