# Current plywood cutting job

**Current shop jobs: [four smaller sequential DXFs](Batches/README.md).** Cut all four once OR the full master once, never both. Their part geometry is identical.
[Reaper_ALL_PLYWOOD_R5G_6mm_PROVISIONAL.dxf](Reaper_ALL_PLYWOOD_R5G_6mm_PROVISIONAL.dxf) contains all 37 aircraft pieces, one of each listed ID, across two 609.6 Ã— 457.2 mm stock layouts. [Layout image](Maps/ALL_PLYWOOD_R5G_Layout.png), [part map](PART_TO_PANEL.csv) and [manufacturing map](Manufacturing_Map.json) identify the pieces. Individual DXFs are the same profiles used in the combined file, for reference; do not cut a second set.

Use nominal 6 mm plywood, millimetres, 100% scale and CUT only. Keep stock face grain along each panel's +X/long direction. A18 is intentionally rotated 90 degrees in this layout to carry its physical grain correctly. Reference stock borders and labels must not cut. Each layout is a separate stock sheet; panel 2 starts at X659.6 mm in the combined file. Nominal minimum part gap is 5 mm; geometric serialization differs by under 0.000004 mm. The shop must measure actual kerf, thickness and machine limits before cutting; no kerf offset is encoded.

All digital profiles and nominal extrusions passed independent readback, source-profile comparison, overlap/spacing, grain and quantity checks. Physical fit and strength are unverified. Qualify representative coupons and dry-fit the actual printed A12 receiver and wood interfaces before committing the complete cutting run.

A43 shallow seats, A62_F's A54 seat, spar seating relief and other existing source secondary operations do not come from laser through-cutting. Follow the guide and [wood datums](../Data/Wood_Assembly_Datums.md). A44's stock-only underside tail allowance must be pared to the finished profile, preserving its full tip and A53 bond area. [Reference paring profiles](Paring_Templates) are explicitly not laser jobs.

Old separate R5F panel files and maps in Archive_R5F are superseded. The current cutting entry is the single R5G combined DXF above.
