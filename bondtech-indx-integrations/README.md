# Bondtech INDX Printer Integrations

Custom integration designs for the [Bondtech INDX](https://www.bondtech.se/indx/) automatic tool-changing system across multiple 3D printer platforms.

## What is INDX?

The Bondtech INDX is a modular, mechanical tool-changing platform for FDM/FFF printers. Each tool is a self-contained print head that docks and undocks via a Y-axis approach. The carriage carries a motorised latch driven by the extruder motor -- no per-tool electronics or connectors needed.

Key capabilities:

- Wireless induction heating and contactless temperature sensing
- Thin, passive tool bodies enable rapid swaps
- Contamination-free multi-material printing
- Adaptive Dynamic Dual Drive technology for latch and filament feed

For full integration reference geometry and documentation, see the [INDX submodule](./INDX/).

## Printer Integrations

| Printer | Status | Directory |
|---------|--------|-----------|
| Phrozen Arco | Active development | [phrozen-arco/](./phrozen-arco/) |
| Sovol SV08 Max | Planned | [sovol-max/](./sovol-max/) |
| Sovol Zero | Planned | [sovol-zero/](./sovol-zero/) |
| Peopoly Magneto X | Future | -- |

## Repository Structure

```
bondtech-indx-integrations/
  INDX/                    # Git submodule -- official Bondtech INDX reference repo
  common/                  # Shared docs: INDX overview, requirements, firmware base
  phrozen-arco/            # Phrozen Arco integration design and guides
  sovol-max/               # Sovol SV08 Max integration (planned)
  sovol-zero/              # Sovol Zero integration (planned)
```

## Common Documentation

Shared resources applicable to all integrations:

- [INDX System Overview](./common/indx-overview.md) -- Architecture, tool specs, core requirements
- [General Requirements](./common/general-requirements.md) -- Power, cooling, firmware prerequisites
- [Toolholder Specifications](./common/toolholder-specs.md) -- Dimensions, mounting patterns, dock design
- [Firmware Base Configuration](./common/firmware-base.md) -- Common Klipper macros and tool-change sequences
- [Common BOM](./common/bom-common.md) -- Shared components across integrations

## Reference Material

- [INDX Integration Overview](./INDX/docs/integration.md) -- Official dock geometry, tool positions, clearance envelope
- [INDX CAD Reference](./INDX/CAD/) -- Simplified STEP geometry for clearance checks
