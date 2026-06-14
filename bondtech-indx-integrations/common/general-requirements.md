# General Requirements

Prerequisites and requirements common to all INDX printer integrations.

## Firmware

- **Klipper** -- INDX integration requires Klipper firmware with multi-tool support
- Tool-change macros for dock/undock sequences
- Per-tool offset calibration (X, Y, Z)
- Global Z offset management

## Motion System Requirements

- **Y-axis clearance** -- Sufficient Y travel to accommodate dock positions behind the build area
- **X-axis range** -- Enough X travel to reach all dock positions plus the full print area
- **Z hop capability** -- Firmware-controlled Z raise during tool changes
- **Repeatability** -- Docking requires consistent positioning; linear rails recommended over rods for XY

## Power Requirements

- Induction heater power supply (TBD -- consult Bondtech specifications)
- Stepper driver for extruder motor (used for both filament drive and latch mechanism)

## Cooling

- Active cooling for the induction heater electronics
- Part cooling fan considerations per tool (passive tools may need carriage-mounted cooling)

## Structural

- Rigid carriage mounting -- tool-change forces are transmitted through the carriage
- Dock mounting must be rigid and repeatable -- any flex causes tool alignment drift
- Consider vibration from rapid XY moves during tool-change sequences

## Build Volume Impact

INDX docks consume Y-axis space at the rear of the build area. The effective print volume in Y is reduced by:

- Dock depth (tool body length when seated)
- Clearance for peel distance (~10mm)
- Any additional structure for dock mounting

Plan dock placement early to understand the real usable build volume.
