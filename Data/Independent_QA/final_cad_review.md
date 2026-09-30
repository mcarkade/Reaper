# Independent R5F CAD review

Reviewed stable release outputs in `task/cad/release` using separately written `audit_final_cad.py`. Checks are frozen by artifact SHA256 in `final_cad_independent_checks.json`.

## Results

- A44_L and A44_R print-orientation STEP each valid, one solid. Independently rigid-transforming the unchanged released installed source to the stated print frame gives zero solid symmetric difference versus actual exported STEP. No rib interface or stock geometry was redesigned.
- A26 DXF actual readback: millimetres (DXF units4), CUT layer only, one valid closed outer contour and four circles radius1.6mm. Extruding the actual DXF in its declared frame by6mm gives a valid solid with zero symmetric difference versus actual exported A26 STEP. Profile area x thickness differs from STEP volume by about3e-10mm3. This proves profile location as well as area.
- New A26 hole adjacent-centre distances are13.4350288425mm and opposite-centre distances19mm. Every new hole material probe returns zero. The four obsolete19mm-square hole-centre probes each now contain42.4115008mm3 of solid, establishing removal of the old erroneous hole pattern.
- Source central shaft opening is keyhole-shaped and belongs to the outer contour, rather than a separate inner wire. Both source and export have zero material in an11mm-diameter centre-cylinder probe and the lower5.8mm-wide slot probe. No missing-centre-hole defect exists. The real motor underside boss still needs normal flush-seating acceptance against this existing opening.
- Both A26 flank receiving slots now pass a1 x6 x0.6mm probe in the newly cleared Z-5.8 to-5.2mm band; this same band was solid in source. Full material remains below the slot atZ-6.8 to-6.2mm. This independently confirms the local5mm-to6mm relief without thinning the entire frame.
- A62_A removed952.1889106mm3. Every removed point is aft ofY582.650mm within numerical tolerance; the source and final clipped forward solids have zero symmetric difference, final adds zero material outside source, and result remains valid with one connected solid. Firewall/keel attachment ahead of the mounting face is preserved.
- Unchanged aileron STL hashes and watertight readback remain verified as in source_evidence_audit.md.

## Scope and remaining acceptance

No independent digital geometry defect found in these reviewed outputs. Valid CAD and mesh are not measured hardware fit, print strength or motor safety. Nominal6mm frame slots require actual stock/kerf dry fit; ECO II2807 base/shaft boss, screw stack and safe thread penetration require actual flush-seating and engagement checks. Printing/slicing, bond qualification, loaded structural proof, propulsion tests, mass/balance, firmware configuration and flight acceptance remain distinct.

No release output or repository file was edited by this audit.
