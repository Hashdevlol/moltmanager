# MoltManager 🦁

<p align="center">
 
</p>

<p align="center">
  <strong>Manage your AI agent zoo, locally</strong>
</p>

<p align="center">
  A local-first CLI tool to create, organize, and share AI agent personas (moltbots).<br>
  Inspired by <a href="https://moltbook.com">Moltbook</a>, but built for your terminal.
</p>

<p align="center">
  <em>No cloud • No API calls • No subscriptions • Just your agents, your way</em>
</p>

---

## 🎬 See It In Action

```bash
# Create your first AI agent
$ molt create python-tutor "You are a patient Python teacher who explains concepts simply with clear examples."

Created moltbot: python-tutor
ID: 1
Model: claude-sonnet-4

# Create more with tags
$ molt create code-reviewer "Senior engineer who reviews for bugs and best practices." --tag coding

# List your collection
$ molt list

Your Moltbots:

1. python-tutor [education]
   You are a patient Python teacher who explains concepts...
2. code-reviewer [coding]
   Senior engineer who reviews for bugs and best practices...

# Copy a prompt to use in ChatGPT/Claude
$ molt copy python-tutor | clip

# System prompt copied! Now paste it into ChatGPT and start chatting!
```

---

## 🤔 Why MoltManager?

**The Problem:**
You've crafted the perfect system prompt for Claude to be your Python tutor. A week later, you need it again but can't remember exactly how you worded it. You've lost dozens of great prompts in chat history.

**The Solution:**
MoltManager lets you save, organize, and instantly retrieve your best AI agent personas. Think of it as a **prompt library** for your terminal.

### What Makes It Different?

- 🏠 **Local-First** - Your prompts stay on your machine, private and secure
- 🚀 **Instant Access** - Copy any prompt in 2 seconds
- 🏷️ **Tagged Organization** - Find prompts by category
- 📤 **Shareable** - Export your best agents to share with friends
- 💎 **Zero Dependencies** - Pure Node.js, nothing else
- 🎯 **Terminal Native** - Built for developers who live in the terminal

---

## ✨ Features

### Core Features
- ✅ **Create Agents** - Define AI personas with custom system prompts
- ✅ **Tag & Organize** - Categorize agents by purpose (coding, writing, education)
- ✅ **Quick Copy** - Instantly copy prompts to use in any AI chat
- ✅ **Search** - Find agents by name, tags, or prompt content
- ✅ **Import/Export** - Share agents with teammates or back up your collection

### Advanced Features
- 🔍 **Full-Text Search** - Search across all agent prompts
- 📊 **Statistics** - See your most-used agents
- 🏷️ **Tag Management** - View and filter by all tags
- 💾 **Backup/Restore** - Export your entire collection as JSON
- 🔄 **Edit & Rename** - Update agents as your needs evolve

---

## 🚀 Quick Start

### Installation

**npm (Recommended):**
```bash
npm install -g moltmanager
```

