# Offline Storage Migration

![Project Status](https://img.shields.io/badge/status-in%20progress-yellow)
![Phase](https://img.shields.io/badge/phase-1%20cataloging-blue)
![Data Processed](https://img.shields.io/badge/cataloged-5TB%20%2F%2020%2B%20drives-green)

Systematic consolidation of 20+ legacy hard drives (1990s-present) into a single organized archive with verified backups, using catalog-based deduplication to minimize storage costs.

## 📋 Table of Contents
- [Challenge](#challenge)
- [Technical Approach](#technical-approach)
- [Tools Used](#tools-used)
- [Project Phases](#project-phases)
- [Skills Demonstrated](#skills-demonstrated)
- [Current Progress](#current-progress)
- [How to Use This Repository](#how-to-use-this-repository)
- [Lessons Learned](#lessons-learned)
- [Future Improvements](#future-improvements)

---

## 🎯 Challenge

**Problem Statement:**
Over 20 external hard drives accumulated across 30+ years containing mixed data types (photos, documents, videos, music, projects, backups) with:
- Unknown duplicate rates across drives
- Inconsistent file organization and naming
- No centralized inventory or searchable index
- Risk of data loss from aging hardware
- Prohibitive cloud storage costs for initial consolidation

**Goal:**
Consolidate all data into a single organized archive with verified backup, while:
- Avoiding upfront hardware investment before knowing actual storage needs
- Eliminating duplicates to minimize final storage requirements
- Maintaining data integrity throughout migration
- Creating a repeatable, documented process

**Constraints:**
- Mac-only workflow (no Windows/Linux tools)
- No cloud dependency for primary workflow (bandwidth/cost)
- Must work with offline drives (can't have all 20 connected simultaneously)
- Limited staging space for intermediate processing

---

## 🔧 Technical Approach

### Strategy Overview
Use **catalog-based workflow** to analyze offline drives before physical consolidation:

1. **Catalog First, Buy Later** - Index all drives with checksums to determine actual storage needs
2. **Content-Based Deduplication** - Use MD5/SHA hashes to identify true duplicates regardless of filename
3. **Staged Migration** - Process drives in batches using temporary staging area
4. **Verified Backup** - Clone final archive with byte-level verification

### Why This Approach?
- ✅ Eliminates guesswork on storage requirements (typical 40-60% deduplication rate)
- ✅ Reduces risk (originals untouched until verified)
- ✅ Enables duplicate detection across offline volumes
- ✅ Documents entire process for repeatability

---

## 🛠️ Tools Used

| Tool | Purpose | Why This Tool |
|------|---------|---------------|
| **NeoFinder** | Drive cataloging & indexing | MD5 checksum support, offline search, virtual folders for planning organization |
| **dupeGuru** | Content-based deduplication | Open-source, true hash-based matching, cross-folder comparison |
| **Carbon Copy Cloner** | Verified backup creation | Byte-level verification, bootable clones, incremental updates |
| **DaisyDisk** | Visual storage analysis | Identify storage hogs, cleanup candidates |
| **macOS Terminal** | Automation scripting | Batch operations, verification scripts |

### Tool Selection Criteria
- Mac-native or well-supported on macOS
- Handles large datasets (multi-TB scale)
- Content-based matching (not just filename/date)
- Offline capability (works with cataloged/unmounted drives)
- Free or one-time purchase (no subscriptions)

---

## 📁 Project Phases

### [Phase 1: Cataloging & Inventory](./01-cataloging/) 
**Status:** 🟡 In Progress (9/20+ drives cataloged, 5TB indexed)

- Catalog all drives with MD5 checksums using NeoFinder
- Create searchable inventory of all files across offline volumes
- Document drive details (size, age, content types)
- **Deliverable:** Complete drive inventory with metadata

---

### [Phase 2: Capacity Planning](./02-capacity-planning/)
**Status:** ⚪ Not Started

- Run cross-catalog duplicate analysis
- Calculate actual storage requirements: `(Total - Duplicates - Junk) × 1.3-1.5`
- Select appropriate hardware based on deduplication results
- **Deliverable:** Storage requirement calculation, hardware purchase decision

---

### [Phase 3: Deduplication & Consolidation](./03-deduplication/)
**Status:** ⚪ Not Started

- Set up staging workflow on final drive
- Process drives iteratively: copy → dedupe → organize → verify
- Resolve duplicate conflicts (keep newest/highest quality)
- Build final organized folder structure
- **Deliverable:** Single consolidated archive with all unique files

---

### [Phase 4: Backup & Verification](./04-backup-verification/)
**Status:** ⚪ Not Started

- Clone final drive using Carbon Copy Cloner
- Verify backup integrity with checksum validation
- Test recovery process
- Securely wipe original drives
- **Deliverable:** Verified backup system, documented recovery procedure

---

## 💼 Skills Demonstrated

### Technical Skills
- **Data Integrity:** Checksum generation and validation (MD5/SHA-1)
- **Storage Management:** Capacity planning, deduplication strategies
- **macOS Administration:** Disk utilities, file system management (APFS/HFS+)
- **Scripting:** Bash automation for batch operations
- **Backup & Recovery:** Clone creation, verification procedures
- **Documentation:** Process documentation, technical writing

### Soft Skills
- **Project Planning:** Breaking complex projects into manageable phases
- **Risk Management:** Maintaining data integrity, avoiding data loss
- **Problem Solving:** Working within constraints (offline drives, limited staging space)
- **Attention to Detail:** Tracking 20+ drives, ensuring no data loss
- **Cost Optimization:** Avoiding unnecessary cloud/hardware costs

---

## 📊 Current Progress

### Phase 1 Status (Updated: [DATE])

**Drives Cataloged:** 9 of 20+
**Total Raw Data Indexed:** 5 TB (estimated 15-20TB total)
**Files Cataloged:** [TBD - NeoFinder total]
**Oldest Data Found:** 1990s
**Cataloging Rate:** ~0.5-1TB per hour (varies by drive speed)

### Preliminary Findings
- Mix of photos, documents, videos, music, software backups
- Multiple backup generations discovered (potential high duplicate rate)
- Some drives contain overlapping time periods (2010-2015 appears on 3+ drives)
- Aging drives showing slow read speeds (candidates for priority migration)

**Next Milestone:** Complete cataloging of all drives (target: [DATE])

---

## 📖 How to Use This Repository

### For Replicating This Process

1. **Review Phase 1** for cataloging methodology
```bash
