# PRD Directory

This directory contains Product Requirements Documents (PRDs) for specific features of the project.

## Structure

```
prd/
├── README.md                   # This file
└── features/                   # Feature-specific PRDs
    ├── feature1/               # Example feature directory
    │   └── prd.md              # Feature PRD file
    └── feature2/               # Another feature directory
        └── prd.md              # Feature PRD file
```

## Purpose

The PRD directory is used to store detailed requirements for individual features within the project. Note that the overall product requirements are maintained in:

- `../projectBrief.md` - Core product requirements and goals
- `../productContext.md` - User experience and product context

Feature PRDs should reference and align with these core documents while providing detailed specifications for individual features.

## How to Create a New Feature PRD

1. Create a new subdirectory under `features/` with the name of your feature
2. Create a `prd.md` file in that directory using the [Feature PRD Template](.cursor/rules/prd-creator.mdc)
3. Update relevant memory bank files to reference the new PRD
4. Maintain consistency with system patterns and technical decisions

## Important Notes

- Reference core PRD documents for context and alignment
- Update memory bank files to reflect new PRDs
- Follow the PRD creation process defined in .cursor/rules/prd-creator.mdc
