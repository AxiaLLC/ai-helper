# Research Project Example - AI Helper Template

This example shows how to use the AI Helper Template for academic research projects, data analysis, or experimental work.

## Project Context

**Type**: Academic research with data analysis  
**Team Size**: 1-2 researchers + AI collaboration  
**AI Collaboration**: Heavy use for literature review, data analysis, and writing assistance  

## Setup Process

1. **Copy template files to your research directory**:
   ```bash
   cp -r ai-helper-template/* your-research-project/
   ```

2. **Customize PROJECT_PLAN.md**:
   - Replace `[PROJECT NAME]` with your research title
   - Define your research questions and hypotheses
   - Outline your methodology and expected deliverables
   - Set your timeline and milestones

3. **Initialize WIP.md**:
   - Set your current research phase
   - Create checklists for literature review, data collection, analysis
   - Track progress on writing and revisions

4. **Set up task management**:
   - Use file-based task management for research workflows
   - Create folders for different research phases

## Example Workflow

### Literature Review Phase

1. **Create research checklist in WIP.md**:
   ```markdown
   ### **Active Checklist** - Literature Review Phase
   - [ ] Search academic databases for relevant papers (Est: 2 hours)
   - [ ] Review and categorize 20 key papers (Est: 4 hours)
   - [ ] Identify research gaps and opportunities (Est: 1 hour)
   - [ ] Draft literature review section (Est: 3 hours)
   ```

2. **AI Collaboration**: Use AI to help summarize papers, identify themes, and suggest additional sources

3. **Progress Tracking**: Update checklist as papers are reviewed and insights are captured

### Data Analysis Phase

1. **Analysis checklist**:
   ```markdown
   ### **Active Checklist** - Data Analysis
   - [ ] Clean and preprocess dataset (Est: 2 hours)
   - [ ] Exploratory data analysis and visualization (Est: 3 hours)
   - [ ] Statistical analysis and hypothesis testing (Est: 4 hours)
   - [ ] Interpret results and identify key findings (Est: 2 hours)
   ```

2. **AI Assistance**: Use AI for code review, statistical interpretation, and visualization suggestions

## Technology Stack Example

```markdown
### **Technology Stack**
- **Data Analysis**: Python, Pandas, NumPy, Scikit-learn
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Statistical Analysis**: R, SPSS, or Python statsmodels
- **Writing**: LaTeX, Overleaf, or Markdown with Pandoc
- **Version Control**: Git for code and data versioning
```

## Research-Specific Patterns

### File Organization
```
your-research-project/
├── PROJECT_PLAN.md          # Research overview and methodology
├── WIP.md                   # Current progress and next steps
├── CHANGE_LOG.md            # Research decisions and pivots
├── data/                    # Raw and processed datasets
├── analysis/                # Analysis scripts and notebooks
├── literature/              # Papers and literature notes
├── writing/                 # Drafts and final papers
├── figures/                 # Generated plots and visualizations
└── ARCHIVE/                 # Completed analysis and old drafts
    ├── completed-analysis/
    ├── literature-reviews/
    └── failed-experiments/
```

### Git Workflow for Research
- **Commit frequently**: Save progress on analysis and writing
- **Tag milestones**: Mark important versions (draft submissions, revisions)
- **Branch for experiments**: Try different analysis approaches safely

### AI Collaboration Patterns

#### Literature Review
- **Paper Summarization**: AI helps extract key points from papers
- **Gap Identification**: AI suggests unexplored research areas
- **Citation Management**: AI helps format references and find related work

#### Data Analysis
- **Code Review**: AI checks analysis scripts for errors
- **Statistical Interpretation**: AI helps explain statistical results
- **Visualization**: AI suggests effective ways to present data

#### Writing
- **Draft Review**: AI provides feedback on clarity and structure
- **Argument Strengthening**: AI helps identify weak points in reasoning
- **Language Polishing**: AI improves academic writing style

## Benefits for Research

- **Accelerated Literature Review**: AI helps process and synthesize large amounts of literature
- **Robust Analysis**: Systematic approach reduces errors and improves reproducibility
- **Better Documentation**: All decisions and changes tracked for transparency
- **Efficient Writing**: AI assistance speeds up drafting and revision process
- **Knowledge Retention**: Important insights and failed experiments preserved

## Common Research Checklists

### **Experimental Design**
- [ ] Define research questions and hypotheses
- [ ] Design experimental methodology
- [ ] Identify required data and collection methods
- [ ] Plan statistical analysis approach

### **Data Collection**
- [ ] Prepare data collection instruments
- [ ] Collect pilot data and validate approach
- [ ] Execute full data collection
- [ ] Verify data quality and completeness

### **Analysis & Writing**
- [ ] Conduct exploratory data analysis
- [ ] Perform statistical tests and modeling
- [ ] Create visualizations and tables
- [ ] Write results and discussion sections

### **Publication**
- [ ] Prepare manuscript for target journal
- [ ] Internal review and revision
- [ ] Submit to journal and respond to reviews
- [ ] Prepare presentation materials

## Next Steps

1. Customize the template files for your specific research project
2. Set up your research environment and tools
3. Create your first research phase checklist in WIP.md
4. Start collaborating with AI using research-focused patterns

See the main README.md for complete setup instructions and workflow details. 