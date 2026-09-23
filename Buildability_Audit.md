# Reaper buildability audit

**The plywood motor-access correction is complete in REV3. The whole aircraft is still a prototype, not a proven beginner kit or a flight-approved design.** No physical build or flight tests were completed by this audit.

Use the [single REV3 plywood DXF](Workshop_Plywood_REV3/REAPER_PLYWOOD_6mm_8x4ft_REV3.dxf) with its [shop instructions](Workshop_Plywood_REV3/SHOP_INSTRUCTIONS.md). It contains 32 aircraft pieces and five test pieces. The current findings do not justify further plywood changes. Cut the test pieces first; actual material and hardware fit can still require a prototype adjustment.

## What is resolved

FMF has four 3.2 mm holes on a 19 mm circle, rotated 45 degrees from the earlier pattern. The new FMT combines the former cross tie and base, with two 7 mm driver openings. Separate FMGB is removed; FK remains unchanged. Do not mix old and revised motor parts.

The revised geometry clears all four tested screw-head envelopes, 6 mm diameter by 3.5 mm high, and straight driver corridors, 6 mm diameter by 60 mm long. The minimum driver clearance is 0.5 mm. These envelopes are explicit assumptions, not measurements of the supplied hardware. See the [sheet verification](Workshop_Plywood_REV3/INDEPENDENT_CHECK.json).

Motor screws pass through plywood and thread into the motor's metal base. Before the main cut, use TEST_MOTOR to check the real hole pattern, head clearance, screw engagement and rear shaft/retainer projection. Confirm that no screw bottoms out or touches a winding. Any needed central relief must follow measurement. Keep the propeller off during these checks.

## What still needs work

| Item | Current evidence | Next practical check |
| --- | --- | --- |
| Plywood fit | Profiles use nominal 6 mm thickness. Three root layers form an 18 mm tongue in an 18.3 mm receiver. | Measure stock at several positions. Cut the slot and lamination samples; include cured glue thickness. Never scale the whole drawing to fix thickness. |
| Aileron setup | Straight-down servo-arm indexing puts the nominal +15-degree surface position close to a geometric limit. A forward-indexed arm is a promising setup correction. | Trial the actual factory arm, retained spoke bends and measured travel before changing printed parts. |
| Foam construction | The 35 patterns are outer-surface references. A broader body-wrap trial now supplies dimensions, crease marks and a profile reference. | Prove the actual stock forming, inner relief and bonds before the full cut. |
| Wing skin | The deepest beam pocket leaves about 0.5 mm of outer foam/paper in the model. | Form and pocket actual stock without tearing, bulging or an unreliable bond. A failed trial may require a revised interface. |
| Pitot | A simple external tape-on trial and foam-seam hose route are now described. N1 and plywood stay unchanged. | Fit the actual probe to the nose curve; prove two-band retention, exposed ports, hose bends and cover access. |
| Loads and flight | Geometry and calculation checks do not establish strength, control authority, propulsion suitability or stability. | Complete representative structural, loaded-control, propulsion, balance and ground tests before a pilot approves flight. |

## Battery: simple restraint, with real support

Use two broad releasable Velcro straps, a nonslip pad and smooth bearing surfaces. The straps must loop through or around load-bearing wood. Small adhesive spots may locate the pad or straps; they are not the primary restraint. Do not tighten hard zip ties directly around the battery or leave sharp edges pressing into it.

The 512 g pack produces about 15 N at an illustrative 3g and 25 N at 5g. These are load examples, not approved proof-test levels. Do not assume two straps share load equally.

Keep FBT, FBWL, FBWR and FBC in the current build. At the estimated balance position, most of the pack and both preferred strap rows lie ahead of the main FLR/FLL rails. Removing the tray therefore removes a real forward support. It also affects GPS support, the airspeed board, pitot mounting and battery removal.

The tray and its three supports are estimated at 102 g. The eight balsa body-former pieces total only about 5 g, and ten equipment-support pieces about 13 g. Fewer pieces might simplify assembly, but deleting them is not automatically a meaningful weight saving. No member of the current primary frame has been demonstrated redundant.

## Aileron: test an arm-indexing correction first

The numerical candidate uses the existing 10 mm servo-arm hole with the arm approximately **15 degrees forward from straight down**, followed by fitting the spoke while the surface is held neutral. It requires no change to the plywood, servo cradle or printed horn in the kinematic model.

