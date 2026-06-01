# Steel-Dogbone-Specimen--fatigue-static-structural-and-buckling-FEA
FEA study of a steel dogbone specimen in ANSYS Workbench 2025 R2. A 50 MPa compressive load was applied to one fixed end to evaluate static stress, fatigue life (1M cycles), and eigenvalue buckling across three linked analyses. Geometry and workflow based on a YouTube tutorial.
# Steel dogbone specimen — fatigue, static structural & buckling FEA

FEA study of a steel dogbone specimen in ANSYS Workbench 2025 R2. A 50 MPa 
compressive load was applied to one fixed end to evaluate static stress, fatigue 
life (1M cycles), and eigenvalue buckling across three linked analyses. 
Geometry and workflow based on a YouTube tutorial.

## Specimen geometry
| Parameter        | Value  |
|------------------|--------|
| Length           | 38 mm  |
| Width (ends)     | 15 mm  |
| Width (waist)    | 5 mm   |
| Fillet radius    | 3 mm   |
| Fillet position  | 8 mm from each end |
| Thickness        | 3 mm   |
| Material         | Structural steel (ANSYS default) |

## Boundary conditions
- Fixed support: bottom face
- Applied load: 50 MPa pressure on top face

## Analyses performed
1. **Static structural** — von Mises stress, total deformation, safety factor
2. **Fatigue** — life, damage, and safety factor at 1,000,000 cycles
3. **Eigenvalue buckling** — 3 modes extracted from pre-stressed state

## Key results
| Analysis | Result                  | Value   |
|----------|-------------------------|---------|
| Buckling | Mode 1 load multiplier  | 0.78173 |
| Buckling | Mode 2 load multiplier  | 2.0094  |
| Buckling | Mode 3 load multiplier  | 5.7321  |

> Mode 1 multiplier < 1 means the specimen buckles before reaching the full 50 MPa load.

## Software
ANSYS Workbench 2025 R2 — Student Edition

## How to open
1. Download `ansys_files/dogbone_analysis.wbpz`
2. Open ANSYS Workbench → File → Restore Archive
3. Pick a working directory and solve
