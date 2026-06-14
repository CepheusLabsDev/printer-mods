# Phrozen Arco -- INDX Integration

Integration design for the Bondtech INDX tool-changing system on the Phrozen Arco large-format resin-to-FDM conversion / FDM printer.

## Status

**Active Development** -- Mechanical design phase. Analyzing mounting points and designing adapter brackets.

## Printer Overview

The Phrozen Arco is a large-format printer with:

- Cast aluminum Z-axis gantry with internal ribbing structure
- Single lead screw + smooth rod Z-axis drive
- Linear rails on the Z column
- Substantial build volume

## Integration Approach

The INDX integration for the Arco uses a mix of:

- **Existing mounting points** -- Reusing bolt holes in the Z-axis casting
- **New adapter brackets** -- Custom designed brackets for dock and carriage mounting
- **1515 aluminum extrusion** -- Dock rail for toolholder positioning

## Documentation

| Document | Description |
|----------|-------------|
| [Printer Analysis](./01-printer-analysis.md) | Stock Arco specs, Z-axis layout, existing mounting points |
| [Mechanical Design](./02-mechanical-design.md) | Adapter brackets, mounting strategy, clearances |
| [Bill of Materials](./03-bom.md) | Arco-specific components and fasteners |
| [Assembly Guide](./04-assembly-guide.md) | Step-by-step installation with photos |
| [Firmware Configuration](./05-firmware-config.md) | Klipper config, pin mappings, macros |
| [Testing and Calibration](./06-testing-calibration.md) | Validation steps, calibration procedures |

## Quick Links

- [Common INDX Overview](../common/indx-overview.md)
- [INDX Integration Reference](../INDX/docs/integration.md)
- [INDX CAD Reference](../INDX/CAD/)
