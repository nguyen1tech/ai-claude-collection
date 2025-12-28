# Skills Collection

This directory contains custom skills for AI agents and assistants. Skills are reusable capabilities that can be invoked to perform specific tasks following standardized patterns.

## Directory Structure

```
skills/
├── examples/           # Example skill implementations
│   └── standardized-report-generator/
│       ├── SKILL.md   # Skill definition and instructions
│       └── README.MD  # Skill-specific documentation
└── README.md          # This file
```

## What are Skills?

Skills are structured templates that define:
- **Name**: A clear identifier for the skill
- **Description**: When and how to use the skill
- **Instructions**: Step-by-step guidance for execution
- **Examples**: Sample inputs and expected outputs

## Installation

To install and use these skills:

1. **Clone or download this repository**:
   ```bash
   git clone <repository-url>
   cd ai-claude-collection/skills
   ```

2. **For Claude Code CLI**:
   - Copy the skills directory to your Claude Code skills path
   - Or configure Claude Code to load skills from this directory
   - Skills will be automatically discovered and available for use

3. **To install a specific skill**:

   **System-wide installation**:
   ```bash
   # Copy skill to global Claude Code skills directory
   cp -r examples/standardized-report-generator ~/.config/claude-code/skills/
   ```

   **Project-wide installation**:
   ```bash
   # Copy skill to project's skills directory
   mkdir -p ./skills
   cp -r examples/standardized-report-generator ./skills/
   ```

4. **For custom AI implementations**:
   - Point your skill loader to this directory
   - Ensure your system can parse the SKILL.md frontmatter and instructions

5. **Verify installation**:
   - Check that skills are recognized by your AI assistant
   - Test with the example skill to confirm proper functionality

## Example Skills

### [Standardized Report Generator](examples/standardized-report-generator/SKILL.md)
Create structured, branded reports with Executive Summary, Findings, Recommendations, and Appendix sections. Use when generating formal business reports.

## Adding New Skills

To add a new skill:

1. Create a new directory under `examples/` or at the root level
2. Add a `SKILL.md` file with the following structure:
   ```markdown
   ---
   name: "Your Skill Name"
   description: "Brief description of when to use this skill"
   ---

   # Skill Name

   ## Instructions
   - Step-by-step instructions

   ## Example
   - Sample usage
   ```
3. Optionally add a `README.md` for additional documentation

## Usage

Skills can be invoked by AI assistants when the task matches the skill's description. The assistant will follow the instructions defined in the SKILL.md file to complete the task consistently and effectively.
