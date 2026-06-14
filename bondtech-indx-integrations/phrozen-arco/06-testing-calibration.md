# Phrozen Arco -- Testing and Calibration

Validation and calibration procedures after INDX installation.

## Pre-Flight Checks

Before any powered testing:

- [ ] All brackets tight with thread locker applied
- [ ] Dock rail level and parallel to X-axis (check with calipers at both ends)
- [ ] No mechanical interference through full Z travel range
- [ ] Wiring secure and routed away from moving parts
- [ ] Toolholders seated and fastened on dock rail

## Phase 1: Motion Verification

### Dry Run (No Tools Loaded)

1. Home all axes
2. Manually jog to each dock X position -- verify no collisions
3. Jog along Y from print area to `dock_y` -- verify clearance
4. Verify Z travel is unobstructed with dock rail installed
5. Check `clearance_y` position clears all dock positions

### Speed Testing

- Run tool-change moves at reduced speed (25%) first
- Gradually increase to target speed
- Listen for unexpected sounds (binding, grinding, loose parts)

## Phase 2: Tool Docking

### Single Tool Test

1. Manually place a tool in Dock 0
2. Run pickup sequence at low speed
3. Verify latch engagement
4. Run drop-off sequence
5. Verify tool seats correctly

### Multi-Tool Test

1. Load all docks
2. Run sequential pickup/dropoff for each tool
3. Verify no cross-contamination (tools stay in correct docks)
4. Run 10 cycles per tool to check repeatability

## Phase 3: Offset Calibration

### Z Offset Calibration

For each tool:
1. Pick up tool
2. Run standard Z offset calibration (paper test or probe)
3. Record offset
4. Repeat 3 times for consistency
5. Store averaged offset in `tool-offsets.cfg`

### XY Offset Calibration

1. Print calibration pattern with Tool 0 (reference tool)
2. Print same pattern with each subsequent tool
3. Measure X and Y offset between patterns
4. Store offsets in `tool-offsets.cfg`

## Phase 4: Print Testing

### Single-Tool Print

- Print a known test model with Tool 0 only
- Verify print quality matches pre-INDX baseline

### Multi-Tool Print

- Print a two-color test model
- Check layer registration between tools
- Inspect tool-change area for stringing or blobs

## Troubleshooting

| Symptom | Possible Cause | Fix |
|---------|---------------|-----|
| Tool doesn't seat fully | Dock misaligned | Re-align dock rail, check Y coordinates |
| Latch won't engage | Extruder motor misconfigured | Check E motor direction and steps/mm |
| Tool offset drifts | Dock flex | Reinforce dock rail brackets |
| Collision during X travel | `clearance_y` too close | Increase `clearance_y` value |
| Z binding after install | Bracket interferes with Z axis | Check clearance, modify bracket |

## Calibration Log

| Date | Tool | Z Offset | X Offset | Y Offset | Notes |
|------|------|----------|----------|----------|-------|
| -- | T0 | -- | 0.0 (ref) | 0.0 (ref) | Reference tool |
| -- | T1 | -- | -- | -- | -- |
