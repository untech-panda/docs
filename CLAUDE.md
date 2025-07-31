# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site with MDX content files and JSON configuration. The site covers guides, API references, and AI development tools.

## Essential Commands

### Development
- `mint dev` - Start local development server at http://localhost:3000
- `mint dev --port [PORT]` - Start server on custom port
- `mint update` - Update Mintlify CLI to latest version
- `mint broken-links` - Validate all documentation links

### Prerequisites
- Node.js version 19 or higher
- Mintlify CLI: `npm i -g mint`

## Content Standards

### File Requirements
- All content files use `.mdx` extension
- Required frontmatter on every MDX file:
  ```yaml
  ---
  title: 'Clear, descriptive page title'
  description: 'Concise summary for SEO/navigation'
  ---
  ```

### Writing Guidelines
- Use second-person voice ("you")
- Include prerequisites at start of procedural content
- Test all code examples before publishing
- Use language tags on all code blocks
- Include alt text on all images
- Use relative paths for internal links (never absolute URLs)

### Content Strategy
- Document just enough for user success
- Search existing content before adding new information
- Check existing patterns for consistency
- Start with smallest reasonable changes
- Make content evergreen when possible

## Architecture

### Configuration
- `docs.json` - Navigation structure, theming, site settings
- Navigation uses tabs → groups → pages hierarchy

### Content Organization
- `api-reference/` - API documentation and endpoint examples  
- `essentials/` - Core Mintlify features and components
- `ai-tools/` - AI development tool documentation
- `snippets/` - Reusable content snippets

### Components
Uses Mintlify-specific components: `<Info>`, `<Steps>`, `<Frame>`, `<AccordionGroup>`, `<Accordion>`

## Git Workflow
- NEVER use `--no-verify` when committing
- Ask about uncommitted changes before starting work
- Create new branch when no clear branch exists
- Commit frequently during development
- NEVER skip or disable pre-commit hooks