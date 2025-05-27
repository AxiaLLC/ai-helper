# Tasks.md Board Setup Instructions
# =================================
# Complete setup guide for visual task management

## 🎯 Purpose
Tasks.md provides a visual Kanban board using markdown files, accessible at `http://localhost:8080`. This integrates with the WIP.md system for comprehensive task tracking.

## 🔍 Quick Check
**Is Tasks.md already running?**
- Try opening `http://localhost:8080` in your browser
- If it loads → you're ready to go
- If it doesn't load → follow setup below

---

## 🏗️ COMPLETE SETUP (From Scratch)

### Step 1: Check Docker Installation
```bash
docker --version
```

**If Docker is not installed:**

#### On macOS:
```bash
# Install Homebrew if not already installed
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Docker
brew install --cask docker

# Start Docker Desktop
open /Applications/Docker.app
```

#### On Windows:
1. Download Docker Desktop from https://docker.com/products/docker-desktop
2. Run the installer
3. Restart computer if prompted
4. Start Docker Desktop

#### On Linux:
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install docker.io docker-compose
sudo systemctl start docker
sudo systemctl enable docker

# Add user to docker group
sudo usermod -aG docker $USER
# Log out and back in for group changes to take effect
```

### Step 2: Set Up Tasks.md Board
```bash
# Create project tracker directory with port-based naming
mkdir -p project-tracker-local-8080

# Create Kanban board structure
# Note: Documentation uses aliases like [Backlog], [In Progress], [Done] etc. for future-proof references
mkdir -p project-tracker-local-8080/{01\ Backlog,02\ In\ Progress,03\ Review,04\ Waiting,05\ Done,06\ Archive}

# Pull and run Tasks.md container with descriptive naming
docker run -d \
  --name tasks-md-8080 \
  -p 8080:8080 \
  -v $(pwd)/project-tracker-local-8080:/tasks/ \
  --restart unless-stopped \
  baldissaramatheus/tasks.md
```

### Step 2b: Multiple Project Trackers (Optional)
Use the included management script for easy multi-tracker setup:

```bash
# Make script executable
chmod +x manage-project-trackers.sh

# Create additional trackers
./manage-project-trackers.sh create 8081 $(pwd)/project-tracker-local-8081
./manage-project-trackers.sh create 8082 /path/to/global-project-tracker-local-8082

# List all trackers
./manage-project-trackers.sh list

# Manage individual trackers
./manage-project-trackers.sh stop 8081
./manage-project-trackers.sh start 8081
```

**Note**: The Tasks.md application automatically detects your folder structure. Each folder becomes a lane (column) and each .md file becomes a task card.

### Step 3: Verify Setup
1. Wait 30 seconds for container to start
2. Open `http://localhost:8080` in browser
3. You should see Kanban board with 5 columns: Backlog, In Progress, Waiting, Review, Done

---

## 📋 RICH TASK PLANNING (Key Feature)

### **Full Markdown Support**
Tasks.md supports complete markdown formatting in each task file:
- ✅ **Interactive checklists** (`- [ ]` syntax)
- ✅ **Headers, code blocks, links**
- ✅ **Detailed context and research**
- ✅ **AI planning sections**
- ✅ **Progress tracking**

### **Hybrid Information Architecture**
**Task Files (Warm Information)**:
- Complete task context and background
- Detailed checklists and sub-tasks
- AI's proposed approach and plan
- Research links and technical details
- Success criteria and testing steps

**WIP.md (Hot Information)**:
- Current progress on active tasks
- Session-specific updates and blockers
- Quick links to active task files

### **Enhanced Task Template**
```markdown
# [Task Title]

**Category**: Infrastructure | Backend | Frontend | Testing | Documentation
**Priority**: High | Medium | Low  
**Epic**: [Project phase or major feature]
**Effort**: 1-2 hours | 1 day | 1 week
**Dependencies**: [What's needed before starting]

## Description
[Clear description of what needs to be done]

## AI Proposed Approach
- [ ] [Step 1: Specific action]
- [ ] [Step 2: Specific action]
- [ ] [Step 3: Specific action]
- [ ] [Step 4: Specific action]

## Context & Research
[Background information, links, technical details, discoveries]

## Success Criteria
- [ ] [Specific measurable outcome 1]
- [ ] [Specific measurable outcome 2]
- [ ] [Specific measurable outcome 3]

## Progress Log
**[Date]**: [Brief update on progress]
**[Date]**: [Brief update on progress]
```

