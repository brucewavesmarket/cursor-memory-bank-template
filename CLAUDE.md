# Cursor Rules

## Memory Bank Management (REQUIRED)

### Initial Validation

- MUST check for existence of .cursor/rules/cursor-memory-bank.mdc at the start of EVERY new conversation thread
- MUST verify all required memory bank files exist:
  - memory-bank/projectbrief.md
  - memory-bank/productContext.md
  - memory-bank/systemPatterns.md
  - memory-bank/techContext.md
  - memory-bank/activeContext.md
  - memory-bank/progress.md
- MUST initialize missing memory bank files before proceeding with any work
- MUST read ALL memory bank files at the start of EVERY task

### Update Protocol

- MUST update relevant memory bank files after EACH significant change:
  - memory-bank/activeContext.md: Update current focus and recent changes
  - memory-bank/progress.md: Update status and achievements
  - memory-bank/systemPatterns.md: Document new patterns or architectural changes
  - memory-bank/techContext.md: Record technical decisions or stack changes
- MUST validate memory bank consistency after updates
- MUST ensure all updates maintain documentation quality and clarity

### PRD Integration

- MUST recognize projectBrief.md and productContext.md as the core PRD documents
- WHEN creating feature-specific PRDs:
  - Create in memory-bank/prd/features/{feature-name}/prd.md
  - Reference core PRD documents for context and alignment
  - Update memory bank files to reflect the new PRD with specific changes to:
    - activeContext.md (Current Focus, Recent Changes, Next Steps, Active Decisions)
    - progress.md (Recent Achievements, Next Priorities, Current Status, Milestones)
    - Conditionally update systemPatterns.md and techContext.md as needed
  - Maintain consistency with system patterns and technical decisions
- MUST follow PRD creation process defined in .cursor/rules/prd-creator.mdc
- MUST ensure proper cross-referencing between PRDs and memory bank files
- MUST follow the PRD creation workflow visualized in .cursor/rules/prd-creator.mdc diagrams

## Coding Pattern Requirements

### Code Quality

- Always prefer simple solutions over complex ones
- Avoid code duplication by checking existing codebase for similar functionality
- Keep codebase clean and well-organized
- Maintain file size under 200-300 lines
  - Complete and verify feature work BEFORE refactoring
  - Only refactor after changes are proven working
  - Document refactoring decisions in memory bank

### Environment Handling

- Write code considering all environments: dev, test, prod
- Never use mock data in dev or prod environments
- Only use mocking for test environments
- Never modify .env files without explicit user confirmation

### Change Management

- Only implement explicitly requested changes
- Verify understanding before making related changes
- Exhaust existing implementation options before introducing new patterns
- Remove old implementations when introducing new patterns
- Avoid one-off scripts in source files

## Tool Usage Guidelines

### Claude Think Tool Usage

#### Use For:

1. Complex Multi-Step Problems
   - Breaking down interdependent steps
   - Planning implementation sequences
2. Reasoning Through Constraints
   - Analyzing multiple requirements
   - Evaluating trade-offs
3. Policy Adherence
   - Ensuring guideline compliance
   - Validating against standards
4. Planning Complex Operations
   - Organizing tool call sequences
   - Structuring implementation steps
5. Debugging/Troubleshooting
   - Analyzing error causes
   - Planning solution approaches
6. Multi-Variable Decisions
   - Evaluating multiple factors
   - Assessing trade-offs

#### Do Not Use For:

- Simple, straightforward questions
- Tasks without multi-step reasoning
- Basic information retrieval
- Simple creative writing

### Memory Bank Tool Integration

- Use tools systematically to maintain memory bank
- Document tool usage patterns in techContext.md
- Record tool-related decisions in activeContext.md
- Track tool effectiveness in progress.md
- Follow filesystem tool usage patterns defined in prd-creator.mdc for PRD-related operations

## Documentation Standards

### Memory Bank Updates

- Keep all documentation current and accurate
- Use clear, consistent formatting
- Include rationale for significant changes
- Maintain traceability of decisions
- Update related files consistently
- Ensure feature PRDs reference core PRD documents appropriately
- Cross-reference related features and capabilities

### Quality Requirements

- Comprehensive coverage of changes
- Clear explanation of decisions
- Consistent terminology
- Regular validation of accuracy
- Proper cross-referencing between files
- Alignment with established patterns and principles
- Integration with existing documentation hierarchy

## PRD Standards

### PRD Structure

- Follow Feature PRD template in prd-creator.mdc
- Maintain proper sectioning and organization
- Include all required sections for completeness
- Ensure clear integration with memory bank documents

### PRD Creation Workflow

1. Read and understand all memory bank files before starting
2. Follow the structured questioning approach from prd-creator.mdc
3. Create feature PRD in the correct location
4. Update memory bank files with standardized sections as specified in prd-creator.mdc
5. Verify cross-references between PRD and memory bank files
6. Review documentation consistency across all files
7. Validate PRD alignment with system patterns and technical decisions
