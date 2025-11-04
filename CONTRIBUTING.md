# Contributing to AI Video Factory - Brand OS

Thank you for your interest in contributing to the AI Video Factory Brand OS! This document provides guidelines for contributing to this repository.

## Code of Conduct

### Our Standards

- **Be Direct** - Clear communication over politeness for politeness' sake
- **Demonstrate, Don't Speculate** - Show receipts and working examples
- **Respect Consent & Credit** - Always attribute sources and respect intellectual property
- **No Shadow Violations** - We're not entertainers; outcomes matter more than applause

### Brand Identity

This Brand OS is built on:
- **Primary Archetype:** Rebel (challenge broken systems)
- **Secondary Archetype:** Lover (build community, credit collaborators)
- **Shadow (Not-Us):** Entertainer (no shock-for-shock, no empty humor)

Keep this identity in mind when contributing.

## How to Contribute

### Reporting Issues

1. **Check existing issues** first to avoid duplicates
2. **Use descriptive titles** - Be specific about the problem
3. **Provide context** - Include:
   - What you expected to happen
   - What actually happened
   - Steps to reproduce (if applicable)
   - Relevant files or sections

### Suggesting Enhancements

1. **Describe the enhancement** clearly
2. **Explain the use case** - Why is this valuable?
3. **Provide examples** - Show how it would work
4. **Consider the brand** - Does it align with Rebel + Lover?

### Pull Requests

#### Before You Start

- **Review CLAUDE.md** - Understand what changes are allowed
- **Check for existing PRs** - Someone may be working on similar changes
- **Discuss major changes** - Open an issue first for big modifications

#### Pull Request Process

1. **Fork the repository** and create a new branch from `main`
2. **Make your changes** following the guidelines below
3. **Test your changes** - Ensure links work, formatting is correct
4. **Commit with clear messages** - Explain what and why
5. **Submit the PR** with a detailed description

#### PR Checklist

- [ ] Changes follow the Brand OS structure and conventions
- [ ] All YAML frontmatter is properly formatted
- [ ] No placeholder URLs are introduced without documentation
- [ ] Links are tested and working
- [ ] Markdown formatting is consistent
- [ ] No violations of brand shadow (Entertainer)
- [ ] Changes are documented in PR description

## Documentation Standards

### File Structure

All content files should include YAML frontmatter:

```yaml
---
type: charter | pin | dm | sales | runbook | ritual | reference
channel: fb | skool | both | internal
status: draft | final | posted
date: YYYY-MM-DD
aliases:
  - Alternative Name
tags:
  - type/value
  - channel/value
  - status/value
last_pasted:
live_link:
violates_shadow: false
---
```

### Writing Guidelines

1. **Be Concise** - Zero fluff; receipts win
2. **Use Active Voice** - "Ship today" not "It should be shipped"
3. **Include CTAs** - Every piece should have a call-to-build
4. **Link Sources** - Credit and link to original sources
5. **Stay On-Brand** - Use approved words, avoid banned words

#### Approved Words
- ship, today, receipt, exact, consent, posted

#### Avoid These Words
- hype, hustle, secret, hack, passive, "$X/day"

### Markdown Formatting

- Use `##` for main sections (frontmatter uses level 1)
- Use code blocks with triple backticks for templates
- Use `**bold**` for emphasis, not ALL CAPS
- Use lists for steps and checklists
- Use `---` for horizontal rules between major sections

## What We're Looking For

### High-Value Contributions

✅ **Documentation improvements** - Clearer instructions, better examples
✅ **Bug fixes** - Broken links, formatting issues, typos
✅ **Template enhancements** - Better DM scripts, pin copy, runbooks
✅ **Reference materials** - Guides, checklists, best practices
✅ **Obsidian optimizations** - Better Bases configs, property structures

### What to Avoid

❌ Breaking changes to established templates
❌ Removing content without justification
❌ Adding heavy dependencies or complex tooling
❌ Introducing entertainment-focused content
❌ Changing brand voice without discussion

## Development Setup

### Prerequisites

- [Obsidian](https://obsidian.md) (recommended) or any markdown editor
- Git for version control
- Basic understanding of YAML frontmatter

### Setup Steps

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/brand-os-ai-video-factory.git
   cd brand-os-ai-video-factory
   ```

2. Open in Obsidian
   - File → Open vault
   - Select the cloned directory

3. Review the structure
   - Read `README.md`
   - Review `01-Core/Brand Charter.md`
   - Check `config.template.md` for placeholders

4. Create a new branch
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Commit Message Guidelines

Use clear, descriptive commit messages:

**Good examples:**
- `docs: Add configuration examples to README`
- `fix: Correct broken link in DM Scripts`
- `feat: Add new Rapid Response template`
- `refactor: Reorganize Guardrails checklist`

**Format:**
```
type: Short description (50 chars max)

Optional longer description explaining the change
and why it was necessary.
```

**Types:** docs, feat, fix, refactor, style, test

## Review Process

1. **Automated checks** - GitHub Actions will run basic validation
2. **Maintainer review** - A maintainer will review your PR
3. **Feedback & iteration** - Address any requested changes
4. **Merge** - Once approved, your PR will be merged

## Questions?

- **Open an issue** for questions about contributing
- **Check existing docs** in `Brand OS/00-Reference/`
- **Review CLAUDE.md** for AI-assisted contribution guidelines

## Recognition

Contributors will be acknowledged in:
- Git commit history
- Release notes (for significant contributions)
- Community mentions (with consent)

---

**Remember:** From blank to posted in one sitting. Keep contributions focused, demonstrable, and on-brand.

Thank you for helping improve the AI Video Factory Brand OS! 🎥⚙️
