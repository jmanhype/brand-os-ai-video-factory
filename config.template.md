# Configuration Template

This file documents all placeholder URLs and configuration values used throughout the Brand OS.

## Required Placeholders

Before using the marketing materials in `02-Marketing/` and `03-Skool/`, replace these placeholders with your actual values:

### Marketing & Community Links

| Placeholder | Description | Example | Used In |
|------------|-------------|---------|---------|
| `[STARTER_CHECKLIST_URL]` | Link to your free starter checklist | `https://example.com/checklist` | Pins - Facebook |
| `[SKOOL_URL]` | Primary link to your Skool community | `https://skool.com/your-community` | Pins - Facebook, DM Scripts |
| `[YOUR SKOOL LINK]` | Alternative Skool link reference | `https://skool.com/your-community` | Pins - Facebook |
| `[FRI_TIME_CT]` | Build Friday time in Central Time | `10:00 AM CT` or `Fridays at 10 AM` | Pins - Facebook |
| `[CHECKLIST LINK]` | Another checklist reference | `https://example.com/checklist` | DM Scripts |
| `[SKOOL LINK]` | Another Skool reference | `https://skool.com/your-community` | DM Scripts |

## How to Configure

### Option 1: Manual Find & Replace

1. Open each file in `02-Marketing/` and `03-Skool/`
2. Use find & replace in your editor
3. Replace each placeholder with your actual value
4. Save the file

### Option 2: Using VS Code

```bash
# Find all placeholders
grep -r "\[.*_URL\]" 02-Marketing/ 03-Skool/
grep -r "\[YOUR.*\]" 02-Marketing/ 03-Skool/
grep -r "\[FRI_TIME.*\]" 02-Marketing/ 03-Skool/
```

Then use VS Code's multi-file find & replace (Cmd/Ctrl+Shift+H).

### Option 3: Using sed (macOS/Linux)

```bash
# Example: Replace STARTER_CHECKLIST_URL
find . -name "*.md" -type f -exec sed -i '' 's|\[STARTER_CHECKLIST_URL\]|https://example.com/checklist|g' {} +

# Replace SKOOL_URL
find . -name "*.md" -type f -exec sed -i '' 's|\[SKOOL_URL\]|https://skool.com/your-community|g' {} +

# Replace FRI_TIME_CT
find . -name "*.md" -type f -exec sed -i '' 's|\[FRI_TIME_CT\]|10:00 AM CT|g' {} +
```

**Note:** On Linux, remove the `''` after `-i`

## Verification

After configuration, verify no placeholders remain:

```bash
# Check for remaining placeholders
grep -r "\[.*_URL\]" 02-Marketing/ 03-Skool/ || echo "✅ All URL placeholders configured"
grep -r "\[YOUR.*\]" 02-Marketing/ 03-Skool/ || echo "✅ All YOUR placeholders configured"
grep -r "\[FRI_TIME.*\]" 02-Marketing/ 03-Skool/ || echo "✅ All time placeholders configured"
```

## Files That Need Configuration

- `02-Marketing/Pins - Facebook.md` - Contains most placeholders
- `02-Marketing/DM Scripts.md` - Contains Skool and checklist links

## Best Practices

1. **Keep URLs consistent** - Use the same link for the same resource
2. **Use tracking parameters** - Add UTM parameters to track traffic sources
3. **Test all links** - Verify each link works before publishing
4. **Update regularly** - Keep links current as your offerings change
5. **Backup original** - Keep a copy with placeholders for future reference

## Example Configuration

```yaml
STARTER_CHECKLIST_URL: https://example.com/checklist?utm_source=facebook
SKOOL_URL: https://skool.com/ai-video-factory
FRI_TIME_CT: Fridays at 10:00 AM Central
```

## Need Help?

- Check the main [README.md](README.md) for setup instructions
- Review [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines
- See individual files for context on how placeholders are used
