# Code Quality

This directory contains configurations and tools to ensure code quality in your projects.

## Tools and Configurations

### Biome
- **File**: `biome.json`
- **Description**: Biome is a fast formatter for JavaScript, TypeScript, JSX, TSX, JSON, CSS and GraphQL that scores 97% compatibility with Prettier, saving CI and developer time. It's perfect to use in your project like React, Next.js and Solid.js
---
- **Document**: https://biomejs.dev/guides/getting-started/
- Install command: `bun add --dev --exact @biomejs/biome`
- init command: `bunx biome init`
- 

### CSpell
- **File**: `cspell.yaml`
- **Description**: Configuration for CSpell, a spell checker for code.
- **Usage**: The configuration includes dictionaries for TypeScript, Node, and fonts. It ignores the `node_modules` and `package.json` files.

### Lefthook
- **File**: `lefthook.yml`
- **Description**: Configuration for Lefthook, a tool for managing Git hooks.
- **Usage**: The configuration sets up a pre-commit hook to check JavaScript and TypeScript files using Biome. It stages fixed files automatically.

## Usage Instructions

1. **Biome**: Run `biome check` to check for code quality issues and `biome format` to format the code.
2. **CSpell**: Run `cspell` to check for spelling errors in the code.
3. **Lefthook**: The pre-commit hook will automatically run when you commit changes. Ensure you have Lefthook installed and configured in your project.
