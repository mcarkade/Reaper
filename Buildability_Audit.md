# Buildability checks — REV4

The digital package now uses 6 mm plywood for every wooden part, short-panel frame and wing joints, and foamboard moving controls. The estimated mass is 2.66 kg. This remains an unbuilt prototype; no physical or flight check is marked complete.

| Item | Digital result | Builder check |
| --- | --- | --- |
| Plywood stock | 87 aircraft profiles fit 2 small panels with specified grain | Measure thickness and kerf. Cut tests first; dry-fit the cured three-layer root tongue. Do not scale the drawing to fix thickness. |
| Frame joints | Paired keel and rail reinforcing pieces have positive contact and clear nearby parts | Jig straight, prepare faces and qualify adhesive/cure on representative joints. Butt ends alone carry no rated load. |
| Wing joints | Staggered cap edge laps and double web face laps retain both whole carbon rods | Prove both joint types and assembled wing/root under a builder-defined load plan. Shape the rod grooves and root relief using the finished model. |
| Wing stiffness | Ideal-bond 3g central estimate: 66.7 mm tip bend, 6.2° slope | Actual plywood, carbon, glue, torsion, joint slip and buckling are unqualified. This is load demand, not a 3g rating. |
| Wing foam | Revised wood clears the original exterior by at least 0.513 mm in the geometric check | Trial the deepest pocket using actual board; preserve paper and inspect for tearing, bulges and weak bonds. |
| Foam controls | Four valid 5 mm blanks, bevels, flanged horns/backers and sampled travel | Prove paper bonds, captive spoke ends, loaded travel and neutral return. Flat controls change the previous camber. |
| Tail and fairing | 6 mm trays raise servos 1 mm; revised inner fairing clears them | Inspect thin opening lips and support removal. Neutral pin spacing is 88.250 mm before actual bend allowances. |
| Foam body | 35 original exterior references plus 4 new flat controls | Use the [body-wrap trial](Data/Foam_Forming_Trial/method.md) before cutting full wraps. Forming and inside relief still need a real-stock trial. |
| Battery | Existing supported shelf and two straps retained; calculated target position is reachable | Weigh the completed aircraft and adjust battery to measured balance. Hot glue only locates the nonslip pad. |
| Motor | Existing corrected FMF/FMT holes and driver access retained | Use TEST_MOTOR. Screws pass through wood and engage the metal motor base; check hole pattern, screw reach, shaft clearance and free rotation. Drill/file only as measured. |
| Gear | Simple plywood legs and owned wheel/axle assemblies | Spread the load into the frame; avoid a pointed leg into foam. Measure wheel offsets, straight tracking and loaded propeller clearance. |
| Pitot | [External two-band trial](Data/Pitot_Installation.md), foam-seam hose route | Keep ports exposed and forward; test grip, hose bends, leaks and removable covers. Do not drill the original nose. |
| Electronics | Connections and setup sequence retained | Propeller off: verify voltage/polarity, FC orientation, each control direction, mixed corners, sensors, throttle cut and failsafes. |
| Propulsion/flight | Current/thrust/temperature of the owned 4S/9045 three-blade combination unknown | Measure the exact setup; an experienced builder/pilot must review flight readiness and runway/abort plan. |

Mass assumptions span 2.20–3.30 kg; this is sensitivity, not a confidence interval. Estimated stall is 39–50 km/h at nominal mass. No guaranteed endurance or takeoff distance is available.

Record actual results in [Physical_Checks.csv](Data/Physical_Checks.csv). Use [the guide](Build_Guide.pdf) for the build sequence; this table identifies what the computer cannot establish.
