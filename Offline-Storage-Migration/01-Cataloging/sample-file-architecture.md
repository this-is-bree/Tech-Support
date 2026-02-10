# Sample File Architecture

Organized structure provided to client during cataloging for workflow planning.

## Proposed Structure
```
Archive/
├── Photos/
│   ├── 2007-2009/
│   │   ├── Events/
│   │   ├── Family/
│   │   └── Travel/
│   ├── 2010-2012/
│   │   ├── Events/
│   │   ├── Family/
│   │   └── Travel/
│   ├── 2013-2015/
│   └── 2016-2018/
│
├── Videos/
│   ├── Family/
│   ├── Travel/
│   ├── Events/
│   └── Projects/
│
├── Documents/
│   ├── Work/
│   │   ├── Projects/
│   │   ├── Contracts/
│   │   └── Archive/
│   ├── Personal/
│   │   ├── Financial/
│   │   ├── Medical/
│   │   └── Legal/
│   └── Reference/
│
├── Time-Machine-Extracts/
│   └── [User data only - Documents, Photos, Music, Movies]
│
└── Misc/
    └── [Uncategorized - pending client review]
```

## Design Principles

1. **Chronological for media:** Photos/Videos by year ranges
2. **Categorical for documents:** By type and purpose
3. **Separate Time Machine data:** Client can review extracted user files
4. **Misc folder:** Temporary holding for uncategorized items

## Client Feedback

- ✅ Chronological photo organization approved
- ✅ Video subcategories helpful
- 📝 Requested: Add "Projects" subfolder under Documents/Work
- 📝 Considering: Separate "Scanned Documents" category

## Implementation Notes

- Structure will be created in Phase 3
- Client can refine during ongoing cataloging
- Final structure may evolve based on actual content discovered
