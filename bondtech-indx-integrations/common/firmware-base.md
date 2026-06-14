# Firmware Base Configuration

Common Klipper configuration and macros for INDX tool-changing across all printer integrations.

## Prerequisites

- Klipper firmware with multi-tool support
- Familiarity with Klipper configuration and macro syntax
- Access to printer's `printer.cfg` and macro files

## Tool Definitions

Each tool requires a definition with its dock position and offsets:

```ini
# Example tool definition (printer-specific values)
# [tool T0]
# dock_x: <x_position>
# dock_y: <y_position>
# offset_x: 0.0
# offset_y: 0.0
# offset_z: 0.0
```

## Core Macros

### Tool Change Sequence

The fundamental tool-change macro follows this flow:

1. Retract filament (if active tool loaded)
2. Move to `clearance_y`
3. Move to current tool's `tool.x`
4. Approach `dock_y` along Y
5. Unlock latch (wiggle sequence: Y + E moves)
6. Retract to `clearance_y`
7. Move to new tool's `tool.x`
8. Approach new tool's `dock_y`
9. Lock latch (forward E move)
10. Retract to `clearance_y`
11. Apply new tool's Z offset
12. Resume printing

### Latch Control

- **Lock**: Forward extruder move engages gear mesh and clamps tool
- **Unlock**: Wiggle sequence (coordinated Y + E moves) to mesh activation gear before pull-away

### Z Offset Management

- Per-tool Z offset stored in tool definition
- Global Z offset persists across reboots
- Applied automatically after tool pickup

## Printer-Specific Configuration

Each printer integration will have its own firmware config that extends this base with:

- Specific dock coordinates
- Stepper pin mappings
- Speed and acceleration values for tool-change moves
- Safety checks (endstop positions, travel limits)

See individual printer directories for complete configurations.
