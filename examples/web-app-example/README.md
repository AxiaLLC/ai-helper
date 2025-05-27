# Web App Example - AI Helper Template

This example shows how to use the AI Helper Template for a typical web application project.

## Project Context

**Type**: React/Node.js web application  
**Team Size**: 1-3 developers  
**AI Collaboration**: Heavy use of AI for development acceleration  

## Setup Process

1. **Copy template files to your project root**:
   ```bash
   cp -r ai-helper-template/* your-web-app/
   ```

2. **Customize PROJECT_PLAN.md**:
   - Replace `[PROJECT NAME]` with your app name
   - Fill in your technology stack (React, Node.js, database, etc.)
   - Define your phases and deliverables
   - Set your success criteria

3. **Initialize WIP.md**:
   - Set your current focus and next session goal
   - Create your first checklist of 3-5 tasks
   - Get user confirmation before starting work

4. **Set up task management**:
   - Follow TASKS_MD_SETUP.md to install Tasks.md board
   - Or use file-based task management in project-tracker directories

## Example Workflow

### Starting a New Feature

1. **Create task checklist in WIP.md**:
   ```markdown
   ### **Active Checklist** - Confirmed by user on [Date]
   - [ ] Design user authentication flow (Est: 45 min)
   - [ ] Set up Firebase Auth integration (Est: 30 min)
   - [ ] Create login/signup components (Est: 60 min)
   - [ ] Test authentication end-to-end (Est: 30 min)
   ```

2. **Get user confirmation**: "Here are my next steps for implementing authentication. Shall I proceed?"

3. **Execute checklist**: Work through each item, updating status in real-time

4. **Archive completed work**: Move detailed implementation notes to ARCHIVE/

### AI Collaboration Pattern

- **Context Acquisition**: AI reads hot files (README, PROJECT_PLAN, WIP, CHANGE_LOG) in <5 minutes
- **Task Planning**: AI proposes 3-5 step checklists for user confirmation
- **Progress Tracking**: Real-time updates in WIP.md Current Checklist section
- **Decision Logging**: Major choices documented in CHANGE_LOG.md

## Technology Stack Example

```markdown
### **Technology Stack**
- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Backend**: Node.js, Express, TypeScript
- **Database**: PostgreSQL with Prisma ORM
- **Infrastructure**: Vercel (frontend), Railway (backend)
- **External Integrations**: Stripe, SendGrid, Auth0
```

## Common Patterns

### Git Workflow
- **Task-driven commits**: Reference specific checklist items
- **Commit format**: `feat(auth): implement login component - completes checklist item 3`
- **Regular commits**: After each checklist item completion

### File Organization
```
your-web-app/
├── PROJECT_PLAN.md          # Project overview and roadmap
├── WIP.md                   # Current work and checklists
├── CHANGE_LOG.md            # Recent decisions and changes
├── TASKS_MD_SETUP.md        # Task management setup
├── .cursorrules             # AI collaboration rules
├── UNIVERSAL_AI_INSTRUCTIONS.md  # AI workflow protocols
├── src/                     # Your application code
├── docs/                    # Additional documentation
└── ARCHIVE/                 # Completed work details
    ├── completed-features/
    ├── technical-research/
    └── failed-experiments/
```

## Benefits for Web Apps

- **Rapid Feature Development**: AI can quickly understand context and propose implementation steps
- **Consistent Architecture**: Template enforces good documentation and decision tracking
- **Reduced Context Switching**: All project state visible in hot files
- **Better Collaboration**: Clear handoffs between human and AI work sessions
- **Knowledge Retention**: Important decisions and learnings preserved in CHANGE_LOG

## Next Steps

1. Customize the template files for your specific project
2. Set up your development environment
3. Create your first feature checklist in WIP.md
4. Start collaborating with AI using the established patterns

See the main README.md for complete setup instructions and workflow details. 