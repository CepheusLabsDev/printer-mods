# INDX System Overview

## Architecture

The Bondtech INDX is a mechanical tool-changing platform where each tool is a passive, self-contained print head. The system consists of:

1. **Toolhead Carriage** -- Mounts to the printer's XY motion system. Contains the motorised latch (Dynamic Dual Drive) that locks/releases tools.
2. **Tools** -- Passive assemblies containing nozzle, heat break, and filament path. No per-tool wiring or connectors.
3. **Docks** -- Fixed stations where tools park when not in use. Positioned along the Y-axis at the rear of the build area.
4. **Induction Heater** -- Wireless heating system on the carriage. Heats tools without physical electrical connections.
5. **Contactless Temperature Sensor** -- Monitors tool temperature without wired thermocouples.

## Tool-Change Sequence

1. Carriage moves to `clearance_y` (safe Y position clear of all docked tools)
2. Carriage moves in X to align with the target dock
3. Carriage approaches along Y toward the dock
4. At `trigger_y` (dock_y + 5mm), the latch engages/disengages
5. Extruder motor drives the latch mechanism (forward = lock, wiggle sequence = unlock)
6. Carriage retracts to `clearance_y`

## Critical Dimensions

Per the [INDX integration guide](../INDX/docs/integration.md):

| Dimension | Description |
|-----------|-------------|
| `dock_y` | Tool fully seated position |
| `trigger_y` | `dock_y + 5mm` -- latch engage/disengage point |
| `clearance_y` | Safe Y for X travel without clipping docked tools |
| `tool.x` | Per-tool X coordinate for latch alignment |
| Peel distance | ~10mm Y move after seat/pickup before sprinting to clearance_y |

## Clearance Envelope

When designing for INDX, account for:

- **Peel distance** -- ~10mm relative Y move after seating/pickup
- **Z hop** -- Firmware raises nozzle during toolchange approach
- **Carriage width** -- Must not foul adjacent docked tools during X travel
- **Dock structure** -- Must not obstruct the exit path after seating

## CAD Reference

Simplified STEP geometry available at `INDX/CAD/INDX_simplified_1.1.step` for clearance checks and integration modelling.
