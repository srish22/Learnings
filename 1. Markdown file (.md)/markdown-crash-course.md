# Markdown (.md) Crash Course

> Quick revision notes for writing clean and developer-friendly markdown documentation.

---

# 1. What Is Markdown?

Markdown is a lightweight text formatting language used for:
- documentation
- technical notes
- README files
- developer wikis
- GitHub repositories

---

## Why Developers Use It

- simple syntax
- readable as plain text
- GitHub compatible
- lightweight
- easy to maintain
- AI-friendly

---

## Common File Names

```text
README.md
notes.md
setup-guide.md
cli-cheatsheet.md
```

---

# 2. Syntax 

## Headings

```markdown
# Main Heading
## Sub Heading
### Smaller Heading
```

## Lists

### Bullet List

```markdown
- item 1
- item 2
- item 3
```

---

### Numbered List

```markdown
1. Step one
2. Step two
3. Step three
```

---

## Code Blocks

Most important feature for developer notes.

---

### Syntax

````markdown
```bash
npm install
```
````

---

### Examples

-  Bash

```bash
npm install
```

---

- JavaScript

```javascript
console.log("hello");
```

---

- JSON

```json
{
  "name": "test"
}
```

---

### Best Practice

Always specify language type:
- bash
- javascript
- json
- yaml
- sql

---

## Inline Code

### Syntax

```markdown
Use `joule deploy`
```

---

### Example

Use `joule deploy`

---

## Links

### Syntax

```markdown
[Google](https://google.com)
```

---

### Best Practice

Keep:
- official docs
- installation links
- reference links

inside notes.

---

## Images

### Syntax

```markdown
![Image Name](images/setup.png)
```

---

### Recommended Structure

```text
JOULE/
│
├── images/
│   ├── setup.png
│   └── deploy.png
│
├── setup.md
└── cli-cheatsheet.md
```

---

### Important Rule

Use:
- relative paths

Avoid:
- local machine paths

---

### Example

```markdown
![Setup](images/setup.png)
```

---

## Tables

Very useful for quick revision notes.

---

### Syntax

```markdown
| Command | Purpose |
|---|---|
| joule login | login |
| joule deploy | deploy |
```

---

### Example

| Command | Purpose |
|---|---|
| `joule login` | Login |
| `joule deploy` | Deploy |

---

## Blockquotes

Used for:
- warnings
- important notes
- reminders

---

### Syntax

```markdown
> Important note
```

---

### Example

> Always run lint before deployment.

---

## Horizontal Separator

### Syntax

```markdown
---
```

---

## Text Formatting

### Bold

```markdown
**bold**
```
---

### Italic

```markdown
*italic*
```

---

## Markdown Preview

### VS Code Shortcut

```text
Ctrl + Shift + V
```

---

# Useful Editors

| Tool | Purpose |
|---|---|
| VS Code | Best overall |
| Cursor | AI-assisted editing |
| GitHub | Viewing/rendering |
| Obsidian | Personal notes |

---

## GitHub Markdown Rendering

GitHub automatically renders:
- headings
- tables
- code blocks
- images
- links

This is why most repositories have:

```text
README.md
```

---

# Best Practices For Technical Notes

## Keep Notes Concise

Good notes:
- quick to scan
- easy to revise
- implementation-focused

Avoid:
- huge copied documentation
- long paragraphs

---

## Use Consistent Structure

Recommended pattern:

```text
What
Why
Commands
Workflow
Common Issues
Links
```

---

## Use Tables For Revision

Tables are excellent for:
- commands
- comparisons
- mappings

---

## Use Code Blocks For Commands

Always wrap commands inside code blocks.

---

## Keep Official Documentation Links

Notes should:
- summarize concepts
- not replace official docs

---



---


# Summary

