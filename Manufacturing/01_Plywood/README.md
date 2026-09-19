# Final plywood fabrication files

Authoritative files: manufacturing_profiles/, revised_assembly_parts/, manufacturing_register.json/.csv, Manufacturing_Profile_Atlas.pdf, shop_layouts/. Source evidence: assembly_profiles/ and assembly_profiles.json. Exclude early diagnostic profiles/ and inventory.json.

22 distinct profiles /31 intended pieces. Order nominal5mm plywood for24 pieces (22 exact5mm plus two A44 Outer_Rib at4.990mm, finish0.01mm),3mm for4 pieces,2.5mm for3 pieces. A40 is merged into A62: do not cut a separateA40. Plywood preferred; balsa requires separate structural judgment.

Native DXF cutting: CUT layer only. LABELS_NONCUT, SANDING_GUIDE_NONCUT and STOCK_NONCUT are not cutting geometry. Unitsmm; no kerf offset or dimensional scaling. Native line/arc/circle/spline curves retained. A24/A44 guide layer shows opposite original cap; sand outer edge to skin/fit, preserve revised sleeve bore. Atlas previews are not paper templates.

Laser sheets: one1220x2440 reference DXF per nominal stock, unchanged by paper optimization. Occupied5mm layout362.82x1117.40mm,3mm36.73x363.17mm,2.5mm101x301.59mm. Grain alongsheetY/long axes of spars. Shop may renest preserving grain. Bounding boxes do not overlap.

A4 paper templates are SEPARATE efficient part-based layouts:5pages for5mm stock,1page for3mm,1page for2.5mm =7pages total, all31 pieces. Landscape287x200mm and portrait200x287mm windows use5mm margins. Every part that fits onepage stays whole. Longparts share striprows:750mm spars3tiles each,887.6mm rearspine4tiles,440/550.7/467mm members2tiles each. Whole smallparts occupy free areas and empty U-profile cutouts. Firstpage of each PDF includes100x20mm calibration within spare space; no extra cover sheet. Join strips in printed TILE1..4 order using paired named marks and10mm common-world overlap. Physical PDFpage order may start with tile4 because it carries calibration. Printable PAGE/TILE identifiers are inside paper margins. Print100%/actualsize with Fit/Shrink disabled. Paper_Page_Manifest.csv and Paper_Layout_Verification.json give everycopy/page/rotation and checks. Native laserDXFs are authoritative; paper curves have0.01mm flattening tolerance.

Quantity evidence: original2000mm assembly has one positive-X occurrence ofA01,A05,A07,A10,A24,A35,A44,A53. Mirror each acrossX=0 for opposite wing; source occurrence1 and intended build2 remain separate. All centered membersqty1. Through-cut plywood uses same profile twice, flipped as needed.

Declared manufacturing changes (full dimensions/coordinates in JSON):
- A01 rear-joiner support hole8.0->8.2mm both wings.
- A24/A35 sleeve holes10.0->10.2mm. AxesY60.454326154274,Z15.632498214492. A24 moved0.09184mm; A35 center unchanged. Exported STEP cylinders checked.
- A04 bottom spine slot5.2mm wide, topZ-30.9; removes1.9893mm2 from profile. Hoop remains one piece; eliminates small spine collision.
- A26 motor mounting holes replaced: original4x3mm/25mmPCD becomes4x3.2mm/19mmPCD per official Emax drawing.12mm central hole/slot preserved. Bolt-hole radial web1.9mm; use washers and verify motor fit before drilling. Pattern comparison PDF/PNG provided.
- A47 gear retention holes2.0->3.2mm forM3 through-bolts/large washers/nyloc nuts. Centers preserved; matching strip modified in root package.
- A62 unifies A40+A62, removes duplicated17742.13mm3 overlap, preserves uniqueA40 geometry. A18/A26 receiving reliefs restored. Native mid-thickness section handles fragmented near-coplanar source caps; resulting solid is a single constant5mm manufacturing spine. Nosewire bypass now deliberately splits A62 into A62F/A62R at3.4mm gap, bridged by two continuous2.5mm aircraft-ply doublers (cutA63qty2; installedA63/A64). Four2.2mm transverseholes receive4M2 bolts: inner2 approximatelyM2x40-45,outer2M2x16,8washers,4lockingnuts. Facegrain along72mm cheeklength; no softbalsa substitution.
- A04,A10,A24,A44 source solids were not perfectly prismatic. Manufacturing contours use selected source cap as a constant-thickness blank. A24/A44 opposite-cap departure sampled~0.45mm; finish edges to skin. These are declared manufacturing changes, not exact source-solid copies.

Validation: all22 individual manufacturing DXFs and3 sheet DXFs audit0errors/mm units; all31 cut-piece occurrences represented by valid solids. Unifiedspine versus all other revised plywood has0intersections>0.01mm3. Paired registration marks checked in actual PDFvector coordinates, maxerror0.0000371mm. PDF100x20mm calibration checked from final vectors; actual longest-cut-segment scale error<0.0000717mm. Sheet CUT entity counts equal allsource copies:550/42/64 for5/3/2.5mm. Flattened perimeter delta5mm sheet0.0159mm over17.7m (<0.0001%), attributable to adaptive curve sampling underrotation; others nearzero. Layout_Verification.json records placements, page maps, paired marks, dimensions and checks.

Stock fit: measured internal loops includeA24 rounded18x5mm slot andA26 rectangular5x10mm slot. Source5mm slots have no nominal sheet allowance. Measure stock and cut a same-machine tab/slot coupon; use machine kerf compensation before production. Geometry verification does not establish plywood strength, motor/gear load capacity or flight readiness.

Numerics: use Gauss-Kronrod volume integration with BSpline span splitting. Default CadQuery and ordinary adaptive Gauss volumes were materially wrong/unstable for these source curves. Source deviations/boolean limits retained as evidence. No approximation silently substituted for claimed original geometry.

Relevant scripts: assembly_profiles.py; revise_manufacturing.py; add_finish_guides.py; unify_spine.py; spine_section_probe.py; finalize_unified_spine.py; revise_motor_pattern.py; relieve_hoop_notch.py; gear_reliefs.py (historical failed nose-notch experiment: do not rerun wholesale); build_shop_layouts.py; verify_layout_outputs.py. Final files/registers are authoritative; some exploration scripts document rejected alternatives and are not a one-command rebuild pipeline.

Final nose-bypass profiles reconstruct their provided manufacturing solids with0.0mm3 missing/extra volumes. A62F133.720x41.714mm, A62R887.615x41.714mm, both5mm; A63qty272x10.7mm at2.5mm. Assembly placementA63left/A64right. revised_assembly_parts/A62_manufacturing.step is the TWO-SOLID assembled reference; A62F/R files are separate cutpieces. Do not add the compound a second time to assembly mass/BOM. LegacyA62.dxf andA40.dxf were removed from cutting folders.

Final paper rebuild: build_efficient_paper.py. Do not rerun build_shop_layouts.py afterward: that older script generates superseded sheet-based paper tiling. Laser layouts remain unchanged.