---

## 🔄 DAILY OPERATIONS

### Starting Tasks.md (if stopped)
```bash
docker start tasks.md
```

### Stopping Tasks.md
```bash
docker stop tasks.md
```

### Checking Status
```bash
docker ps -a | grep tasks.md
```

### Viewing Logs (if issues)
```bash
docker logs tasks.md
```

### Complete Reset (if needed)
```bash
docker stop tasks.md
docker rm tasks.md
# Then repeat Step 2 above
```

---

## 📋 INTEGRATION WITH WIP.md

### **AI Workflow Pattern**

#### **When Starting Task Work:**
1. **Read task file** for complete context and approach
2. **Confirm plan** with user: "I see the task has this checklist approach - should I proceed?"
3. **Update WIP.md** with current session progress  
4. **Update task file** with discoveries and progress

#### **When Planning Large Tasks:**
1. **Write detailed checklist** in task file
2. **Ask user for confirmation**: "I've created this approach in the task file - does this look right?"
3. **Iterate on plan** in task file before starting work
4. **Track daily progress** in WIP.md

#### **Example AI Confirmation:**
> "I've reviewed the 'Research KeyDiscovery Setup Process' task and created a 5-step checklist focusing on config-overrides.js, Firebase, DNS, email auth, and automation opportunities. The full plan is in `Backlog/research-keydiscovery-setup.md`. Should I proceed with this approach, or would you like me to adjust the plan first?"

### **Task Flow Pattern**
1. **Create task** → Add to Backlog column with detailed checklist
2. **Start work** → Move to "In Progress" + update WIP.md current focus
3. **External blocker** → Move to "Waiting" + note in WIP.md blockers  
4. **Ready for review** → Move to "Review" 
5. **Complete** → Move to "Done" + archive details from WIP.md

### **WIP.md Integration Example**
```markdown
## 🔥 CURRENT FOCUS

### **This Week's Priority**
Document KeyDiscovery setup for automation planning

### **Active Work Session**
- **Task**: Research KeyDiscovery Setup Process (see Backlog/research-keydiscovery-setup.md)
- **Progress**: Completed config-overrides.js analysis, found multi-site pattern
- **Next**: Check Firebase hosting configuration  
- **Discovery**: Build system uses webpack entry points for site isolation
```

---

## 🚨 TROUBLESHOOTING

### Port 8080 Already in Use
```bash
# Find what's using port 8080
lsof -i :8080

# Kill the process (replace PID with actual process ID)
kill -9 [PID]

# Or use different port
docker run -d --name tasks.md -p 8081:8080 -v $(pwd)/project-tracker:/tasks/ [image-name]
```

### Docker Permission Issues (Linux)
```bash
sudo chown -R $USER:$USER project-tracker/
```

### Container Won't Start
```bash
# Check Docker is running
docker info

# Check for errors
docker logs tasks.md

# Try different image or restart Docker
```

### Board Not Updating
- Refresh browser page
- Check that files are being created in `project-tracker/` directory
- Verify Docker volume mount is working

---

## 🔄 FALLBACK: File-Based Management

**If Docker/Tasks.md cannot be set up:**
Use WIP.md task tracking exclusively:

```markdown
## 🔄 TASK STATUS

### **In Progress**
- [ ] [Task description] - [Owner] - [Status/Notes] - [Link to detailed task file if exists]

### **Waiting For**  
- [ ] [Task description] - [Blocked by what] - [Expected resolution]

### **Ready to Start**
- [ ] [Task description] - [Prerequisites met]
```

---

**Remember**: Tasks.md board enables rich task planning with detailed checklists and AI confirmation workflows, while WIP.md tracks session-specific progress. Both integrate with the information temperature system for optimal context management. 