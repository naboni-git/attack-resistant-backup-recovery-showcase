# Attack-Resistant Backup and Recovery System (ARBR)

A showcase repository for the ARBR project. 

**An automated system for detecting attacks, protecting backups, and enabling secure recovery.**

## 🔗 Source Code
The full source code, commit history, and complete team contributions are hosted on the original project repository:

👉 **[View the ARBR Source Code on GitHub](https://github.com/total64/attack-resistant-backup-recovery)**

## 📂 Project Structure
- `backend/` — Server-side logic
- `detector/` — Attack detection modules
- `frontend/` — User interface
- `isolation/` — Core isolation and recovery scripts
- `recovery/scripts/` — Firewall and recovery automation
- `rules/` — Security rules and verification
- `tests/` — Test suites

## 👥 My Contribution

My role was to build the brain of the system: the **Cyber Resilience Decision Engine**, along with the data models, policies, and rules. 

When the risk engine detects a threat, my engine decides how the system should respond based on the policies I wrote. It outputs one of five actions:
- **Allow** — Safe activity
- **Alert** — Medium risk
- **Protect** — Create a backup
- **Isolate** — Cut network access
- **Recover** — Restore from a backup

I also built the **audit logging** to ensure every decision is tracked.

### 📁 Key Files I Built

- **[Decision Models](https://github.com/total64/attack-resistant-backup-recovery/blob/main/backend/app/decision/models.py)** — The core data structures (like `SecurityEvent`) used by the Decision Engine. *(See my commit adding the `host_id` tracking).*
- **[Unit Tests for Decision Engine](https://github.com/total64/attack-resistant-backup-recovery/blob/main/backend/tests/unit/test_decision_engine.py)** — Comprehensive test suite proving the logic works.
- **[Integration Tests](https://github.com/total64/attack-resistant-backup-recovery/blob/main/backend/tests/test_decision_engine_integration.py)** — Ensuring the engine plays nicely with the rest of the system.

**📊 Test Results:**
I successfully fixed the `SecurityEvent` model compatibility and verified the logic by getting **all 35 tests to pass** (Commit `9d4fbaa`).
