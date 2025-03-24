# Cursor Memory Bank Template

This repository serves as a template for projects using a custom Memory Bank system for AI-assisted development that enables much more consistent, and context aware generation from AI-enabled IDEs like Cursor, or agentic code editors like Claude Code. It provides a standardized structure for project documentation and AI assistance.

## Structure

- `.cursor/rules/` - Contains rules for Cursor AI
- `memory-bank/` - Core memory bank files for project documentation
- `.cursorrules` - Main configuration file for Cursor AI
- `CLAUDE.md` - Rules for Claude AI assistant

## How to Use This Template

### Method 1: GitHub UI (Easiest)

1. Click the green "Use this template" button at the top of this repository
2. Select "Create a new repository"
3. Enter a name for your new project
4. Choose public or private visibility
5. Click "Create repository from template"
6. Clone your new repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/your-new-project.git
   cd your-new-project
   ```

### Method 2: GitHub CLI (Suggested)

```bash
# Install GitHub CLI if needed (https://cli.github.com/)
# Then create a new repo from this template
gh repo create your-new-project --template hbruceweaver/cursor-memory-bank-template --private  # or --public

# Clone the newly created repository
git clone https://github.com/YOUR-USERNAME/your-new-project.git
cd your-new-project
```

### Method 3: Manual Approach

```bash
# Clone this template repository
git clone https://github.com/hbruceweaver/cursor-memory-bank-template.git your-new-project

# Go into the new project directory
cd your-new-project

# Remove connection to the template repository
rm -rf .git

# Initialize a new git repository
git init

# Add all files
git add .

# Commit the files
git commit -m "Initial commit from template"

# Create a new repository on GitHub and add as remote
git remote add origin https://github.com/YOUR-USERNAME/your-new-project.git

# Push to GitHub
git push -u origin main
```

## Working with Cursor

1. Open your new project in Cursor
2. Cursor will automatically detect and use the memory bank system
3. Begin developing with AI assistance

## Memory Bank Files

- `projectBrief.md` - Project overview, requirements, goals
- `productContext.md` - Problem statement, solution, UX goals
- `systemPatterns.md` - Architecture, components, patterns
- `techContext.md` - Technology stack, dependencies, constraints
- `activeContext.md` - Current focus, decisions, next steps
- `progress.md` - Status tracking, achievements, priorities

## PRD Structure

Feature PRDs are organized under `memory-bank/prd/features/` with each feature having its own directory:

```
memory-bank/
└── prd/
    └── features/
        ├── feature1/
        │   └── prd.md
        └── feature2/
            └── prd.md
```

## First Steps After Creating Your Project

1. Update `memory-bank/projectBrief.md` with your project's specific details
2. Fill in `memory-bank/productContext.md` with your product's context
3. Begin working on your project with Cursor AI assistance
4. The AI will automatically maintain the memory bank as you work

## Troubleshooting

If Cursor AI doesn't seem to be using the memory bank:

1. Ensure all files are in the correct locations
2. Try restarting Cursor
3. Enter "update memory bank" in a message to the AI
