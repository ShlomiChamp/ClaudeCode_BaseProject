# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a base project template designed for Claude Code sessions. It serves as a starting point for AI-first development workflows and provides organizational structure for Claude Code interactions.

## Repository Structure

```
ClaudeCode_BaseProject/
├── memory/           # Persistent context files for Claude Code sessions
├── prompts/          # Reusable prompt templates for common workflows
├── skills/           # Custom skill definitions (currently empty)
└── slash/            # Custom slash command definitions (currently empty)
```

### Key Directories

**memory/**
- Stores persistent context between Claude Code sessions
- Contains environment audits, project notes, and other reference documentation
- Example: `dev_environment.md` tracks installed development tools and versions
- Use this folder to save important context that future Claude instances should reference

**prompts/**
- Contains reusable prompt templates for common operations
- Example: `create_memory_file.md` provides templates for generating memory files
- Designed to be copied/adapted for specific use cases

**skills/** and **slash/**
- Reserved for Claude Code custom skills and slash commands
- Currently empty but ready for extensions

## Development Environment

This project is configured for a Windows development environment with:
- Python 3.12.6 (managed with pip and uv)
- Node.js 22.11.0 (managed with nvm4w)
- Docker 27.3.1
- PostgreSQL 17.2
- Git 2.47.1

See [memory/dev_environment.md](memory/dev_environment.md) for the complete environment audit.

## Working with This Repository

### Memory Management
When creating persistent documentation, save files to the `memory/` folder:
- Use clear, descriptive filenames (e.g., `dev_environment.md`, `project_context.md`)
- Format documents in Markdown with clear sections and tables
- Include dates and version information where relevant

### Prompt Templates
When creating reusable workflows:
- Save prompt templates to the `prompts/` folder
- Include example usage and clear instructions
- Keep templates modular and adaptable

## Project Purpose

This repository serves as a clean slate for Claude Code sessions, providing:
1. Organized structure for saving session context
2. Templates for common workflows
3. Documented development environment
4. Foundation for building AI-first applications with MCP integration
