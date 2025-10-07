---
type: reference
channel: internal
status: draft
date: 2025-10-06
source: Obsidian Official Documentation + Community Resources
aliases:
  - Bases Guide
  - Database Views
  - Base Creation
tags:
  - type/reference
  - channel/internal
  - status/draft
last_pasted:
live_link:
violates_shadow: false
---

#type/reference #channel/internal #status/draft

# Obsidian Bases Setup Guide

## What Are Bases?

Bases are Obsidian's native database feature that lets you create dynamic, filtered table views of your notes. Think of them as spreadsheet views of your vault organized by properties.

**Key Benefits:**
- No programming knowledge required (unlike Dataview)
- Interactive filtering and sorting
- Inline property editing
- Multiple views of the same data
- Can be embedded in notes

## Enable Bases Plugin

1. Settings → Core plugins
2. Find "Bases" and toggle ON
3. Restart Obsidian if needed

## Creating Your First Base

### Method 1: Command Palette
1. `Cmd/Ctrl + P` → "Bases: Create new base"
2. Name your base
3. Select folder location

### Method 2: Right-Click
1. Right-click any folder
2. Select "New base"
3. Name your base

### Method 3: Insert Base
1. `Cmd/Ctrl + P` → "Bases: Insert new base"
2. Creates an embedded base in current note

## Anatomy of a Base

A Base consists of:
- **Filters** — Which notes to include
- **Properties** — Which columns to display
- **Views** — Different perspectives on the same data

## Setting Up Filters

Filters determine which notes appear in your Base.

### Common Filter Patterns

**By Type:**
```
property: type
operator: is
value: pin
```

**By Channel:**
```
property: channel
operator: is
value: fb
```

**By Status:**
```
property: status
operator: is not
value: posted
```

**By Tag:**
```
property: tags
operator: contains
value: type/runbook
```

### Filter Operators

- `is` — Exact match
- `is not` — Excludes exact match
- `contains` — Includes substring
- `does not contain` — Excludes substring
- `starts with` — Begins with
- `ends with` — Ends with
- `exists` — Has any value
- `does not exist` — Empty/missing

### Combining Filters

**AND (all must be true):**
```
type is pin
AND status is draft
```

**OR (any can be true):**
```
type is pin
OR type is dm
```

**NOT (none can be true):**
```
NOT status is posted
```

## Selecting Properties (Columns)

Choose which metadata fields to display:

**Essential Properties:**
- Title (note name)
- type
- channel
- status
- last_pasted
- live_link
- violates_shadow

**How to Add:**
1. Click "Add property" button
2. Select from dropdown
3. Drag to reorder columns

## Creating Multiple Views

Different views = different filters on same base

**Example Views:**
- **All Draft Content** — Status is draft
- **Ready to Post** — Status is final, violates_shadow is false
- **Posted This Week** — Status is posted, last_pasted within 7 days
- **Facebook Only** — Channel is fb or both
- **Skool Only** — Channel is skool or both

**To Create View:**
1. Click view dropdown (top of base)
2. Click "+ New view"
3. Name it
4. Configure filters

## Practical Bases for Brand OS

### 1. Content Pipeline Base
**Purpose:** Track all content from draft to posted
**Folder:** Anywhere (or embed in Operator Runbook)
**Filters:** None (show all content)
**Properties:** title, type, channel, status, last_pasted, live_link
**Views:**
- Backlog (status: draft)
- Ready to Ship (status: final)
- Posted (status: posted)
- Needs Review (violates_shadow: true)

### 2. Weekly Rituals Base
**Purpose:** Track ritual content (Wed/Fri/Sun)
**Filters:** type is ritual OR type is pin
**Properties:** title, channel, status, last_pasted
**Views:**
- Facebook Pins (channel: fb)
- Skool Rituals (channel: skool)
- This Week (last_pasted: last 7 days)

### 3. Guardrails Check Base
**Purpose:** Find content that might violate shadow
**Filters:** violates_shadow is true OR violates_shadow exists
**Properties:** title, type, channel, violates_shadow, live_link
**Views:**
- All Flagged
- Posted Violations (needs urgent fix)

### 4. Sales Assets Base
**Purpose:** All sales and DM scripts
**Filters:** type is sales OR type is dm
**Properties:** title, channel, status, last_pasted, live_link
**Views:**
- Facebook Assets (channel: fb)
- Skool Assets (channel: skool)
- Ready to Use (status: final)

## Embedding Bases in Notes

Add bases directly in your markdown files:

```markdown
## My Content Pipeline

```base
path: Brand OS/Bases/Content Pipeline.base
```
\```
```

**Use Cases:**
- Embed in Operator Runbook for daily dashboard
- Add to Creator Runbook for queue visibility
- Include in Monthly Review for metrics

## Tips & Best Practices

### 1. Keep Filters Simple
Start with 1-2 filters, add more as needed

### 2. Use Views for Complexity
Instead of complex filters, create multiple simple views

### 3. Name Views Clearly
"Draft FB Pins" is better than "View 1"

### 4. Regular Property Types
Stick to consistent property types across vault:
- Text: type, channel, status
- Date: last_pasted
- URL: live_link
- Boolean: violates_shadow

### 5. Sort Strategically
- Content Pipeline: Sort by status, then last_pasted
- Weekly Rituals: Sort by last_pasted descending
- Guardrails: Sort by violates_shadow, then type

### 6. Limit Columns
Show 4-6 key properties, hide the rest

### 7. Update Properties Inline
Click any cell to edit without opening the note

## Limitations (as of 2025)

- Only table views (card/list views coming)
- No image support in tables
- Inline properties not supported
- No nested property display
- Limited date formatting options

## Next Steps

1. ✅ Enable Bases plugin
2. ✅ Review vault properties (already done!)
3. 📝 Create "Content Pipeline" base
4. 📝 Add views for different statuses
5. 📝 Embed base in Operator Runbook
6. 📝 Create additional bases as needed

## Resources

- [Official Obsidian Bases Docs](https://help.obsidian.md/bases)
- [Bases Syntax Reference](https://help.obsidian.md/bases/syntax)
- [Getting Started Guide](https://obsidian.rocks/getting-started-with-obsidian-bases/)
- [Bases Plugin Overview](https://practicalpkm.com/bases-plugin-overview/)
