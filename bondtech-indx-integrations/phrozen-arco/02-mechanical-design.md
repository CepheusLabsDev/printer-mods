# Phrozen Arco -- Mechanical Design

Adapter bracket design and mounting strategy for the INDX integration.

## Design Strategy

The integration uses a hybrid approach:

1. **Reuse existing mounting holes** on the Z-axis casting where possible
2. **Design new adapter brackets** for dock rail mounting and carriage adaptation
3. **1515 aluminum extrusion** as the dock rail (proven in proof-of-concept)

## Dock Rail Assembly

### Rail Selection

- 1515 aluminum extrusion (confirmed from toolholder proof-of-concept)
- Length determined by number of tools and required spacing

### Rail Mounting

The dock rail needs to be:

- Rigidly mounted to the printer frame
- Positioned at the correct Y coordinate for docking
- Level and parallel to the X-axis travel

#### Mounting Options Under Consideration

| Option | Description | Status |
|--------|-------------|--------|
| Direct to Z-gantry casting | Use existing threaded holes on casting face | Investigating fit |
| Frame-mounted brackets | New brackets attached to main frame extrusions | Backup option |
| Hybrid | Casting holes for alignment, frame for structural load | Preferred if feasible |

## Adapter Brackets

### Dock Rail Brackets

Purpose: Connect 1515 dock rail to the printer frame/gantry

Design constraints:
- Must not interfere with Z-axis travel
- Must clear lead screw and smooth rod
- Rigid enough to maintain dock alignment under tool-change forces
- Accessible fasteners for adjustment

Material options:
- 3D printed (PETG/ABS) for prototyping
- Aluminum for final design (if rigidity insufficient with printed parts)

### Carriage Adapter

Purpose: Mount INDX toolhead carriage to the Arco's XY motion system

Design constraints:
- Compatible with existing XY carriage mounting pattern
- Correct Z height for tool engagement
- Clearance for induction heater module
- Does not reduce XY travel range

TODO: Document carriage adapter design once XY system is analyzed

## Clearance Analysis

### Z-Axis Clearances

- Lead screw to dock rail: TBD
- Smooth rod to dock rail: TBD
- Z-platform to docked tools at home: TBD

### XY Clearances

- Carriage width vs dock spacing: TBD
- Y travel available for dock approach: TBD
- X travel for reaching all dock positions: TBD

## CAD Files

Custom parts will be stored in the `cad/` directory:

| File | Description | Status |
|------|-------------|--------|
| `dock-rail-bracket.step` | Dock rail mounting bracket | Not started |
| `carriage-adapter.step` | XY carriage to INDX adapter | Not started |

## Design Iteration Log

Track design changes and decisions here:

| Date | Change | Reason |
|------|--------|--------|
| 2026-04-08 | Initial analysis started | Photo review of Z-axis mounting points |
