# Toolholder Specifications

## Tool Body Dimensions

> Refer to `INDX/CAD/INDX_simplified_1.1.step` for precise geometry.

Key dimensions to extract from CAD:

- Tool body width (determines minimum dock spacing)
- Tool body depth (determines dock depth and Y clearance)
- Tool body height (determines Z clearance above dock)
- Latch engagement geometry

## Dock Design

Each dock must:

1. **Rigidly hold the tool** at a repeatable position
2. **Allow smooth Y-axis approach** without binding
3. **Clear the peel distance** (~10mm) after tool seating
4. **Not interfere with adjacent tools** during X travel

### Dock Mounting Options

| Method | Pros | Cons |
|--------|------|------|
| Aluminum extrusion (1515/2020) | Adjustable, rigid, off-the-shelf | Adds depth, requires brackets |
| Direct frame mount | Compact, minimal added depth | Less adjustable, printer-specific |
| Printed brackets on extrusion | Fast iteration, low cost | May lack rigidity for heavy tools |

## Dock Spacing

Minimum X spacing between docks depends on:

- Tool body width
- Carriage width at dock height
- Any clearance margin for safe X travel

## Mounting Pattern

TODO: Document the specific bolt pattern and fastener sizes for dock mounting once confirmed from CAD reference.

## INDX Toolholder Mounting

From the proof-of-concept photos, the INDX toolholders can mount on 1515 aluminum extrusion. The extrusion serves as:

- A rigid mounting rail for multiple docks
- An adjustable platform for dock spacing
- A structural member that can be integrated into the printer frame
