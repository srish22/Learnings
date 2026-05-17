
# 1. What Is Markdown?

| What Is Markdown? | Why Developers Use It | Common File Names |
| :--- | :--- | :--- |
| - Lightweight text formatting language<br><br>- Used for documentation<br><br>- Used for technical notes<br><br>- Used for README files<br><br>- Used for developer wikis<br><br>- Used for GitHub repositories | - Simple syntax<br><br>- Readable as plain text<br><br>- GitHub compatible<br><br>- Lightweight<br><br>- Easy to maintain<br><br>- AI-friendly | - `README.md`<br><br>- `notes.md`<br><br>- `setup-guide.md`<br><br>- `cli-cheatsheet.md` |

<br><br><br>

---

# 2. Syntax Cheat Sheet

| Feature | Syntax | Example / Notes |
|---|---|---|
| Main Heading | `# Heading` | `# Joule Notes` |
| Sub Heading | `## Heading` | `## Setup` |
| Smaller Heading | `### Heading` | `### Install` |
| Bullet List | `- item` | `- install node` |
| Numbered List | `1. item` | `1. Login` |
| Link | `[text](url)` | `[Google](https://google.com)` |
| Image | `![alt](path)` | `![Setup](images/setup.png)` |
| Table | `| col | col |` | Best for quick revision |
| Blockquote | `> note` | `> Important note` |
| Horizontal Line | `---` | Section separator |
| Empty line |` <br> `| empty space line |
| Bold | `**text**` | `**Important**` |
| Italic | `*text*` | `*note*` |
| Inline Code | `` `code` `` | `` `joule deploy` `` |
| Code Block | ```` ```lang ```` | Use language type for syntax highlighting |

---

## Code Block Examples

| Type | Example |
|---|---|
| Bash | ```bash\nnpm install\n``` |
| JavaScript | ```javascript\nconsole.log("hello");\n``` |
| JSON | ```json\n{\n  "name": "test"\n}\n``` |

---

## Images Best Practices

| Topic | Recommendation |
|---|---|
| Recommended Structure | `images/setup.png` |
| Good Path Example | `![Setup](images/setup.png)` |
| Avoid | Local machine paths like `C:\\Users\\...` |
| Naming Style | Use `kebab-case` → `setup-guide.png` |
| Folder Structure | Keep all images inside `/images` folder |

---

## Table Best Use Cases

| Use Case | Why Useful |
|---|---|
| Command Cheatsheets | Quick scanning |
| Comparisons | Easy understanding |
| Role Mappings | Compact format |
| Revision Notes | ADHD-friendly |
| Summaries | Less scrolling |

---

## Code Block Best Practices

| Recommendation | Why |
|---|---|
| Specify language type | Enables syntax highlighting |
| Use `bash` for commands | Cleaner terminal rendering |
| Use `json` for payloads | Better readability |
| Use code blocks for commands | Easier copy-paste |

---

## Common Language Types

| Type | Usage |
|---|---|
| `bash` | terminal commands |
| `javascript` | JS code |
| `json` | payloads/config |
| `yaml` | configs |
| `sql` | database queries |

---

## Blockquote Example

| Syntax | Output |
|---|---|
| `> Important note` | > Important note |


<br><br><br>

---

# 3. Useful Editors

| Tool | Purpose |
|---|---|
| VS Code | Best overall |
| Cursor | AI-assisted editing |
| GitHub | Viewing/rendering |
| Obsidian | Personal notes |

<br>

### Preview - VS Code Shortcut

```text
Ctrl + Shift + V
```

###  Preview - Github  

```text
Edit --> edit/preview
```

<br><br><br>

---

# 4. Best Practices For Technical Notes

| Keep Notes Concise | Use Consistent Structure | Use Tables For Revision |
| :--- | :--- | :--- |
| - Quick to scan<br><br>- Easy to revise<br><br>- Implementation-focused<br><br>- Avoid huge copied documentation<br><br>- Avoid long paragraphs | - Follow fixed structure<br><br>- What<br><br>- Why<br><br>- Commands<br><br>- Workflow<br><br>- Common Issues<br><br>- Links | - Best for commands<br><br>- Best for comparisons<br><br>- Best for mappings<br><br>- Reduces scrolling<br><br>- Faster understanding |

---

| Use Code Blocks For Commands | Keep Official Documentation Links | Summary |
| :--- | :--- | :--- |
| - Wrap commands inside code blocks<br><br>- Easier copy-paste<br><br>- Better readability<br><br>- Syntax highlighting support | - Notes should summarize concepts<br><br>- Official docs remain source of truth<br><br>- Keep important links in notes | - Prioritize clarity over completeness<br><br>- Make notes quick to revisit<br><br>- Optimize for low cognitive load<br><br>- Build reusable revision system |




