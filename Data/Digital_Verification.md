# Digital verification

The current package contains 112 aircraft CAD identities. FMF and FMT match the reviewed REV3 motor correction; FMGB is removed. All other 110 individual STEP files, all 14 new print STLs, all balsa/foam cutting sheets, stock blanks and reference clearance files are unchanged.

The plywood DXF is the exact published REV3 file, with 32 aircraft pieces and 5 separate test pieces. Cut the test layer first. The current guide, part lists and 179-page paper set use this revision. The revised motor paper profiles match the actual DXFs; every 100 mm paper scale bar was checked.

- [Integration checks](Integration_Checks.json): identities, hashes, counts and recalculated mass/CG.
- [Geometry evidence](Geometry_Verification.json): inherited unchanged-shape checks and separately reviewed motor correction.
- [Guide verification](Guide_Verification.json) and [paper verification](Paper_Verification.json): exact PDFs and visual-review scope.
- [Buildability audit](../Buildability_Audit.md): unresolved construction and physical checks.

Physical_Checks.csv remains a blank test record. None of these checks establishes material strength, glue quality, physical print fit, measured balance, propulsion suitability or flight readiness.
