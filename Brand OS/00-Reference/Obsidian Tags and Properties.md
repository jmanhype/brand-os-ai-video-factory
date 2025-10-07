---
type: reference
source: Obsidian Official Documentation
date: 2025-10-06
---

# Obsidian Tags and Properties Reference

## Tags

### Creating Tags

Tags are keywords that help you quickly find notes. Create tags by:

1. **Inline tags:** Type `#` immediately followed by the tag name (no spaces)
   - Example: `#work`, `#recipes`, `#tasks`

2. **YAML frontmatter tags:**
```yaml
---
tags:
  - recipe
  - cooking
---
```

### Tag Format Rules

**Allowed characters:**
- Alphabetical letters
- Numbers
- Underscore (`_`)
- Hyphen (`-`)
- Forward slash (`/`) for nested tags

**Important rules:**
- Must contain at least one non-numerical character (#y1984 ✅, #1984 ❌)
- Case-insensitive (#tag and #TAG are treated as identical)
- No spaces allowed

**Multi-word tags:**
- `#camelCase`
- `#PascalCase`
- `#snake_case`
- `#kebab-case`

### Nested Tags

Create hierarchies using forward slashes:
- `#inbox/to-read`
- `#inbox/processing`
- `#blogwriting/writing`
- `#blogwriting/editing`
- `#blogwriting/publishing`

When you search for a parent tag, all subtags are included.

### Finding Notes with Tags

**Using Tags View:**
1. Enable "Tags" core plugin
2. Click tags icon in sidebar
3. Click any tag to search

**Using Search:**
```
tag:#meeting
tag:#blogwriting/editing
tag:#blogwriting  (includes all nested tags)
```

### Tag Best Practices

1. **Tag consistently** — Use same format every time
2. **Tag sparingly** — Less is more; every tag should mean something
3. **Tag memorably** — Tags only need to make sense to you
4. **Use lowercase** — Prevents duplication issues
5. **Use singular form** — `#book` not `#books`
6. **Utilize autocomplete** — Prevents typos and new unwanted tags

### Tag Wrangler Plugin

Community plugin for advanced tag management:
- Right-click to rename tags across entire vault
- Merge tags by renaming to same name
- Granular search options
- Exclude specific tags from searches

---

## Properties (YAML Frontmatter)

### What Are Properties?

Properties are structured metadata for your notes, added at the top of files in YAML format.

### Basic Format

```yaml
---
property_name: value
another_property: value
---
```

### Common Property Types

**Text:**
```yaml
---
author: Edgar Allan Poe
status: Draft
---
```

**Numbers:**
```yaml
---
published: 1845
rating: 5
---
```

**Lists/Arrays:**
```yaml
---
tags:
  - poems
  - classic
aliases:
  - Doggo
  - Woofer
---
```

**Dates:**
```yaml
---
created: 2025-10-06
due_date: 2025-12-31
---
```

**Checkboxes:**
```yaml
---
completed: true
archived: false
---
```

### Special Properties

**aliases:**
Alternative names for the note
```yaml
---
aliases:
  - Rebel + Lover
  - AI Video Factory Brand
---
```

**cssclasses:**
Apply custom CSS styling
```yaml
---
cssclasses:
  - soft-embed
  - list-cards
---
```

**permalink:**
Custom URL structure
```yaml
---
permalink: brand-charter
---
```

### Searching with Properties

**Check if property exists:**
```
[aliases]
```

**Search for specific value:**
```
[status:Draft]
[author:Edgar Allan Poe]
```

**Use OR operator:**
```
[status:Draft OR Published]
```

### Inline Properties (Dataview syntax)

Alternative to frontmatter:
```
[property:: value]
From [author:: Edgar Allan Poe], written in (published:: 1845)
```

---

## Obsidian Bases (Database Views)

### What Are Bases?

Bases allow you to create database-like views of your notes formatted as tables or cards. You can edit, sort, and filter files using their properties.

### Key Features

- View notes as tables or cards
- Filter and sort by properties
- Group notes by property values
- Edit properties directly in the view
- Real-time updates

### Bases vs. Dataview

**Bases (Native):**
- Built-in Obsidian feature
- GUI-based
- Easier for beginners
- Limited query capabilities

**Dataview (Plugin):**
- More powerful querying
- JavaScript API available
- Greater flexibility
- Steeper learning curve

---

## For AI Video Factory Brand OS

### Recommended Tag Structure

```
#type/charter
#type/pin
#type/dm
#type/sales
#type/runbook
#type/ritual

#channel/fb
#channel/skool
#channel/both
#channel/internal

#status/draft
#status/final
#status/posted
```

### Recommended Properties

```yaml
---
type: charter | pin | dm | sales | runbook | ritual
channel: fb | skool | both | internal
status: draft | final | posted
last_pasted: 2025-10-06
live_link: https://...
violates_shadow: false
---
```

### Using Both Together

Tags for **quick filtering** and **discovery**:
- Browse all #type/pin files
- See all #status/draft items

Properties for **structured data** and **tracking**:
- Sort by last_pasted date
- Filter where violates_shadow = false
- Create Bases view of all content with links

This approach gives you maximum flexibility and organization power!
