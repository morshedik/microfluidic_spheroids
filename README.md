# Microfluidic Spheroids

Reproducible analysis framework for experiments that generate, culture, image, or
perturb multicellular spheroids in microfluidic devices.

## Project status

**Study-design stage.** This repository does not yet contain an analyzed dataset or a
validated biological conclusion. The immediate goal is to define the experiment,
outcomes, controls, and analysis contract before adding notebooks or model code.

## Questions this repository should answer

1. What biological system and microfluidic geometry are being studied?
2. Which intervention is varied: flow, matrix, cell composition, treatment, oxygen, or
   another registered factor?
3. What is the experimental unit: device, channel, well, spheroid, field, or cell?
4. Which measurements are primary and which are exploratory?
5. How are device, batch, operator, and biological replicate effects separated?
6. What constitutes independent validation?

These questions must be answered in [docs/STUDY_DESIGN.md](docs/STUDY_DESIGN.md)
before inferential analysis begins.

## Proposed repository structure

```text
microfluidic_spheroids/
├── README.md
├── docs/
│   └── STUDY_DESIGN.md
├── data/
│   └── README.md
├── analysis/
│   └── README.md
├── notebooks/          # Exploration only; no canonical final statistics
├── src/                # Reusable image/data processing functions
├── tests/              # Synthetic and unit tests
└── results/            # Generated outputs, not hand-edited
```

## Minimum analysis standard

- Preserve raw data unchanged.
- Use stable sample and device identifiers.
- Record exclusions before inspecting treatment effects.
- Avoid treating many cells or images from one device as independent replicates.
- Split training and evaluation by biological replicate or device, not by image tile.
- Report effect sizes and uncertainty, not only p-values.
- Include segmentation and measurement quality-control panels.
- Freeze the primary endpoint before model tuning.

## Next milestone

Complete the study-design document with the actual biological system, device design,
replicate structure, primary endpoint, controls, and available data modalities. Only
then should the repository select an image-analysis or statistical stack.

No license or reuse terms have been selected.
