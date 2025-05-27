# AI Helper Template
# ==================
# Universal AI collaboration system for rapid project onboarding and efficient task management

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/axia-llc/ai-helper-template.svg)](https://github.com/axia-llc/ai-helper-template/stargazers)

## 🎯 What is this?

The AI Helper Template is a proven system that enables any AI assistant to rapidly understand and contribute to any project. Instead of spending 20+ minutes explaining your project context every session, AI can get oriented in under 5 minutes and immediately start productive work.

**Perfect for:**
- Solo developers working with AI assistants (Cursor, ChatGPT, Claude)
- Small teams needing consistent AI collaboration patterns
- Anyone frustrated with repeatedly explaining project context to AI
- Projects requiring systematic documentation and decision tracking

## ⚡ Quick Start

```bash
# 1. Clone the template
git clone https://github.com/axia-llc/ai-helper-template.git
cd ai-helper-template

# 2. Copy to your project
cp -r * /path/to/your/project/
cd /path/to/your/project

# 3. Activate AI integration
mv template-cursorrules.md .cursorrules

# 4. Customize for your project
# Edit PROJECT_PLAN.md with your project details
# Edit WIP.md with current status
# Edit CHANGE_LOG.md with initial context

# 5. Start collaborating with AI!
# Open in Cursor or your preferred AI-enabled editor
```

**That's it!** Any AI opening your project will now:
- Understand your project context in <5 minutes
- Follow established collaboration patterns
- Work through confirmed task checklists
- Maintain organized documentation automatically

## 🚀 Live Examples

See the template in action across different project types:

### **[Web App Development](examples/web-app-example/)**
React/Node.js project with authentication, database integration, and deployment workflows.

### **[Research Projects](examples/research-project-example/)**
Academic research with literature review, data analysis, and publication workflows.

### **[Content Creation](examples/content-creation-example/)**
Documentation, courses, and marketing content with research, writing, and publishing workflows.

### **[Legal Work](examples/legal-team-example/)**
Contract analysis, document drafting, and legal research with compliance and review workflows.

## 🧠 How It Works

### **Information Temperature System**
- **🔥 Hot Files** (Always read first): PROJECT_PLAN.md, WIP.md, CHANGE_LOG.md
- **🔶 Warm Files** (Read when working): Task files, README.md, documentation
- **🧊 Cold Files** (Reference only): ARCHIVE/, completed work, historical decisions

### **AI Collaboration Pattern**
1. **Context Acquisition**: AI reads hot files in <5 minutes
2. **Task Planning**: AI proposes 3-5 step checklists
3. **User Confirmation**: "Here are my next steps. Shall I proceed?"
4. **Execution**: AI works through confirmed checklist
5. **Progress Tracking**: Real-time updates in WIP.md
6. **Archival**: Completed work moves to ARCHIVE/

### **Self-Maintaining Documentation**
- Automatic size limits prevent information overload
- Completed work archives automatically
- Decisions tracked with 30-day rolling window
- Single source of truth for all project information

## 📋 Template Contents

### **Core Files**
- **`.cursorrules`** - AI's entry point and behavior guidelines
- **`UNIVERSAL_AI_INSTRUCTIONS.md`** - Complete AI workflow and decision tree
- **`PROJECT_PLAN.md`** - Project vision, architecture, and roadmap
- **`WIP.md`** - Current work status and active checklists
- **`CHANGE_LOG.md`** - Recent decisions and changes (30-day window)

### **Setup & Integration**
- **`TASKS_MD_SETUP.md`** - Optional visual task board setup (Docker)
- **`CONTRIBUTING.md`** - Guidelines for improving the template
- **`LICENSE`** - MIT license for open source use

### **Examples**
- **`examples/web-app-example/`** - Full web application workflow
- **`examples/research-project-example/`** - Academic research patterns
- **`examples/content-creation-example/`** - Content and documentation workflows
- **`examples/legal-team-example/`** - Legal analysis and drafting workflows

## 🎯 Key Benefits

### **For Developers**
- **Faster AI onboarding**: 5 minutes vs. 20+ minutes per session
- **Consistent collaboration**: Established patterns across all AI interactions
- **Better documentation**: Self-maintaining project knowledge base
- **Reduced context switching**: All project state visible in hot files

### **For Teams**
- **Knowledge retention**: Important decisions and learnings preserved
- **Smooth handoffs**: Any team member (or AI) can quickly understand project state
- **Systematic approach**: Consistent documentation and decision tracking
- **Scalable patterns**: Works for projects of any size or complexity

### **For AI Assistants**
- **Rapid orientation**: Clear entry point and context hierarchy
- **Structured workflows**: Established patterns for different types of work
- **Confirmation protocols**: Built-in checkpoints prevent overreach
- **Progress tracking**: Clear visibility into current work and next steps

## 🔧 Task Management Options

### **Option A: Visual Board (Recommended)**
Set up a beautiful Kanban board at `localhost:8080`:
```bash
# Follow the complete setup guide
cat TASKS_MD_SETUP.md
```
- Works on macOS, Windows, Linux
- Rich markdown support in task descriptions
- Visual progress tracking

### **Option B: File-Based (No Dependencies)**
Use the built-in checklist system in WIP.md:
- No Docker or additional tools required
- Fully functional for most workflows
- Perfect for simple projects or restricted environments

## 🌟 Success Stories

> "Cut my AI onboarding time from 30 minutes to 3 minutes. Game changer for solo development." - *Web Developer*

> "Finally, a system that keeps AI context organized. No more explaining the same project details every session." - *Research Scientist*

> "The checklist-driven confirmation prevents AI from going off track. Much more productive collaboration." - *Content Creator*

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ways to help:**
- Report bugs or suggest improvements
- Add new example implementations
- Improve documentation and guides
- Share your success stories and use cases

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- **GitHub Repository**: [axia-llc/ai-helper-template](https://github.com/axia-llc/ai-helper-template)
- **Issues & Feature Requests**: [GitHub Issues](https://github.com/axia-llc/ai-helper-template/issues)
- **Discussions**: [GitHub Discussions](https://github.com/axia-llc/ai-helper-template/discussions)

---

**Made with ❤️ by [Axia LLC](https://axia-llc.com)** - Empowering efficient AI collaboration across all project domains.

*Transform your AI collaboration from chaotic to systematic. Start using the AI Helper Template today!*
