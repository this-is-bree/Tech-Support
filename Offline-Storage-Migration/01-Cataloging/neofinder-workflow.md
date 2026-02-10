# NeoFinder Cataloging Workflow

Step-by-step guide for cataloging drives with MD5 checksums.

## Initial Setup

1. **Install NeoFinder** ($40 from cdfinder.de)
2. **Configure Preferences:**
   - Tools → Preferences → Cataloging
   - ✅ Calculate MD5 Checksums
   - ✅ Create Thumbnails (High, 512×512)
   - ✅ Index file contents

## Per-Drive Workflow

### 1. Connect Drive
- Use powered Thunderbolt hub (OWC Thunderbolt Go)
- Wait for drive to mount
- Check for unusual sounds (clicking = failing drive)

### 2. Create Catalog
```
Menu: Catalog → Catalog a Volume (⌘-N)

Settings:
✅ Create Thumbnails
✅ Calculate Checksums (MD5)
✅ Index file contents

Naming: "Drive## - [Content] - [Size] - [DateRange]"
Example: "Drive01 - Photos - 1TB - 2010-2014"

Click "Start"
```

### 3. Monitor Progress
- Time: 0.5-2TB per hour (depends on drive speed)
- Do NOT disconnect until "Catalog Complete"

### 4. Verify Quality
- Browse catalog (should load without drive mounted)
- Check thumbnails loaded
- Verify MD5 column shows hashes
- Test search functionality

### 5. Analyze Duplicates
```
Tools → Find Duplicates
- Select: Current catalog only
- Method: Checksum (MD5)
- Note: "Total wasted space" at bottom
```

### 6. Document
- Update drive-inventory.csv with results
- Calculate duplicate percentage
- Label physical drive

### 7. Eject Safely
```bash
# Right-click icon → Eject
# OR
diskutil eject /Volumes/[DriveName]
```

## Tips

**For Multiple Drives:**
- Can catalog 2-3 simultaneously with Thunderbolt dock
- Saves ~40% wall-clock time

**For Failed Drives:**
- Document specific errors
- Note which files failed
- Set aside for professional recovery assessment

**Time Management:**
- Old HDDs: ~1-2 hours each
- Modern SSDs (3-4TB): ~2-4 hours each
- Batch overnight for large drives
