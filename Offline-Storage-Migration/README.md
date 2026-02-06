# Offline Storage Migration

![Project Status](https://img.shields.io/badge/status-in%20progress-yellow)
![Phase](https://img.shields.io/badge/phase-1%20cataloging-blue)
![Data Processed](https://img.shields.io/badge/cataloged-5TB%20%2F%2020%2B%20drives-green)

Systematic consolidation of 20+ legacy hard drives (1990s-present) into a single organized archive with verified backups, using catalog-based deduplication to minimize storage costs.

---

## 🎯 Challenge

**Problem:**
Over 20 external hard drives accumulated across 30+ years with unknown duplicate rates, inconsistent organization, and no centralized inventory. Cloud storage costs for 15-20TB+ are prohibitive, and purchasing hardware before knowing actual storage needs risks overspending.

**Goal:**
Consolidate into a single organized archive with verified backup while eliminating duplicates and maintaining data integrity throughout migration.

**Approach:**
Catalog-first workflow using checksums to analyze offline drives, determine true storage needs, then purchase appropriately-sized hardware.

---

## 📁 Project Phases

### [Phase 1: Cataloging & Inventory](./01-cataloging/) 
**Status:** 🟡 In Progress (9/20+ drives, 5TB indexed)
- Index all drives with MD5 checksums using NeoFinder
- Create searchable offline inventory
- Document drive conditions and content types

### [Phase 2: Capacity Planning](./02-capacity-planning/)
**Status:** ⚪ Not Started
- Run cross-catalog duplicate analysis
- Calculate storage needs: `(Total - Duplicates - Junk) × 1.3`
- Select appropriate hardware

### [Phase 3: Deduplication & Consolidation](./03-deduplication/)
**Status:** ⚪ Not Started
- Set up staging workflow
- Process drives iteratively: copy → dedupe → organize
- Build final organized structure

### [Phase 4: Backup & Verification](./04-backup-verification/)
**Status:** ⚪ Not Started
- Clone final drive with Carbon Copy Cloner
- Verify integrity with checksum validation
- Document recovery procedures

---

## 🛠️ Tools Used

| Tool | Purpose | Why Selected |
|------|---------|--------------|
| **NeoFinder** | Drive cataloging | MD5 checksums, offline search, virtual folder planning |
| **dupeGuru** | Deduplication | Hash-based matching, cross-folder comparison |
| **Carbon Copy Cloner** | Backup | Byte-level verification, bootable clones |
| **macOS Terminal** | Automation | Batch operations, verification scripts |

---

## 💼 Skills Demonstrated

**Technical:** Data integrity (checksums), storage management, macOS administration, bash scripting, backup/recovery procedures

**Process:** Project planning, risk management, documentation, cost optimization, problem-solving under constraints

---

## 📊 Current Progress

**Updated:** February 6, 2025

**Phase 1 Status:**
- Drives cataloged: 9 of 20+
- Data indexed: 5TB (estimated 15-20TB total)
- Cataloging rate: ~0.5-1TB/hour
- Oldest data found: 1990s

**Key Findings:**
- Multiple backup generations discovered (high duplicate likelihood)
- Overlapping time periods across drives (2010-2015 on 3+ drives)
- Some aging drives showing slow read speeds (priority migration candidates)

**Next Milestone:** Complete all drive cataloging

---

## 📖 Repository Structure
```
offline-storage-migration/
├── 01-cataloging/          # Drive inventory methodology
├── 02-capacity-planning/   # Storage requirement calculations  
├── 03-deduplication/       # Consolidation workflow
├── 04-backup-verification/ # Data integrity validation
└── docs/                   # Tool comparisons, lessons learned
```

Each phase folder contains detailed documentation, configuration files, and scripts.

---

## 💡 Key Learnings (So Far)

**What's Working:**
- NeoFinder's checksums enable true offline duplicate detection
- Clear drive labeling during cataloging saves significant time
- Parallel spreadsheet tracking helps monitor progress

**Challenges:**
- USB 2.0 drives significantly slower (3-4x longer cataloging time)
- Mixed file systems require different handling approaches
- Powered USB hub essential for safely connecting multiple drives

**Adaptations:**
- Processing faster drives first to build momentum
- Running slow drives overnight
- Prioritizing aging/failing drives for early migration

---

## 🚀 Future Improvements

- Automate duplicate resolution with smart rules (higher resolution, newer dates)
- Implement automated backup schedule post-migration
- Consider NAS solution for network-accessible archive at scale
- Add selective cloud backup tier for critical files only

---

## 📄 License

MIT License - Documentation freely adaptable for similar projects

---

## 👤 Contact

February 2025 | Help Desk / General IT Portfolio Project

---

**Project Started:** February 2025  
**Last Updated:** February 6, 2025
