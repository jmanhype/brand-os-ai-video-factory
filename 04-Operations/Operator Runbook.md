---
type: runbook
channel: internal
status: draft
date: 2025-10-06
aliases:
  - Daily Operations
  - Weekly Reset
tags:
  - type/runbook
  - channel/internal
  - status/draft
last_pasted:
live_link:
violates_shadow: false
---

#type/runbook #channel/internal #status/draft

# Operator Runbook — AI Video Factory

## Daily 15-Minute Ship

1. Open Publishing Queue (Table) → pick oldest last_pasted
2. Paste the card live (FB/Skool)
3. Update live_link + last_pasted=today + Shadow check
4. Post a proof (before/after or 10-sec clip) or queue it for Wed

## Weekly 60-Minute Reset (Fri 10:00 CT)

1. Plan Rogue Build (#case card; link Persona → Case → ProductFacts)
2. QC: claims from /claims/ProductFacts.yml, real packshot, OCR/ASR match
3. Refresh Pins/Sales/Start-Here if needed
4. Post events (Fri/Wed/Sun) + log links
5. Update publishing tracker

## Definitions

**DoR (card):** headings filled; linked to Charter + Guardrails
**DoD (card):** status=final; pasted; live_link set; proof captured
