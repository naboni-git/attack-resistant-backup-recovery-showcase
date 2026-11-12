# Attack-Resistant Backup and Recovery System (ARBR)

A showcase repository for the ARBR project. 

**An automated system for detecting attacks, protecting backups, and enabling secure recovery.**

## 🔗 Source Code
The full source code, commit history, and complete team contributions are hosted on the original project repository:

👉 **[View the ARBR Source Code on GitHub](https://github.com/total64/attack-resistant-backup-recovery)**

## 👥 My Contribution

My role was to build the brain of the system: the **Cyber Resilience Decision Engine**, along with the data models, policies, and rules. 

When the risk engine detects a threat, my engine decides how the system should respond based on the policies I wrote. It outputs one of five actions:
- **Allow** — Safe activity
- **Alert** — Medium risk
- **Protect** — Create a backup
- **Isolate** — Cut network access
- **Recover** — Restore from a backup

I also built the **audit logging** to ensure every decision is tracked.

### 📁 Key Files I Built (View on my feature branch)
You can see my exact work on the `feature/decision-engine` branch here:

- **[Decision Engine Models](https://github.com/total64/attack-resistant-backup-recovery/blob/feature/decision-engine/backend/app/decision/models.py)** — The core data structures (like `SecurityEvent`) used by the Decision Engine. 
- **[Unit Tests Folder](https://github.com/total64/attack-resistant-backup-recovery/tree/feature/decision-engine/backend/tests/unit)** — The comprehensive test suite for the Decision Engine and Risk Engine.

**📊 Test Results:**
I successfully fixed the `SecurityEvent` model compatibility and verified the logic by getting **all 35 tests to pass**.