**Windows:**
Download `install.bat` from [releases](https://github.com/Hashdevlol/moltmanager/releases) and double-click it.

**From Source:**
```bash
git clone https://github.com/Hashdevlol/moltmanager.git
cd moltmanager
npm link
```

### Create Your First Agent

```bash
# A Python teaching assistant
molt create python-tutor "You are a patient Python teacher who explains concepts simply, provides clear code examples, and encourages learning through practice." --tag education --tag python

# A code reviewer
molt create code-reviewer "You are a senior software engineer with 10+ years of experience. You review code for bugs, security vulnerabilities, performance issues, and best practices. You provide constructive, detailed feedback." --tag coding --tag review

# A creative writing coach
molt create writer-coach "You are an experienced creative writing instructor who helps improve storytelling, character development, dialogue, and prose. You provide specific, actionable feedback." --tag writing --tag creative
```

### Use Your Agents

```bash
# List all agents
molt list

# Filter by tag
molt list --tag coding

# Copy a prompt to clipboard (Windows)
molt copy python-tutor | clip

# Copy a prompt to clipboard (Mac)
molt copy python-tutor | pbcopy

# Copy a prompt to clipboard (Linux)
molt copy python-tutor | xclip -selection clipboard

# View full details
molt show python-tutor
```

---

## 📚 Command Reference

### Create & Manage

```bash
# Create new agent
molt create <name> "<system-prompt>" [--tag <tag>] [--model <model>]

# List agents
molt list                    # All agents
molt list --tag coding       # Filter by tag

# View details
molt show <name>             # Full agent details
molt info <name>             # Same as show

# Modify agents
molt edit <name> "<new-prompt>"
molt rename <old-name> <new-name>
molt delete <name>
```

### Use Your Agents

```bash
# Copy system prompt (pipe to clipboard)
molt copy <name>

# Example with clipboard:
molt copy python-tutor | clip         # Windows
molt copy python-tutor | pbcopy       # macOS
molt copy python-tutor | xclip -selection clipboard  # Linux
```

### Search & Organize

```bash
molt search <query>          # Search by name, tags, or content
molt tags                    # List all tags
```

### Import/Export

```bash
molt export <name>           # Export single agent as JSON
molt export <name> > agent.json

molt import <file>           # Import agent from JSON
molt import agent.json

molt backup                  # Export all agents
molt backup > backup.json
```

### Utilities

```bash
molt stats                   # View statistics
molt storage                 # Show storage location
molt version                 # Show version
molt help                    # Show help
```

---

## 💡 Real-World Examples

### For Software Developers

```bash
# Python expert
molt create python-expert "You are a Python expert who writes clean, idiomatic code following PEP 8. You explain complex concepts clearly and suggest best practices." --tag python --tag coding

# JavaScript guru
molt create js-guru "You are a JavaScript/TypeScript expert specializing in modern ES6+, React, and Node.js. You write performant, maintainable code." --tag javascript --tag coding

# SQL optimizer
molt create sql-optimizer "You are a database expert who writes efficient SQL queries, explains execution plans, and suggests optimizations." --tag database --tag sql

# Bug detective
molt create bug-hunter "You are an expert debugger. You ask clarifying questions, analyze error messages, suggest debugging strategies, and help identify root causes." --tag debugging
```

### For Content Creators

```bash
# Blog post editor
molt create blog-editor "You are a professional blog editor who improves clarity, flow, and engagement while preserving the author's voice. You fix grammar and suggest structural improvements." --tag writing --tag editing

# Social media expert
molt create social-media "You are a social media expert who crafts engaging posts, suggests hashtags, and optimizes content for each platform (Twitter, LinkedIn, Instagram)." --tag marketing --tag social

# Title generator
molt create title-gen "You are a headline expert who creates attention-grabbing, SEO-friendly titles. You suggest 10 variations for every topic." --tag marketing --tag seo
```

### For Students & Educators

```bash
# Math tutor
molt create math-tutor "You are a patient math tutor who breaks down problems step-by-step, explains the reasoning, and provides practice problems." --tag education --tag math

# Essay coach
molt create essay-coach "You are an academic writing coach who helps structure essays, develop arguments, and cite sources properly. You provide detailed, constructive feedback." --tag education --tag writing

# Study buddy
molt create study-buddy "You are a study companion who creates flashcards, suggests mnemonics, and quizzes on topics. You make learning engaging and fun." --tag education
```

### For Productivity

```bash
# Meeting summarizer
molt create meeting-notes "You are an executive assistant who takes meeting notes, extracts action items, and creates clear summaries with next steps." --tag productivity

# Email drafter
molt create email-writer "You are a professional communication expert who writes clear, concise, polite emails for business contexts." --tag productivity --tag communication

# Task breaker
molt create task-breaker "You are a project manager who breaks large tasks into small, actionable steps with time estimates." --tag productivity --tag planning
```

---

## 🎯 Workflow Tips

### The Copy-Paste Workflow

1. Create agents for your common tasks
2. When you need one, copy the prompt:
   ```bash
   molt copy code-reviewer | clip
   ```
3. Open ChatGPT/Claude
4. Paste the system prompt
5. Start your conversation!

### Organizing with Tags

Use consistent tags across agents:

```bash
# By skill area
--tag coding --tag writing --tag design --tag marketing

# By use case
--tag education --tag productivity --tag debugging --tag review

# By language
--tag python --tag javascript --tag sql

# Combine tags for power
molt create api-designer "..." --tag coding --tag design --tag review
```

### Sharing with Teams

```bash
# Export your best agents
molt export code-reviewer > code-reviewer.json
molt export python-tutor > python-tutor.json

# Share files with your team

# They import:
molt import code-reviewer.json
```

### Backup Strategy

```bash
# Regular backups
molt backup > ~/Dropbox/moltmanager-backup-$(date +%Y%m%d).json

# Or add to your dotfiles repo
molt backup > ~/dotfiles/moltmanager-backup.json
```

---

## 📂 Storage

### Location

Your agents are stored locally:

- **Unix/Linux/Mac:** `~/.moltmanager/moltbots.json`
- **Windows:** `C:\Users\YourName\.moltmanager\moltbots.json`

### Format

Plain, readable JSON:

```json
[
  {
    "id": 1,
    "name": "python-tutor",
    "systemPrompt": "You are a patient Python teacher...",
    "tags": ["education", "python"],
    "model": "claude-sonnet-4",
    "temperature": 0.7,
    "created": "2026-01-30T12:00:00.000Z",
    "lastUsed": "2026-01-30T14:30:00.000Z"
  }
]
```

### Benefits

- ✅ **Human-readable** - Edit in any text editor
- ✅ **Portable** - Copy folder to any machine
- ✅ **Git-friendly** - Version control your agents
- ✅ **No database** - Just a simple file
- ✅ **Privacy** - Stays on your machine

---

## 🎨 Philosophy

MoltManager is built on these principles:

### 1. 🏠 Local-First
Your prompts are **your intellectual property**. They stay on your machine, always accessible, never locked in a cloud service.

### 2. 🔓 No Lock-In
Plain JSON files mean you're never locked in. Export anytime, import anywhere, or edit manually if you want.

### 3. ⚡ Instant Access
No loading screens, no authentication, no network calls. Your agents are available in milliseconds.

### 4. 🎯 Do One Thing Well
MoltManager manages prompts. It doesn't try to be a chatbot, an API client, or a prompt engineering IDE. It just stores and retrieves prompts really well.

### 5. 🤝 Share Without Barriers
Export a single agent or your entire collection. Share with teammates, contribute to communities, or keep them private. Your choice.

---

## 🚧 What MoltManager Is NOT

To set clear expectations:

- ❌ **Not a chatbot** - It doesn't make API calls to Claude/OpenAI
- ❌ **Not a conversation manager** - It doesn't store chat history
- ❌ **Not cloud-based** - Everything is local
- ❌ **Not a prompt engineering tool** - No testing, no iterations, just storage
- ❌ **Not a marketplace** - No central registry (though you can share exports)

**MoltManager is a prompt library.** That's it. That's the whole point.

---

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.

### What We Welcome

- 🐛 Bug fixes
- 📚 Documentation improvements
- ✨ Feature requests (that align with our philosophy)
- 🎨 UI/UX improvements

### What We Won't Accept

- ☁️ Cloud sync features
- 🤖 API integrations (keep it local)
- 💳 Paid features or subscriptions
- 📊 Analytics or telemetry
- 🖥️ GUI applications

---

## 🗺️ Roadmap

Potential future features (not committed):

- [ ] Conversation templates
- [ ] Moltbot categories/folders
- [ ] Custom model parameters per agent
- [ ] Community export gallery (opt-in)
- [ ] Shell completion scripts
- [ ] Fuzzy search

**Will NOT add:**
- API integrations
- Cloud features
- Subscription model
- Actual chat functionality

---

## 🐛 Troubleshooting

### Command not found: molt

**Solution:** Add npm global bin to PATH:

```bash
# Check npm global path
npm config get prefix

# Add to PATH (add to your shell config to make permanent)
export PATH="$(npm config get prefix)/bin:$PATH"
```

### Where is my data?

```bash
molt storage
```

### Reset everything

```bash
# Unix/Linux/Mac
rm -rf ~/.moltmanager

# Windows
rmdir /s %USERPROFILE%\.moltmanager
```

### Import fails with "already exists"

Some imports include overwrite protection:

```bash
# Force overwrite during import
# (Note: Current version doesn't support this flag yet)
# Workaround: Delete the existing agent first
molt delete existing-name
molt import agent.json
```

---

## 📊 Project Stats

- **Package Size:** ~15KB
- **Dependencies:** 0 (zero!)
- **Platforms:** Windows, macOS, Linux
- **Node.js:** >=14.0.0
- **License:** MIT

---

## 🙏 Acknowledgments

### Inspiration

- **[Moltbook](https://moltbook.com)** - The social media for AI agents that inspired this project
- **Local-first movement** - Building software that respects user data ownership
- **The Prompt Engineering community** - For showing us how powerful good prompts are

### Built With

- Pure Node.js (no dependencies!)
- Love for the command line
- Respect for user privacy

---

## 📝 License

MIT License - see [LICENSE](LICENSE) for details.

**Copyright (c) 2026 [@0xHashlol](https://twitter.com/0xHashlol)**

You can use this for anything, just keep the license notice.

---

## 🔗 Links

- **npm:** [npmjs.com/package/moltmanager](https://www.npmjs.com/package/moltmanager)
- **GitHub:** [github.com/Hashdevlol/moltmanager](https://github.com/Hashdevlol/moltmanager)
- **Issues:** [github.com/Hashdevlol/moltmanager/issues](https://github.com/Hashdevlol/moltmanager/issues)
- **Moltbook:** [moltbook.com](https://moltbook.com)
- **Twitter:** [@0xHashlol](https://twitter.com/0xHashlol)

---

## ⭐ Show Your Support

If MoltManager helps you:

- ⭐ **Star this repo**
- 🐦 **Tweet about it** - Tag @0xHashlol
- 📝 **Write about it** - Blog posts welcome!
- 🦁 **Share your agents** - Export and share cool moltbots
- 💬 **Tell developers** - Word of mouth is the best

---

## 🎉 Join the Community

Using MoltManager? We'd love to hear from you!

- Share your favorite agents on Twitter with #MoltManager
- Open issues for bugs or feature requests
- Contribute examples to the docs
- Help answer questions from other users

---

<p align="center">
  <strong>🦁 Manage your AI agent zoo, locally 🦁</strong>
</p>

<p align="center">
  <em>Built with ❤️ by <a href="https://twitter.com/0xHashlol">@0xHashlol</a></em><br>
  <em>Inspired by <a href="https://moltbook.com">Moltbook</a></em>
</p>

<p align="center">
  <sub>No cloud • No API calls • No lock-in • Just your agents</sub>
</p>
