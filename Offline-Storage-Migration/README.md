# Offline Storage Migration

![Project Status](https://img.shields.io/badge/status-in%20progress-yellow)
![Phase](https://img.shields.io/badge/phase-1%20cataloging-blue)
![Data Processed](https://img.shields.io/badge/cataloged-14.5TB%20%2F%2033%2B%20drives-green)
![Deduplication](https://img.shields.io/badge/duplicate%20rate-80%25-red)

Systematic consolidation of 33+ legacy hard drives (2007-present, with older archives pending) into a single organized archive with verified backups, using catalog-based deduplication to minimize storage costs.

## 📋 Table of Contents
- [Challenge](#challenge)
- [Technical Approach](#technical-approach)
- [Project Phases](#project-phases)
- [Current Progress](#current-progress)
- [Key Findings](#key-findings)
- [Tools Used](#tools-used)
- [Skills Demonstrated](#skills-demonstrated)
- [Repository Structure](#repository-structure)
- [Lessons Learned](#lessons-learned)

---

## 🎯 Challenge

**Problem Statement:**
Over 33 external hard drives accumulated across 15+ years (2007-present, with additional pre-2007 archives) containing mixed data types with:
- Unknown duplicate rates across drives (now confirmed at ~80%)
- Inconsistent file organization and naming conventions
- Multiple Time Machine backups creating massive redundancy
- No centralized inventory or searchable index
- Risk of data loss from aging hardware (30% failure rate encountered)
- Prohibitive cloud storage costs for 15-20TB+ initial consolidation

**Goal:**
Consolidate all data into a single organized archive with verified backup while:
- Eliminating duplicates to minimize final storage requirements (expecting 60-80% reduction)
- Avoiding upfront hardware investment before knowing actual storage needs
- Maintaining data integrity throughout migration
- Creating a repeatable, documented process
- Providing client with usable file architecture during lengthy cataloging phase

**Constraints:**
- Mac-only workflow (no Windows/Linux tools)
- No cloud dependency for primary workflow (bandwidth/cost)
- Must work with offline drives (can't have all 33+ connected simultaneously)
- Limited staging space for intermediate processing
- Client needs access to organized structure before completion

---

## 🔧 Technical Approach

### Strategy Overview

**Catalog-First Workflow:**
1. **Catalog Before Purchase** - Index all drives with MD5 checksums to determine actual storage needs
2. **Content-Based Deduplication** - Use checksums to identify true duplicates regardless of filename/location
3. **Parallel Client Workflow** - Provide sample organized structure for client use during ongoing cataloging
4. **Staged Migration** - Process drives in batches using temporary staging area after cataloging complete
5. **Verified Backup** - Clone final archive with byte-level verification

### Why This Approach?

- ✅ **Reveals true storage needs:** 14.5TB cataloged → 2.9TB unique (80% duplicate rate confirmed)
- ✅ **Reduces risk:** Originals untouched until verified
- ✅ **Enables offline duplicate detection** across 33+ unmounted drives
- ✅ **Provides early value to client** via sample file architecture
- ✅ **Documents entire process** for repeatability and portfolio demonstration

---

## 📁 Project Phases

### [Phase 1: Cataloging & Inventory](./01-cataloging/) 
**Status:** 🟡 In Progress (12/33+ drives, 14.5TB indexed)

- Catalog all drives with MD5 checksums using NeoFinder
- Create searchable inventory of all files across offline volumes
- Document drive conditions and handle hardware failures
- Identify duplicate rates and estimate final storage needs
- Provide sample file architecture to client for early workflow testing
- **Current Progress:** 80% duplicate rate discovered (14.5TB → 2.9TB unique)

---

### [Phase 2: Capacity Planning](./02-capacity-planning/)
**Status:** ⚪ Not Started (awaiting completion of cataloging)

- Run comprehensive cross-catalog duplicate analysis on all 33+ drives
- Calculate final storage requirements: `(Total Raw - Duplicates - Time Machine - Junk) × 1.3`
- Estimate: ~15-20TB raw → ~3-5TB unique (based on current 80% dedup rate)
- Select appropriate hardware based on deduplication results
- **Deliverable:** Final storage requirement calculation and hardware purchase decision

---

### [Phase 3: Deduplication & Consolidation](./03-deduplication/)
**Status:** ⚪ Not Started

- Set up staging workflow on final drive
- Process drives iteratively: copy → dedupe → organize → verify
- Resolve duplicate conflicts (keep newest/highest quality version)
- Build final organized folder structure based on client-tested architecture
- **Deliverable:** Single consolidated archive with all unique files in organized structure

---

### [Phase 4: Backup & Verification](./04-backup-verification/)
**Status:** ⚪ Not Started

- Clone final drive using Carbon Copy Cloner with verification
- Verify backup integrity with checksum validation
- Test recovery process
- Document recovery procedures
- Securely wipe original drives
- **Deliverable:** Verified backup system with documented recovery procedures

---

## 📊 Current Progress

**Updated:** February 10, 2025

### Phase 1 Metrics

**Cataloging Status:**
- Drives cataloged: **12 of 33+** (36% complete)
- Additional uncounted drives: Pre-2007 archive box (quantity TBD)
- Data indexed: **14.5TB** (14,525.11 GB)
- Unique data identified: **2.9TB** (2,900.03 GB)
- **Duplicate rate: 80%** (11.6TB of duplicates)
- Date range cataloged: 2007-2018
- Oldest data found: 2007 (pre-2007 box pending)

**Drive Content Breakdown (12 drives):**
- Time Machine backups: 1 drive (major contributor to duplicates)
- Photos: 7 drives (significant overlap suspected)
- Videos: 2 drives
- Files: 1 drive
- Misc: 5 drives (mixed content)

**Remaining Work:**
- 21+ drives (3TB+ each, newer SSDs - longer catalog times expected)
- Pre-2007 archive box (quantity and capacity unknown)
- Estimated remaining data: 40-60TB raw (based on drive sizes)

### Hardware Issues Encountered

**Failure Rate: 30% (3 of 10 initial drives)**
- 1 drive: Read-only, 3 files unrecoverable
- 1 drive: Won't connect at all
- 1 drive: Consistent disconnects during cataloging
- **Lesson:
