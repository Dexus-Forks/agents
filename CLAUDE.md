# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Claude Code Subagents Collection - a comprehensive set of 32 specialized AI subagents designed to enhance development workflows with domain-specific expertise. Each subagent is a markdown file containing metadata and system prompts that define specialized behaviors for specific development tasks.

## Project Structure

The repository consists of individual markdown files, each representing a specialized subagent:
- Each `.md` file follows a standardized format with YAML frontmatter
- Files are named using lowercase, hyphen-separated names (e.g., `backend-architect.md`)
- No build system or package management is required - these are configuration files

## Subagent File Format

Each subagent file follows this structure:
```markdown
---
name: subagent-name
description: When this subagent should be invoked
tools: tool1, tool2  # Optional - defaults to all tools
---

System prompt defining the subagent's role and capabilities
```

## Key Subagent Categories

1. **Development & Architecture**: backend-architect, frontend-developer, mobile-developer, graphql-architect
2. **Language Specialists**: python-pro, golang-pro, rust-pro, typescript-expert
3. **Infrastructure & Operations**: devops-troubleshooter, deployment-engineer, cloud-architect
4. **Quality & Security**: code-reviewer, security-auditor, test-automator, debugger
5. **Data & AI**: data-scientist, data-engineer, ai-engineer, ml-engineer
6. **Specialized Domains**: api-documenter, payment-integration, quant-analyst, game-developer

## Development Guidelines

When modifying or adding subagents:
1. Maintain the consistent YAML frontmatter format
2. Write clear, actionable descriptions for when the subagent should be used
3. Focus system prompts on specific expertise and concrete outputs
4. Keep instructions practical and implementation-focused
5. Ensure subagent names are descriptive and follow the naming convention

## Testing Subagents

Since these are configuration files, there are no traditional tests. To validate a subagent:
1. Check the YAML frontmatter is properly formatted
2. Ensure the description clearly indicates when to use the subagent
3. Verify the system prompt provides clear, actionable guidance
4. Test by explicitly invoking the subagent in Claude Code

## Common Tasks

### Adding a New Subagent
1. Create a new `.md` file with a descriptive lowercase, hyphenated name
2. Add the required YAML frontmatter (name, description, optional tools)
3. Write a focused system prompt that defines the subagent's expertise
4. Include specific output formats and approaches in the prompt

### Updating an Existing Subagent
1. Modify the relevant `.md` file
2. Ensure changes maintain compatibility with the expected format
3. Test the updated behavior in Claude Code

### Removing a Subagent
Simply delete the corresponding `.md` file from the repository

## Integration with Claude Code

These subagents are automatically available when placed in the `~/.claude/agents/` directory. Claude Code will:
- Automatically delegate to appropriate subagents based on task context
- Allow explicit invocation by mentioning the subagent name
- Coordinate multiple subagents for complex workflows

## Repository Maintenance

- The repository is focused solely on subagent definitions
- No external dependencies or build processes
- Changes are immediately effective when files are updated
- Git is used for version control and collaboration