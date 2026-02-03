# Nature Figure Prompts

**English | [中文](README_zh.md)**

A Claude Code skill for creating publication-quality scientific figure prompts following Nature/Cell journal standards.

## Overview

This skill helps researchers generate detailed prompts for AI image generation tools (like Midjourney, DALL-E, or Gemini) to create scientific figures suitable for high-impact journal publications.

## Features

- **Paper Analysis Framework**: Systematic extraction of key research elements
- **Figure Planning**: Decide figure types based on paper content
- **Prompt Templates**: Pre-configured templates for common figure types:
  - Graphical Abstracts
  - Experimental Design Diagrams
  - Metabolic Pathway Diagrams
- **Color Standards**: Colorblind-friendly palettes with specific HEX values
- **Quality Checklist**: Ensure figures meet publication standards

## Dependencies

This skill **generates prompts only**. To create actual images from these prompts, you need:

- **[scientific-schematics](https://github.com/K-Dense-AI/claude-scientific-skills/tree/main/scientific-skills/scientific-schematics)** - AI-powered diagram generation using Nano Banana Pro with Gemini 3 Pro quality review. Features smart iterative refinement with document-type quality thresholds (journal: 8.5/10, poster: 7.0/10, etc.)

> **Note:** Requires [OpenRouter API key](https://openrouter.ai/keys) for AI image generation.

Install the dependency from [claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills):

```bash
# Clone the scientific-skills repository
git clone https://github.com/K-Dense-AI/claude-scientific-skills.git

# Copy scientific-schematics to your skills directory
cp -r claude-scientific-skills/scientific-skills/scientific-schematics .claude/skills/
```

## Installation

Copy the skill to your Claude Code skills directory:

```bash
# Create skills directory if it doesn't exist
mkdir -p .claude/skills

# Copy the skill
cp -r nature-figure-prompts .claude/skills/
```

## Usage

In Claude Code, use the skill with:

```
/nature-figure-prompts <path-to-paper>
```

Or provide a paper and ask:
```
Help me create figures for this paper: [paper content or path]
```

## Directory Structure

```
nature-figure-prompts/
├── SKILL.md                    # Main skill definition
└── references/
    ├── paper-analysis.md       # Paper analysis framework
    ├── layouts.md              # Layout templates (4 types)
    ├── colors.md               # Color standards & HEX values
    ├── vocabulary.md           # English terminology for figures
    └── troubleshooting.md      # Common fixes & iteration tips
```

## Visual Style Guidelines

All generated prompts follow these standards:
- Nature/Cell journal quality
- Volumetric 3D elements with soft shadows
- Clean off-white background (#FAFAFA)
- Professional typography (gene names in italic)
- Colorblind-friendly palette (Okabe-Ito)

## Color Conventions

- **Upregulation**: RED (#E53935) with ↑ arrow
- **Downregulation**: GREEN (#43A047) with ↓ arrow
- **Glucose metabolism**: Green (#4CAF50)
- **Lipid metabolism**: Orange (#FF9800)
- **Protein metabolism**: Blue (#2196F3)
- **Immune response**: Red (#F44336)

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

MIT License

## Acknowledgments

- Inspired by Nature/Cell publication guidelines
- Color palettes based on Okabe-Ito colorblind-safe palette
