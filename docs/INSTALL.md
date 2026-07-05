<div align="center">

![Deskwise Installation](../assets/banners/banner-install.svg)

[← Back to README](../README.md) · [Features](./FEATURES.md) · [Pricing](./PRICING.md)

</div>

---

## System Requirements

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| OS | Windows 10 (64-bit) | Windows 11 |
| RAM | 4 GB | 8 GB |
| Storage | 10 GB free | 20 GB free |
| Display | 1280 × 720 | 1920 × 1080 |
| Internet | Optional | 10 Mbps+ for cloud sync |

---

## Installation

### Step 1 — Download

Get the latest release from GitHub or the Deskwise website:

- **GitHub:** https://github.com/xenexstudio/Deskwise-updates/releases/latest
- **Website:** https://deskwise.in/downloads

Download `deskwise_v2.0.2.zip`.

### Step 2 — Extract

```
Extract deskwise_v2.0.2.zip to:
  C:\Program Files\Deskwise      ← recommended
```

No installer is required. Deskwise runs directly from the extracted folder.

### Step 3 — Launch

Open the Deskwise folder and double-click `deskwise.exe`. The app initializes on first launch.

### Step 4 — Activate

> [!IMPORTANT]
> A valid license key from Xenex Studio is required. Contact [deskwise.xenex@gmail.com](mailto:deskwise.xenex@gmail.com) to obtain one.

1. Enter your **license key** when prompted
2. The app automatically binds to your device (hardware-linked)
3. Create your **administrator credentials**
4. Enter your school name, registration code, and academic year

### Step 5 — Initial Setup

- Configure grades and sections
- Set up fee structure and heads
- Add staff records
- Import or add students
- *(Optional)* Enable cloud sync under Settings

---

## Updating

### Auto-Update *(Recommended)*

When a new version is available, Deskwise prompts you to update.

1. Click **Update Now** in the prompt
2. The app downloads and applies the patch in the background
3. On next launch, database migrations run automatically — no action needed

### Manual Update

1. Download the latest `deskwise_vX.X.X.zip` from [Releases](https://github.com/xenexstudio/Deskwise-updates/releases/latest)
2. Back up your database: `Settings → Backup → Create Backup`
3. Close Deskwise completely
4. Extract the new files and overwrite the existing folder
5. Launch `deskwise.exe` — database migrates automatically

---

## Data Backup

### Manual Backup

Go to **Settings → Backup → Create Backup**

This creates an encrypted `.deskwise` backup file containing:
- Full AES-256 encrypted database
- All uploaded media and documents
- Automatic rotation — keeps last 3 backups

### Auto-Backup

Deskwise creates backups automatically:
- Daily, when the app is running and connected
- Before every update

### Restore

Go to **Settings → Backup → Restore**, select your backup file, and confirm. The app restarts with restored data.

> [!WARNING]
> Always move backup files to external storage (USB drive, external hard disk). Xenex is not responsible for backup files lost due to device failure, formatting, or accidental deletion.

---

## Command Line Options *(Advanced)*

```batch
:: Use a custom data directory
deskwise.exe --data-path="D:\SchoolData"

:: Enable debug logging
deskwise.exe --debug
```

---

## Troubleshooting

| Error | Resolution |
|-------|-----------|
| `License Not Found` | Verify your key is correct. Contact Xenex if lost. |
| `Device Not Registered` | Contact Xenex with your machine ID (shown in the error). |
| `Database Corrupted` | Restore from backup. If no backup exists, contact support. |
| `Sync Failed` | Check internet connection. Try manual sync later via Settings. |
| `Clock Tamper Detected` | System clock was moved backward — a security check. Contact Xenex. |

---

## Uninstalling

> [!CAUTION]
> Always back up your data before uninstalling. Data not backed up or synced to cloud will be permanently lost.

1. Create a backup: `Settings → Backup → Create Backup`
2. Delete the Deskwise application folder
3. *(Optional)* Delete `%APPDATA%\Deskwise` to remove app data
4. Remove any desktop shortcuts

---

## Support

| Channel | Details |
|---------|---------|
| Email | [deskwise.xenex@gmail.com](mailto:deskwise.xenex@gmail.com) |

---

<div align="center">

[← Back to README](../README.md) · [Features](./FEATURES.md) · [Pricing →](./PRICING.md)

*© 2024–2026 Xenex*

</div>