For the nominal right-side coordinates, effective joint-centre distance is **31.175 mm**. This is not the spoke cut length; add and form the actual retained ends. Surface travel of -15 to +15 degrees requires physical arm angles of approximately -51.43 to +20.99 degrees, or -36.43 to +35.99 degrees relative to the indexed neutral. The positive geometric limit moves from about 15.77 to 25.68 degrees.

A sampled calculation covering 1,536 combinations of 0.5 mm position and rod-length errors remained reachable after remeasuring the rod at neutral. The largest physical arm angle was 57.77 degrees, within the previously checked nominal ±60-degree arm envelope. This is sampled numerical evidence, not guaranteed servo travel or tolerance for every real assembly.

Actual spline indexing, arm-hole radius and spoke diameter remain measurements. The CAD straight-rod approximation clears the wing structure but enters the horn near the end joint; the original setup has the same modelling limitation. The retained bend, free articulation and withdrawal resistance must be demonstrated. Set endpoints by measured surface travel and check both mirrored wings for binding, buzzing, flex and rubbing under load. Do not publish the candidate as a proven fix until that trial passes.

## Foam: valid outlines are not a complete building method

F14, F18 and F33 are only about 5.28 mm wide. They are real bottom exterior surfaces, not mistaken thickness faces or duplicate material. Their areas must remain part of the skin. The avoidable difficulty is making separate pieces at every CAD face boundary.

The forward and middle lower body can geometrically use one 157.4 x 573.7 mm outside-paper wrap, or two wraps of lengths 205.0 and 368.7 mm. This preserves the rounded shape and all wood while replacing ten narrow-piece seams. The [forming trial](Data/Foam_Forming_Trial/method.md) includes actual region order, crease positions, a full-size outer-section reference and a 40 mm-long coupon procedure. It remains an alternative to the released outlines until tested on actual stock.

Treat the existing [reference profiles](Reference_Profiles/) and paper patterns as geometric references until a representative build establishes the method. The new body trial supplies the mating order and forming sequence. Actual relief depths, pocket fitting and adhesive performance still need stock trials; the wing and compound-curved rear body are not covered by the constant-section wrap. All 35 released outlines still contain zero score entities.

Use the actual nominal 5 mm paper-faced XPS board. Measure thickness and mass; test paper peeling, bending and adhesive compatibility. Do not assume it behaves identically to another brand of foamboard. A guide cannot make a 0.5 mm remaining skin easy or repeatable by wording alone.

The reference-pattern area is about 0.819 m² across three 0.6 m² sheets. The third sheet is mostly reusable offcut. Better nesting may save stock, but does not remove difficult seams. Two-sheet feasibility has not been established.

## Pitot: start with a reversible tape-on trial

The [pitot method](Data/Pitot_Installation.md) uses a thin pad and two tape bands on the outside of N1, with both hoses routed outside to a foam-cover seam and around the battery shelf's open rear edge. Keep every pressure hole exposed and the tube aligned forward. Do not drill N1. The real nose taper and hardware decide whether this placement works; check retention, hose bends, pressure integrity and cover removal. The old internal tab route is a more involved alternative, not a requirement.

## Strength and performance remain conditional

Current estimates are about 2.55 kg flying mass, with a 2.12–3.15 kg assumption range, and 0.304 m² wing area. These are not measured finished values. The provisional balance target is not a verified stability margin.

The central illustrative 3g beam calculation predicts approximately **106 mm tip deflection and a 10-degree tip slope**. That is a substantial stiffness concern. The calculation assumes ideal bonds, a fixed root and estimated material properties, without foam stiffness credit; its large slope also limits small-deflection accuracy. It supplies demand estimates, not allowable strengths or a load rating. Actual bending, torsion, root joints and adhesive integrity remain unqualified.

Estimated stall scenarios are approximately 38–49 km/h at nominal mass, or roughly 35–55 km/h across the wider assumptions. Endurance of 15–17 minutes assumes about 15 A average current. Neither speed nor current has been measured in flight. The exact 4S/9045 three-blade propulsion combination lacks current, thrust and temperature qualification; the motor's published application data cover smaller props. Required runway length is unknown.

Before powered flight, weigh and balance the completed aircraft with its real equipment, verify retained and loaded controls, establish propulsion limits, inspect the complete load paths, and complete tracking, failsafe and ground checks with an experienced builder and pilot. Record results in [Physical_Checks.csv](Data/Physical_Checks.csv). Until then, successful cutting, printing or digital clearance checks do not establish flight readiness.
