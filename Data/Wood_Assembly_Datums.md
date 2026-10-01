# Reaper R5F wood assembly

There are 34 wooden aircraft pieces in R5F. A44_L/R are PLA+ printed outer ribs; A26 is currently a PLA fit-test plate; the plywood replacement option is conditional on successful fit and actual stock thickness. Retain the other already-cut wood after the documented local fitting checks. Do not recut the whole skeleton.

All stock is nominal 6 mm plywood. Cut the supplied DXFs at 100%, keeping each profile's X direction along the panel's long face grain. Every profile fits within 589.6 Ã— 437.2 mm, allowing a 10 mm margin on the owned 609.6 Ã— 457.2 mm panels. Qualify actual thickness and kerf on a coupon first.

The DXF always describes the **stock blank**. Where a record has `stock_blank` and `secondary_operations`, the final assembly STEP additionally includes local filing, sanding or paring. Do not assume those operations come from the laser. The removal STEP files show the exact small regions; they are tools, not extra aircraft pieces.

## Assembly order

1. Join A62_F and A62_A at Y100 mm on a straight flat jig. Fit A62_DL and A62_DR on opposite faces, spanning Y40â€“160 mm. Align their lower edges with the keel at Zâˆ’41.7139 mm. Each lap bonds to the full 7.5 mm-high keel band for 60 mm on each half: approximately 450 mmÂ² per half per face. The butt ends locate the halves; both glued side laps transfer the joint load.
2. Dry-fit the front and aft horizontal fuselage frames, body formers and keel. Keep the frame upper face at Z0. Use the original former stations listed below. Complete the local fitting operations before applying glue. Do not thin an entire former or frame.
3. Fit the original gear crossmembers and crossplate. Their presence is not a mount specification for the purchased gear: actual gear attachment, steering clearance and load spreading remain owner-specific.
4. Fit the tail-carrier bulkhead and motor firewall fit prototype. A18 occupies Y454.5â€“460.5 mm. A26 occupies Y576.65â€“582.65 mm, retaining the original motor centre at Xâ‰ˆ0, Zâˆ’2.5 mm. **R5F** uses four 3.2 mm clearance holes on the manufacturer's **19 mm bolt circle** (13.435mm adjacent spacing), not the superseded 19 mm square. The two flank receiving notches match nominal 6 mm A43 thickness; the keel slot remains nominal 6 mm. Actual sheet thickness/kerf must be checked before fitting. Trim only A62_A's 13.015 mm rear projection flush to the A26 aft face Y582.65; retain the forward joint. Check the real motor against the printed plate. Fresh R5F checks show that four nominal 6 mm-diameter driver cylinders over the 60 mm forward approach do not intersect the 34 wood parts or A12. The closest lower-driver clearance to A43 is only about 0.218 mm; upper-driver clearance is about 1.218 mm. These nominal gaps are not an actual tool/hand-access acceptance. Check real driver and heads, wood thickness, wires and tail access before closing the shell. EMAX supplies M3Ã—8 and M3Ã—10 screws; through the nominal 6 mm plate these protrude nominally 2 and 4 mm before seating effects. Measure thread engagement and internal clearance rather than choosing a length by appearance.
5. Join each rear wing spar at XÂ±360 mm. The two 100 mm face laps span X310â€“410 on the right and its mirror on the left, giving 50 mm overlap per half. Each face has approximately 300 mmÂ² contact with each half. Cure straight in a jig.
6. Assemble each original-style wing using its front spar, joined rear spar, rear-rod support rib and inner/middle/outer ribs. The entire two 1000 mm rods cross the fuselage centre: front axis Y60.4543/Z15.6325 mm, rear axis Y100.5004/Z15.0705 mm, both running Xâˆ’500 to X500. Do not cut or butt-join them. The outer front-rod seat is an open local rib notch, not an enclosed bore.
7. Fit the wooden aileron endplates to the revised printed controls. A53's inboard datum remains approximately X493, and its six-millimetre thickness extends outboard; the printed control is locally shortened to suit. The outer plate extends away from the moving control. The 2 mm holes are pilots: align and ream them to the actual short bicycle-spoke pivots on the agreed common hinge line. Positive pivot retention is required; a friction fit alone is not established.
8. Dry-fit the original-style foam covering around the completed frame. Make only the documented internal reliefs, preserve the outer paper and check local skin thickness. Weigh the completed structure before subsequent balance/performance work.

## Fixed body stations

| Member | Assembly datum |
|---|---|
| A13 front horizontal frame | Upper face Z0; original front end near Yâˆ’435.01 |
| A34 front former | Forward face Yâˆ’130 |
| A54 body former | Forward face Yâˆ’5 |
| A25 gear crossmember | Forward face Y125 |
| A48 gear crossmember | Forward face Y142.7 |
| A16 body former | Forward face Y233.65 |
| A04 rear body former | Forward face Y384.65 |
| A18 carrier bulkhead | Aft face Y460.5 |
| A26 motor firewall fit prototype | Aft face Y582.65 |

## Local fitting: stock versus finished shape

`Secondary_Dimensions.json` records each removal region's world bounds, stock-face depth interval and sample remaining material. A depth interval of 0â€“6 mm across a bounding box does **not** instruct removal of that whole box: some regions combine a through-notch edge and an adjacent shallow rebate.

- **A43:** four local seating regions at Y125â€“131, Y142.7â€“148.7, Y233.65â€“239.65 and Y384.65â€“390.65. At the first two, remove 1 mm from the underside locally, leaving 5 mm. The body-former seats also retain about 5 mm at representative patches; one original curved rear seat samples about 4.83 mm. Fit against the matching former, preserving the surrounding full-thickness frame.
- **A05_R/L:** local existing root and middle-rib notch/tab regions at span X53â€“59 and X247.35â€“253.35, mirrored on the left. The removal solid combines notch-edge fitting and local face clearance; do not apply one blanket sanding depth across the whole region. Use the actual mating rib and the finished STEP as the stop.
- **A07_R_I/L_I:** root and middle-rib seating regions at those same span stations. Representative mating tabs retain 5 mm after local relief. Keep the rest of each spar at 6 mm.
- **A62_F:** local A54 former seat at Yâˆ’5 to Y1. The representative side relief leaves 5 mm; retain the adjacent keel band.
- **A53_R/L and A07_R_O/L_O:** tiny source edge wedges, approximately 0.03 mm and 0.015 mm maximum respectively. Dress only if the physical dry-fit requires it; retain the source outline and pivot-support material.

The measured contacts establish geometric attachment areas only. They do not establish plywood grade, adhesive strength, fatigue resistance, bending capacity or safe flight. Representative joints, the completed wing/frame and the real hardware still require physical fit and load checks.


R5F: retain the other cut wood and foam. A44 ribs are printed; A11/A21 STLs are unchanged. A26 PLA fit checking is pending. The separate plywood replacement is conditional on fit and actual stock thickness. See A26_Motor_Mount.md.


The original square-pattern A26 plate is superseded. Its replacement decision is pending the PLA dry fit; no A26 contour is included in the current plywood panel jobs.
