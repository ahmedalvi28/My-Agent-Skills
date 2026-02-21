# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a collection of specialized AI skills organized in the `skills/` directory. Each skill is designed for a specific purpose and follows a standardized structure with a SKILL.md file that defines its capabilities, usage, and behavior.

## Directory Structure

```
My Agent Skills/
└── skills/

    ├── LinkedIn-DailyPost/
    │   └── SKILL.md
    ├── UrduPoetry/
    │   └── SKILL.md
    ├── Sales_Expense_Anomaly_Detector/
    │   └── SKILL.md
    └── Smart_Inventory_Manager/
        └── SKILL.md
```

## Architecture

Each skill follows a consistent pattern:

- **SKILL.md**: Contains the skill definition with:
  - YAML frontmatter (name, description)
  - When to use the skill
  - Step-by-step procedure
  - Input/output parameters
  - Default behaviors
  - Example implementations

## Key Skills

### LinkedIn-DailyPost
- Generates simple, honest, beginner-style motivational LinkedIn posts in a general tone
- Focuses on learning, consistency, and early professional growth without sounding like expert advice
- Limits posts to 2-4 short sentences with 2-4 relevant hashtags
- Uses neutral tone avoiding personal pronouns like "I", "my", or "we"

### UrduPoetry
- Creates original, emotionally rich Urdu poetry in the styles of Gulzar or Jaun Elia
- Outputs concise, elegant poetry in Unicode-safe format suitable for Twitter (≤280 characters)
- Features randomized selection of style (Gulzar/Jaun Elia), theme, tone, and length for variety
- Operates without user input, generating fresh poems with each invocation
- Outputs both clean Urdu script and Roman Urdu for easy sharing and accessibility
- Includes specific style guidelines distinguishing Gulzar's subtle metaphors and visual imagery from Jaun Elia's introspective and melancholic tone
- Applies quality constraints to avoid clichés, overused phrases, and imitation of real verses
- Focuses on creating well-rhymed couplets (shers) with proper rhythm and flow

### Sales & Expense Anomaly Detector
- Analyzes sales, expenses, or financial datasets to detect unusual patterns, spikes, drops, or inconsistencies
- Identifies potential errors, fraud, or abnormal trends with clear explanations and actionable insights
- Performs data validation, preprocessing, and establishes baseline patterns for comparison
- Classifies anomalies by severity (Critical or Warning) with contextual reasoning
- Provides recommended actions and summarizes overall trend health

### Smart Inventory Manager
- Continuously monitors inventory and updates stock automatically after sales, purchases, or returns
- Recommends optimal reorder quantities based on sales velocity, lead time, and safety buffer
- Provides proactive alerts for low stock, overstocking, or delayed reordering risks
- Handles various inventory events (sales, purchases, returns) with appropriate stock adjustments
- Offers structured output with clear separation of stock updates, alerts, and reorder suggestions

## Common Development Tasks

### Adding a New Skill
1. Create a new folder in the `skills/` directory with a descriptive name
2. Inside the folder, create a `SKILL.md` file
3. Follow the standard format with YAML frontmatter, usage instructions, and procedures
4. Include examples and input/output specifications

### Modifying Existing Skills
- Update the SKILL.md file in the respective skill directory
- Ensure backward compatibility when changing input/output formats
- Test the skill behavior after modifications

## Commands

No specific build or test commands are required for this repository as it consists primarily of markdown files defining AI skills. The skills are interpreted by AI systems directly from the markdown definitions.

## File Extensions and Types

- `.md`: Markdown files containing skill definitions with YAML frontmatter
- Folders: Represent individual skill modules

## Skills Directory Organization

Each skill directory contains:
- `SKILL.md`: The primary skill definition file with all necessary configuration
- Additional supporting files as needed by the specific skill

The skills are organized by functionality:
- **Content Creation**: LinkedIn-DailyPost, UrduPoetry
- **Data Analysis**: Sales_Expense_Anomaly_Detector
- **Business Operations**: Smart_Inventory_Manager

## Working with the Repository

When contributing to or modifying this repository:

### For Developers
- Each skill is defined in its own directory with a SKILL.md file
- Follow the standardized format for consistency
- Test skills thoroughly before committing changes
- Maintain backward compatibility when possible

### For AI Systems
- Parse SKILL.md files to understand skill capabilities
- Respect the input/output specifications defined in each skill
- Apply the behavioral guidelines specified in each skill definition

## Repository Maintenance Guidelines

- All skills use markdown files with YAML frontmatter for configuration
- Skills are interpreted directly from markdown definitions
- When modifying existing skills, ensure backward compatibility
- Follow consistent formatting across all SKILL.md files
- Document any breaking changes clearly