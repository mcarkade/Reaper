# Workshop files

**Current shop jobs: [four smaller sequential DXFs](Plywood/Batches/README.md).** Cut those four OR the full master once, never both. Their part geometry is identical.
Use the [R5G complete guide](Reaper_Beginner_Assembly_R5G.pdf), [part list](Data/Parts.csv) and [current combined plywood DXF](Plywood/Reaper_ALL_PLYWOOD_R5G_6mm_PROVISIONAL.dxf). All 37 plywood quantities are included across two stock layouts in one file. The older panel jobs in Plywood/Archive_R5F are superseded references.

Measure actual plywood thickness and laser kerf and qualify mating coupons before the full job. Nominal stock is 6 mm, each stock layout is 609.6 Ã— 457.2 mm, and its long X direction is the required face-grain direction. Use millimetres, 100% scale, CUT only. Disable REFERENCE_NOT_CUT and LABELS_NOT_CUT. Select one stock layout at a time unless the bed accepts both; the file spans 1269.2 mm and does not represent one physical sheet. No kerf compensation is encoded.

A18 already includes 0.25 mm per opposed upper receiver-facing edge; do not add that allowance again. Stock remains 6 mm. A43 keeps full-thickness surrounding material and requires only the illustrated local face rebates. A44 stock includes a 3 mm underside tail web: pare the exact sacrificial allowance to the finished taper without shortening the tip before bonding A53. The old A44 trailing-tip trim is superseded. A26 has no motor screw holes and needs real-hardware marking after the physical frame dry-fit. A62_A's old 13.015 mm aft trim is incorporated into the cut length; do not repeat it.

The missed unchanged prints are A23, A36 and HTRB, one each. Use [Print/README.md](Print/README.md); PLA is available, while the source reference recipes specify PLA+. Neither a filename nor a slicer recipe establishes loaded strength. Preserve already completed unrelated prints and foam. Landing-gear hardware remains a later stage.
