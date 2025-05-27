# Universal AI Project Navigation System
# =========================================
# This file enables any AI to rapidly understand and contribute to any project
# Follow this exact workflow regardless of project domain or complexity

## 🧠 UNIVERSAL AI PROTOCOL (Follow This Decision Tree)

### STEP 1: Context Acquisition (Read These 3 Files)
1. `PROJECT_PLAN.md` - Project overview, architecture, roadmap
2. `WIP.md` - Current work, problems, solutions, task status  
3. `CHANGE_LOG.md` - Recent decisions, pivots, major changes

### STEP 2: Work Management Check
- **First time setup**: See `TASKS_MD_SETUP.md` for complete Docker installation guide
- **If Tasks.md board exists**: Check `http://localhost:8080` for active work
- **If localhost:8080 doesn't load**: Run `docker start tasks.md` or follow setup guide
- **If no Docker available**: Use WIP.md checklist for task tracking
- **If Docker down**: Continue with file-based task management in WIP.md

### STEP 3: Determine Session Type
- **Continuing work?** → Follow "Existing Session" workflow
- **New feature/area?** → Follow "New Feature" workflow  
- **Missing docs?** → Follow "Bootstrap" workflow

## 📋 WORKFLOW TEMPLATES

### 🔄 Existing Session Workflow
1. **Orient**: What was the last session's focus and outcome?
2. **Assess**: What's the next logical step or highest priority?
3. **Work**: Execute using established patterns and tools
4. **Document**: Update WIP.md with progress, problems, solutions
5. **Archive**: Move completed work details to ARCHIVE/ 
6. **Handoff**: Update CHANGE_LOG.md if major decisions made

### 🆕 New Feature Workflow  
1. **Research**: Review existing architecture and patterns
2. **Plan**: Create feature folder with WIP.md if needed
3. **Question**: Ask clarifying questions before building
4. **Build**: Follow established technical patterns
5. **Document**: Update both feature WIP.md and project WIP.md
6. **Archive**: Move implementation details to ARCHIVE/ when complete

### 🏗️ Bootstrap Workflow (Missing Documentation)
1. **Create PROJECT_PLAN.md**: Overview, architecture, goals
2. **Create WIP.md**: Current state, immediate next steps
3. **Create CHANGE_LOG.md**: Note bootstrap date and initial state
4. **Create ARCHIVE/ structure**: Set up cold storage directories
5. **Set up task management**: Follow TASKS_MD_SETUP.md or use WIP.md checklist

## 📂 INFORMATION TEMPERATURE ARCHITECTURE

### 🔥 HOT INFORMATION (Always Read - <5 min total)
```
WIP.md              # Current focus, next steps, active blockers
PROJECT_PLAN.md     # Vision, current architecture, roadmap (current sections only)
CHANGE_LOG.md       # Last 30 days of decisions and changes
```
**Max Size**: 2 pages each - **ENFORCE LIMITS**

### 🔸 WARM INFORMATION (Read When Relevant)
```
README.md           # Technical overview, current patterns
DEPENDENCIES.md     # External service status, API changes
TASKS_MD_SETUP.md   # Task management setup guide (when needed)
```

### ❄️ COLD INFORMATION (Reference When Needed)
```
ARCHIVE/
├── completed-features/     # Detailed implementation notes
├── failed-experiments/     # What didn't work and why
├── technical-research/     # Deep dives, vendor analysis
└── historical-decisions/   # Complete context for old choices

DECISIONS_ARCHIVE/
├── [YEAR-QUARTER]/        # Aged decisions with full context
└── architecture-changes/   # Major system evolution notes
```

## 🔄 INFORMATION LIFECYCLE MANAGEMENT

### Automatic Archival Rules
1. **Work completes** → Move details from WIP.md to ARCHIVE/completed-features/
2. **Decision ages 30 days** → Move from CHANGE_LOG.md to DECISIONS_ARCHIVE/
3. **Hot docs exceed 2 pages** → Archive oldest sections automatically
4. **Feature finished** → Implementation notes → ARCHIVE/

### Archive Before Every Session End
- [ ] Move completed work details to appropriate ARCHIVE/ folder
- [ ] Check WIP.md size - archive if over 2 pages
- [ ] Update CHANGE_LOG.md with session decisions
- [ ] Ensure hot information stays actionable and current

## 🎯 BEHAVIORAL PRINCIPLES

### CONTEXT EFFICIENCY
- **Start with hot information only** - read 3 files maximum
- **Request archives explicitly** when historical context needed
- **Explain approach before significant changes**
- **Propose specific next steps** rather than general direction

### PROACTIVE CONFIRMATION
- **Identify assumptions** and confirm with user
- **Ask clarifying questions** when context is ambiguous  
- **Explain what context might be missing** from hot information
- **Confirm archive reading** before diving into cold storage

### SELF-MAINTAINING SYSTEM
- **Archive automatically** as part of completing work
- **Maintain size limits** on hot documents
- **Reference don't copy** information between documents
- **Single source of truth** for each piece of information

## 🚨 CRITICAL RULES

1. **HOT DOCS HAVE SIZE LIMITS** - Archive when exceeded
2. **NEVER DUPLICATE INFORMATION** - Use references to archives
3. **ARCHIVE IMMEDIATELY** when work completes
4. **ASK BEFORE READING ARCHIVES** - Don't assume you need historical context

---

**Remember**: The system's power is in what it doesn't make you read. Efficient context management enables faster iteration and better results.

## 📋 QUICK START CHECKLIST

**For AI starting in new project:**
- [ ] Read this file first
- [ ] Read PROJECT_PLAN.md (if exists)
- [ ] Read WIP.md (if exists)  
- [ ] Read CHANGE_LOG.md (if exists)
- [ ] Check Tasks.md board at localhost:8080 (follow TASKS_MD_SETUP.md if needed)
- [ ] If any missing → Start Bootstrap Workflow
- [ ] If all exist → Start Existing Session Workflow 