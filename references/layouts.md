# Layout Patterns

## Pattern A: Three-Column Horizontal Flow

Best for: Graphical abstracts, mechanism summaries

```
┌──────────────┬──────────────────────┬──────────────┐
│    INPUT     │   PROCESS/PATHWAY    │   OUTPUT     │
│  (处理/输入)  │    (代谢通路)         │  (结果/表型)  │
└──────────────┴──────────────────────┴──────────────┘
```

**Prompt snippet:**
```
LAYOUT: Left-to-right flow, three main sections

LEFT (30% width): Experimental inputs
- Subject illustration
- Treatment conditions
- Parameters box

CENTER (40% width): Mechanisms
- Multi-tier response (Molecular → Tissue → Organism)
- Pathway connections

RIGHT (30% width): Outcomes
- Regulatory pathways
- Key findings
```

## Pattern B: Vertical Tier Structure

Best for: Multi-level biological responses

```
┌────────────────────────────────────────────────────┐
│         ORGANISM LEVEL (Phenotype)                 │
├────────────────────────────────────────────────────┤
│         TISSUE LEVEL (Organs)                      │
├────────────────────────────────────────────────────┤
│         MOLECULAR LEVEL (Genes)                    │
└────────────────────────────────────────────────────┘
```

**Prompt snippet:**
```
LAYOUT: Top-to-bottom hierarchy, three tiers

TOP TIER (Organism): Growth, survival, quality metrics
MIDDLE TIER (Tissue): Liver, intestine, muscle panels
BOTTOM TIER (Molecular): Gene expression boxes by pathway
```

## Pattern C: Radial Network

Best for: Central organ with multiple pathways

```
                    ┌─────┐
                    │LIVER│
                    └──┬──┘
         ┌─────────────┼─────────────┐
         ▼             ▼             ▼
    ┌─────────┐  ┌─────────┐  ┌─────────┐
    │Glycolysis│  │Lipolysis│  │ Immune  │
    └─────────┘  └─────────┘  └─────────┘
```

**Prompt snippet:**
```
LAYOUT: Radial design with central hub

CENTER: Main organ/tissue icon
RADIATING: 3-6 pathway modules as organic cloud shapes
CONNECTIONS: Curved arrows from center to modules
ANNOTATIONS: Key genes/metrics within each module
```

## Pattern D: Factorial Design Matrix

Best for: Multi-factor experimental designs

```
              Factor A (Temperature)
              15°C    20°C
Factor B    ┌───────┬───────┐
(C:L)    0.8│  T1   │  T4   │
         1.0│  T2★  │  T5   │
         1.6│  T3   │  T6   │
            └───────┴───────┘
```

**Prompt snippet:**
```
LAYOUT: Grid matrix showing factorial design

HEADER ROW: Factor A levels with icons (e.g., thermometer)
HEADER COLUMN: Factor B levels with icons
CELLS: Treatment containers with subjects inside
HIGHLIGHT: Star on optimal combination
FOOTER: Timeline and sampling flow
```

## Combining Patterns

For complex figures, combine patterns:

- **A + B**: Horizontal flow with vertical tiers in center
- **B + C**: Tiers with radial pathway details
- **A + D**: Input matrix flowing to outcomes
