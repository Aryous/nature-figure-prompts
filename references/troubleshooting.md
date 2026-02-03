# Troubleshooting & Iteration Tips

## Common Problems and Fixes

| Problem | Symptom | Fix |
|---------|---------|-----|
| Layout labels appear | "LEFT SECTION", "CENTER AREA" visible | Add `FORBIDDEN: text labels like 'LEFT SECTION'` |
| Tier labels visible | "TIER 1", "TIER 2" shown | Add `NO tier labels as visible text` |
| Star on wrong treatment | ★OPTIMAL on Diet 1 instead of Diet 2 | Specify `star ONLY on Diet 2, NOT on Diet 1 or 3` |
| Wrong organ terminology | "HUMAN LIVER" in fish study | Declare species upfront, use `"LIVER" not "HUMAN LIVER"` |
| Color inconsistency | ↑ arrows not red, ↓ not green | Add complete color rules with HEX values |
| Flat design | No depth or shadows | Add `volumetric 3D, soft shadows, subtle gradients` |

## Iteration Strategy

```
Pass 1: Layout and major elements
├── Check overall structure matches template
├── Verify main sections present
└── Confirm subject illustration quality

Pass 2: Details and corrections
├── Fix any forbidden labels
├── Correct star/badge positions
├── Verify organ/species terminology
└── Check arrow directions

Pass 3: Polish
├── Color consistency
├── Typography quality
├── Legend completeness
└── Final visual balance
```

## Prompt Strengthening Techniques

### Use ABSOLUTE/CRITICAL Keywords

```
ABSOLUTE REQUIREMENTS:
- [requirement 1]
- [requirement 2]

CRITICAL PLACEMENT:
- The star goes on [specific element] ONLY
```

### Use Explicit Negation

```
FORBIDDEN - DO NOT INCLUDE:
- [element 1]
- [element 2]

NOT on Diet 1, NOT on Diet 3
```

### Use Position Redundancy

```
Diet 2 (C:L=1.0): Teal cylinder, WITH ★OPTIMAL badge
- The MIDDLE cylinder
- The TEAL/CYAN colored one
- WITH the golden star
```

## Quality Thresholds by Document Type

| Document | Threshold | Iterations | Post-processing |
|----------|-----------|------------|-----------------|
| Nature/Science/Cell | 9.0/10 | 3-5 | Required |
| Standard SCI | 8.0/10 | 2-3 | Light |
| Thesis | 7.5/10 | 2 | Optional |
| Poster | 7.0/10 | 1-2 | Minimal |
| Presentation | 6.5/10 | 1 | None |

## When AI Cannot Fix

Some issues require manual post-processing:

- Precise text alignment
- Exact color matching to brand guidelines
- Complex overlapping annotations
- Multi-language text
- Very specific logo placements

Tools for post-processing:
- Adobe Illustrator (vector editing)
- Photoshop (raster editing)
- Figma (collaborative design)
- BioRender (scientific figures)
