# My Agent Skills

This repository contains a collection of specialized AI skills designed to automate various tasks that traditionally required human intervention. Each skill serves as an intelligent replacement for manual processes, offering consistent, reliable, and efficient automation.

## Repository Overview

The repository is organized around the concept of specialized AI skills, each designed for a specific purpose. Each skill follows a standardized structure with a SKILL.md file that defines its capabilities, usage, and behavior. The skills are contained within the `skills/` directory and can be easily extended or modified as needed.

## Skills Architecture

Each skill follows a consistent pattern:
- **SKILL.md**: Contains the skill definition with YAML frontmatter, usage instructions, and procedures
- Standardized input/output specifications
- Clear operational guidelines and examples
- Consistent formatting for easy maintenance and understanding

## Available Skills


## Skills Overview

### LinkedIn-DailyPost
**Replaces:** Manual creation of daily LinkedIn posts for beginners

**Traditional Process:** Individuals manually crafting motivational posts, often struggling with writer's block, inconsistent posting schedules, or inappropriate tone for their experience level.

**Automation Provided:** Automatically generates simple, honest, beginner-focused motivational LinkedIn posts with appropriate hashtags. Maintains consistency in posting while ensuring content remains authentic and relatable to early-career professionals. Uses neutral tone avoiding personal pronouns and focuses on learning, consistency, and early professional growth without sounding like expert advice.

---

### UrduPoetry
**Replaces:** Manual composition of Urdu poetry for social media or personal expression

**Traditional Process:** Urdu poetry enthusiasts spending time crafting verses in the style of classical poets like Gulzar or Jaun Elia, requiring deep knowledge of literary techniques and cultural nuances.

**Automation Provided:** Instantly creates original Urdu poetry in the distinctive styles of renowned poets, maintaining the rich metaphorical language and emotional depth characteristic of traditional Urdu poetry, optimized for social media platforms. Features randomized selection of style (Gulzar or Jaun Elia), theme, tone, and length for variety, operates without user input, and outputs both clean Urdu script and Roman Urdu for easy sharing and accessibility. Distinguishes between Gulzar's subtle metaphors and visual imagery versus Jaun Elia's introspective and melancholic tone, while applying quality constraints to avoid clichés, overused phrases, and imitation of real verses. Focuses on creating well-rhymed couplets (shers) with proper rhythm and flow, suitable for Twitter (≤280 characters).

---

### Sales & Expense Anomaly Detector
**Replaces:** Manual monitoring and analysis of financial data for irregularities

**Traditional Process:** Financial analysts manually reviewing sales and expense reports to identify unusual patterns, potential errors, or fraudulent activities - a time-intensive process prone to human oversight.

**Automation Provided:** Analyzes sales, expenses, or financial datasets to detect unusual patterns, spikes, drops, or inconsistencies with clear explanations and actionable insights. Performs data validation, preprocessing, and establishes baseline patterns for comparison. Classifies anomalies by severity (Critical or Warning) and provides recommended actions, significantly reducing the time and effort required for financial oversight.

---

### Smart Inventory Manager
**Replaces:** Manual inventory tracking and reorder management

**Traditional Process:** Inventory managers manually updating stock levels after transactions, calculating reorder quantities, and monitoring low-stock items - a process susceptible to human error and oversight.

**Automation Provided:** Continuously monitors inventory and updates stock automatically after sales, purchases, or returns, recommends optimal reorder quantities based on sales velocity, lead time, and safety buffer, and provides proactive alerts for low stock, overstocking, or delayed reordering risks. Handles various inventory events with appropriate stock adjustments and offers structured output with clear separation of stock updates, alerts, and reorder suggestions.

## Adding New Skills

To add a new skill to the repository:

1. Create a new folder in the `skills/` directory with a descriptive name
2. Inside the folder, create a `SKILL.md` file following the standard format:
   - YAML frontmatter with name and description
   - Clear usage instructions
   - Step-by-step procedures
   - Input/output specifications
   - Examples and default behaviors
3. Test the skill behavior to ensure it functions as expected
4. Update the documentation as needed

## Repository Maintenance

- All skills are defined in markdown files with YAML frontmatter
- The skills are interpreted by AI systems directly from the markdown definitions
- No specific build or test commands are required for this repository
- Ensure backward compatibility when modifying existing skills
- Maintain consistent formatting across all SKILL.md files