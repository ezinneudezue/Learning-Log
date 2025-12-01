# CLAUDE.md - AI Assistant Guide for Learning-Log Repository

## Repository Overview

**Purpose**: A Today I Learned (TIL) log documenting daily technical learnings and insights.

**Owner**: Ezinne Udezue
**License**: MIT
**Repository Type**: Personal knowledge base / learning journal

This repository serves as a structured record of small but meaningful technical insights, concepts, and techniques learned over time. Each entry is designed to be concise, actionable, and reference-able.

## Repository Structure

```
Learning-Log/
├── README.md                 # Repository description and purpose
├── LICENSE                   # MIT License
├── .gitignore               # Python-standard gitignore (prepared for future tooling)
├── YYYY-MM-DD.md            # Daily learning log entries
└── CLAUDE.md                # This file - AI assistant guide
```

### File Organization

- **Date-stamped entries**: Daily logs follow the `YYYY-MM-DD.md` naming convention (e.g., `2025-11-30.md`)
- **Single date per file**: Each file contains learnings from one specific date
- **No subdirectories**: All learning entries live in the root directory for easy browsing
- **Chronological naming**: Files naturally sort chronologically due to ISO 8601 date format

## Content Structure and Format

### Standard Entry Template

Each daily learning file follows this structure:

```markdown
# YYYY-MM-DD – Today I Learned

#[Headline/Key Concept]
[Concise explanation of what was learned, typically 1-3 paragraphs]

[Optional: Code examples, comparisons, or demonstrations]

## Here's an example
[Optional: Practical demonstration with real-world use case]

[Additional context, gotchas, or insights]
```

### Content Guidelines

1. **Headline Format**: Start with a hashtag followed by the core concept (e.g., `#Structured outputs are more reliable than you think—if you ask right.`)

2. **Explanation Style**:
   - Be concise but complete
   - Focus on the "why" not just the "what"
   - Include practical context and real-world applicability
   - Use plain language with technical precision

3. **Code Examples**:
   - Use proper markdown code fencing with language identifiers
   - Provide concrete, runnable examples when relevant
   - Show both the problem and solution

4. **Formatting Conventions**:
   - Use blockquotes (`>`) for schema definitions, expected outputs, or emphasis
   - Use **bold** for key terms or important callouts
   - Use code blocks (` ``` `) for multi-line code
   - Use inline code (`` ` ``) for short references, variables, or technical terms

## Development Workflow

### Adding New Learning Entries

1. **Create new date file** if one doesn't exist for today:
   ```bash
   # Format: YYYY-MM-DD.md
   touch $(date +%Y-%m-%d).md
   ```

2. **Use the standard template** shown above

3. **Write clear, actionable content** that your future self will appreciate

4. **Commit with descriptive message**:
   ```bash
   git add YYYY-MM-DD.md
   git commit -m "Add Learning Log message MM/DD"
   git push
   ```

### Updating Existing Entries

- **Append to current day's file** if adding more learnings
- **Don't modify past entries** unless correcting errors
- Each day's file can contain multiple TIL items separated by clear headings

## Git Conventions

### Branch Strategy

- **Main branch**: Production-ready content
- **Feature branches**: Follow pattern `claude/[description]-[session-id]` for AI-assisted work
- Always develop on designated feature branches when specified

### Commit Message Format

Based on existing commit history:

```
Add Learning Log message MM/DD
```

- Use imperative mood ("Add" not "Added")
- Reference the date of the learning entry
- Keep messages concise and descriptive
- Examples:
  - `Add Learning Log message 11/30`
  - `Update Learning Log message 12/01 with additional examples`
  - `Fix typo in 2025-11-30.md`

### Git Operations

- **Always push to the correct branch**: Use `git push -u origin <branch-name>`
- **Create feature branches** when working on AI-assisted tasks
- **Keep commits atomic**: One logical change per commit
- **Don't amend others' commits**: Only amend your own recent commits

## Content Topics and Themes

Based on current entries, this log focuses on:

- **AI/ML Engineering**: LLM prompting, structured outputs, API usage
- **Software Development**: Best practices, design patterns, technical concepts
- **Tools and Techniques**: Practical how-tos and productivity tips
- **Problem-Solving Insights**: Lessons learned from debugging or optimization

### Quality Standards

- **Accuracy**: Verify technical details before committing
- **Clarity**: Write for your future self who may have forgotten the context
- **Completeness**: Include enough detail to be useful without re-research
- **Examples**: Provide concrete examples that demonstrate the concept
- **Attribution**: Link to sources or references when appropriate

## AI Assistant Guidelines

### When Adding New Entries

1. **Check for existing file**: Always verify if today's date file exists before creating
2. **Follow the template**: Maintain consistency with existing entry structure
3. **Match the tone**: Technical but conversational, educational but concise
4. **Preserve formatting**: Maintain the established markdown conventions
5. **Use proper git workflow**: Commit with appropriate message format

### When Modifying Content

1. **Read first**: Always read existing content before making changes
2. **Preserve voice**: Keep the personal learning journal tone
3. **Don't over-format**: Maintain simplicity; avoid excessive styling
4. **Test code examples**: Ensure any code snippets are correct and runnable
5. **Maintain chronology**: Don't reorganize or re-sort entries

### Best Practices

- **Don't create unnecessary files**: Avoid creating templates, configs, or tooling unless explicitly requested
- **Keep it simple**: This is a text-based learning log, not a complex application
- **Respect the format**: The simplicity is intentional
- **Focus on content quality**: Prioritize clear, valuable insights over elaborate formatting
- **One concept per entry**: Each TIL should focus on a single, coherent insight

## Technical Details

### File Encoding
- UTF-8 encoding for all markdown files
- Unix-style line endings (LF)

### Markdown Flavor
- GitHub-flavored markdown
- Support for code syntax highlighting
- Blockquotes for emphasis

### Dependencies
- None (pure markdown)
- .gitignore suggests future Python tooling may be added

## Future Considerations

As evidenced by the Python .gitignore file, this repository may eventually include:

- Scripts to generate indexes or search functionality
- Automated formatting or validation tools
- Static site generation for web viewing
- Search/tagging capabilities

However, the core remains simple: daily markdown files capturing technical learnings.

## Quick Reference

### File Naming
- Daily logs: `YYYY-MM-DD.md` (e.g., `2025-11-30.md`)
- Special files: `README.md`, `LICENSE`, `CLAUDE.md`

### Commit Messages
- `Add Learning Log message MM/DD`
- `Update Learning Log message MM/DD [specific change]`
- `Fix [description] in YYYY-MM-DD.md`

### Common Tasks

**Add today's learning**:
```bash
# Create/edit today's file
vim $(date +%Y-%m-%d).md
# Commit and push
git add .
git commit -m "Add Learning Log message $(date +%m/%d)"
git push
```

**Search past learnings**:
```bash
# Search for keyword across all entries
grep -r "keyword" *.md
```

**List all topics**:
```bash
# View all date-stamped files
ls -1 [0-9]*.md
```

## Contact and Collaboration

**Repository Owner**: Ezinne Udezue
**Contribution Style**: Personal learning log (primarily single-author)

---

*Last Updated: 2025-12-01*
*This guide is maintained to help AI assistants effectively contribute to and maintain this learning log.*
