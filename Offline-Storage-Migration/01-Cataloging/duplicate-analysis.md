# Duplicate Analysis: 80% Deduplication Rate

Analysis of 12 drives revealing 14.5TB → 2.9TB unique data.

## Overall Statistics

| Metric | Value |
|--------|-------|
| Total Raw Data | 14.5TB (14,525.11 GB) |
| Unique Data | 2.9TB (2,900.03 GB) |
| Duplicate Data | 11.6TB (11,625.08 GB) |
| **Duplicate Rate** | **80%** |

## Breakdown by Content Type

### Time Machine Backups (Primary Culprit)

**Stats:**
- Drives: 1
- Raw size: ~2TB
- Unique content: ~100-200GB
- **Duplicate rate: 90-95%**

**Why So High:**
- Full system state (macOS, Applications, System files)
- Only 5-10% is unique user data (Documents, Photos, etc.)

**Action:**
- Extract only user data folders in Phase 3
- Discard system files, applications, caches
- Expected savings: 1.5-1.8TB

### Photo Collections

**Stats:**
- Drives: 7
- Raw size: ~6TB
- Unique content: ~1.2TB
- **Duplicate rate: 80%**

**Pattern:**
- Same photo libraries on 3-4 different drives
- Example: 2010-2013 photos found on Drives 02, 04, 08, 11
- Each copy ~500GB, only ~100GB unique across all

**Action:**
- Consolidate by MD5 checksum
- Keep highest resolution version
- Expected savings: 4-5TB

### Video Collections

**Stats:**
- Drives: 2
- Raw size: ~3.7TB
- Unique content: ~2.5TB
- **Duplicate rate: 32%**

**Why Lower:**
- Videos less frequently backed up multiple times
- Large file sizes discourage redundant copies

### Files & Misc

**Stats:**
- Drives: 4
- Raw size: ~2.8TB
- Unique content: ~1.1TB
- **Duplicate rate: 61%**

**Pattern:**
- "Misc" drives often contain backups-of-backups
- Documents backed up across multiple "archive" drives

## Implications for Final Storage

**Current Projection (if 80% continues):**
```
Remaining 21 drives @ ~2TB avg = ~42TB
+ Pre-2007 box (est. 5-10TB)
Total raw: ~60-70TB

At 80% duplicate rate:
Unique: ~12-14TB
× 1.3 buffer = 16-18TB final drive

Conservative: 12-16TB final drive needed
```

**Cost Savings:**
- Without deduplication: Would buy 20TB drive (~$500)
- With deduplication: Will buy 12-16TB drive (~$300-350)
- **Savings: $150-200**

## Deduplication Strategy for Phase 3

1. **Time Machine:** Extract user folders only
2. **Photos:** MD5 consolidation, keep best quality
3. **Videos:** Keep all (low duplication)
4. **Misc:** Cross-reference before importing
