# Phrozen Arco -- Firmware Configuration

Klipper configuration for the INDX tool-changing system on the Phrozen Arco.

See [Firmware Base Configuration](../common/firmware-base.md) for common macro structure.

## Arco-Specific Configuration

### Printer MCU and Pin Mapping

TODO: Document Arco control board details

```ini
# [mcu]
# serial: /dev/serial/by-id/...
```

### Stepper Configuration

TODO: Document any stepper changes needed for INDX

### Extruder Configuration

The extruder motor serves dual purpose with INDX:
- Filament drive during printing
- Latch mechanism during tool changes

```ini
# [extruder]
# Existing extruder config modified for INDX latch
```

## Tool Definitions

TODO: Fill in actual coordinates once dock positions are measured

```ini
# Tool 0
# [tool T0]
# dock_x: <measured>
# dock_y: <measured>
# offset_x: 0.0
# offset_y: 0.0
# offset_z: 0.0

# Tool 1
# [tool T1]
# dock_x: <measured>
# dock_y: <measured>
# offset_x: <calibrated>
# offset_y: <calibrated>
# offset_z: <calibrated>
```

## Key Coordinates

| Parameter | Value | Notes |
|-----------|-------|-------|
| `clearance_y` | TBD | Must clear all docked tool bodies across full X range |
| `dock_y` | TBD | Tool fully seated Y position |
| `trigger_y` | dock_y + 5mm | Latch engage/disengage |
| Tool spacing (X) | TBD | Minimum X distance between adjacent docks |

## Macros

### Tool Change

TODO: Arco-specific tool change macro with measured speeds and positions

### Homing Override

TODO: Any homing changes needed with INDX installed

### Safety Checks

TODO: Endstop and travel limit adjustments

## Configuration Files

Complete configuration files will be stored alongside this document:

| File | Description | Status |
|------|-------------|--------|
| `printer.cfg` additions | Core printer config changes | Not started |
| `indx-macros.cfg` | Tool-change macros | Not started |
| `tool-offsets.cfg` | Per-tool calibrated offsets | Not started |
