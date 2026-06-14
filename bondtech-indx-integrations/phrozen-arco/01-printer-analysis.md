# Phrozen Arco -- Printer Analysis

Stock printer analysis for INDX integration planning.

## Z-Axis Assembly

The Arco's Z-axis uses a cast aluminum gantry with the following observed components:

### Lead Screw and Guide Rod

- Single lead screw (appears to be T8 or similar trapezoidal) drives the Z platform
- Smooth rod runs parallel for anti-rotation guidance
- Both pass through the upper cast gantry housing

### Upper Gantry Casting

The upper portion of the Z-axis gantry is a cast aluminum piece with:

- **Bearing pockets** -- Hex-shaped internal pockets visible from the rear (for lead screw bearing and rod bushing)
- **Internal ribbing** -- Cross-hatch reinforcement pattern visible through cutouts (provides structural rigidity)
- **Existing bolt holes** -- Multiple threaded holes on the exterior face of the casting

#### Identified Mounting Points

From photo analysis of the Z-axis casting:

**Exterior face (Photo 1 -- front/side view):**
- Upper circled point: Threaded hole near the lead screw pass-through, appears to be M3 or M4
- Lower circled point: Threaded hole below the lead screw, near the smooth rod

**Rear/internal view (Photo 2 -- structure visible):**
- Upper circled area: Hex pocket opening near the bearing seat -- potential clearance concern, not a mounting point
- Lower circled points: Two bolt holes on a flat section of the casting -- good candidates for bracket mounting

These existing holes can potentially be reused for INDX adapter bracket mounting, reducing the need for drilling or tapping new holes.

### Linear Rail System

- Linear rails run vertically on the Z column
- Stock mounting uses brackets clamped to the rail profile
- The rails provide a rigid reference surface for potential INDX dock rail mounting

## Build Volume

TODO: Confirm exact build volume dimensions

- X: TBD
- Y: TBD  
- Z: TBD

### INDX Impact on Build Volume

The dock rail will consume space at the rear Y extent. Estimated Y reduction:

- Tool body depth when docked: TBD (measure from INDX CAD)
- Peel clearance: ~10mm
- Dock structure depth: TBD

## Motion System

TODO: Document XY motion system details

- Motion type: (CoreXY / Cartesian / other)
- X travel: TBD
- Y travel: TBD
- Rail type: TBD

## Electronics

TODO: Document relevant electronics

- Control board: TBD
- Stepper drivers: TBD
- Available stepper outputs for INDX extruder motor
- Available GPIO for any sensors

## Existing Toolhead

TODO: Document stock toolhead for comparison

- Toolhead type: TBD
- Mounting method: TBD
- Fan configuration: TBD

## Photos

> Place reference photos in the `images/` directory and embed them here.

<!-- ![Z-axis front view](./images/z-axis-front.jpg) -->
<!-- ![Z-axis rear structure](./images/z-axis-rear.jpg) -->
<!-- ![Toolholders on 1515 extrusion](./images/toolholders-1515.jpg) -->
