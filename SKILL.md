---
name: nature-figure-prompts
description: Create publication-quality scientific figures for Nature/Cell/Science journals. Use this skill when (1) analyzing a paper to plan figures, (2) suggesting figure types and content, or (3) generating AI image prompts for graphical abstracts, pathway diagrams, experimental designs. Includes paper analysis framework, figure planning templates, prompt templates, and quality checklists.
---

# Nature Style Scientific Figure Prompts

Create publication-quality scientific figures through a structured workflow: Paper Analysis → Figure Planning → Prompt Generation → Iteration.

## Workflow Overview

```
Step 1: Paper Analysis     → Understand structure, extract key findings
Step 2: Figure Planning    → Decide figure types and content
Step 3: Prompt Generation  → Assemble prompts from templates
Step 4: Quality Check      → Validate and iterate
```

## Step 1: Paper Analysis

Before creating any figures, analyze the paper. See `references/paper-analysis.md` for full framework.

**Extract core information:**
```
研究对象：[species/material]
研究因素：[independent variables]
处理组数：[N groups]
检测层次：整体层 | 组织层 | 分子层
主要发现：[1-3 key conclusions]
最优条件：[which treatment is optimal]
```

**Identify paper type** to determine figure needs:
- 因子试验 → 因子矩阵图
- 剂量效应 → 剂量响应曲线
- 机制研究 → 分子通路图
- 比较研究 → 并列比较图

## Step 2: Figure Planning

**Essential figures (almost always needed):**
- [ ] Fig. 1: Experimental design schematic
- [ ] Graphical Abstract

**Conditional figures (based on data):**
- [ ] Metabolic pathway diagram (if gene expression data)
- [ ] Tissue/organ outcome panel (if histology/enzyme data)
- [ ] Mechanism summary (if regulatory mechanism identified)

**Planning template:**
```
Fig. 1: 实验设计图
- 类型：[流程式/因子矩阵]
- 包含：[动物、处理组、时间线、采样]

Graphical Abstract:
- 核心信息：[主要发现]
- 视觉焦点：[物种插图]
- 关键数据：[最优条件]
```

## Step 3: Prompt Generation

## Core Visual Style

All prompts must include:

```
VISUAL STYLE:
- Nature/Cell journal quality, volumetric 3D elements
- Soft shadows, subtle gradients, fine textures
- Clean off-white background (#FAFAFA)
- Professional typography, gene names in italic
- Colorblind-friendly palette
```

## Prompt Templates

### Graphical Abstract

```
[TITLE]: "[Study title with species in italics]"

ABSOLUTE REQUIREMENTS:
- NO text labels like "LEFT SECTION", "CENTER AREA"
- NO tier labels like "TIER 1", "TIER 2" as visible text
- Star badge ★OPTIMAL on [optimal treatment] ONLY
- Upregulation ↑ = RED (#E53935), Downregulation ↓ = GREEN (#43A047)
- Use "[ORGAN]" not "HUMAN [ORGAN]" for non-human studies

LEFT (Input/Design):
- [Species] illustration (realistic, anatomically correct)
- Treatment conditions (color-coded cylinders/icons)
- Experimental parameters: "[duration] | [conditions] | n=[sample size]"

CENTER (Multi-level Response):
- Row 1 (Phenotype, coral zone): [growth/quality metrics]
- Row 2 (Tissue): [organ icons with key findings]
- Row 3 (Molecular): [colored gene boxes by pathway]

RIGHT (Pathways):
- Curved pathway arrows connecting to outcomes

BOTTOM (Key Findings):
- 2-3 conclusion boxes with treatment comparisons
- Legend: "↑Upregulation (red) | ↓Downregulation (green)"
```

### Experimental Design

```
EXPERIMENTAL DESIGN for [SPECIES] [trial type].

TOP - Animals:
- [Number] [species] illustration
- Initial parameters: [weight, age, etc.]

MIDDLE - Treatment Groups:
- [N] groups arranged horizontally
- Distinct colored containers per treatment
- GOLD STAR on optimal treatment
- n=[X] per group, [Y] replicates

BOTTOM - Timeline:
- Duration bar: "[X]-day trial"
- Conditions: [temperature, environment]
- Sampling: Growth | Tissue | Molecular icons
```

### Metabolic Pathway

```
METABOLIC PATHWAY showing [factor] effects on [species].

PARALLEL STREAMS:

1. GLUCOSE (Green #4CAF50):
- Molecule structure → Glycolysis enzymes → GLUT transport
- Genes: [list with ↑↓ direction]

2. LIPID (Orange #FF9800):
- Fatty acid → β-oxidation → Lipogenesis
- Genes: [list with ↑↓ direction]

3. PROTEIN/IMMUNE (Blue #2196F3 / Red #F44336):
- Synthesis pathway → Immune response
- Pro-inflammatory (RED): [cytokines]
- Anti-inflammatory (BLUE): [cytokines]

CONNECTIONS: Curved arrows, metabolite flow indicators
```

## Forbidden Elements

Always include in prompts:

```
FORBIDDEN - DO NOT INCLUDE:
- "LEFT SECTION", "CENTER AREA", "RIGHT SECTION" labels
- "TIER 1", "TIER 2", "TIER 3" as visible text
- "HUMAN" prefix for non-human studies
- Placeholder or draft annotations
- Flat design without shadows/gradients
```

## Quality Checklist

Before finalizing:

- [ ] Species terminology correct (no cross-species errors)
- [ ] Gene/protein names follow conventions
- [ ] ↑ arrows RED, ↓ arrows GREEN
- [ ] Optimal treatment starred correctly
- [ ] No forbidden labels present
- [ ] Color coding consistent by pathway
- [ ] Legend complete

## References

- **Paper analysis**: See `references/paper-analysis.md` for analysis framework and planning templates
- **Layout patterns**: See `references/layouts.md` for 4 layout templates
- **Color standards**: See `references/colors.md` for HEX values and pathway colors
- **Vocabulary**: See `references/vocabulary.md` for English terminology
- **Common fixes**: See `references/troubleshooting.md` for iteration tips
