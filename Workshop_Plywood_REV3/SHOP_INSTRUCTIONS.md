# Reaper plywood REV3: one file for the laser shop

Use **REAPER_PLYWOOD_6mm_8x4ft_REV3.dxf** only for this plywood order. It replaces the older 33-part plywood sheet.

- Stock: nominal 6 mm plywood, 8 x 4 ft, 2438.4 x 1219.2 mm. Not MDF. Measure actual thickness before the main cut.
- Units: millimetres, 1:1. Do not scale. Face grain along the drawing's X direction.
- Contents: **32 aircraft pieces + 5 test pieces**, one of each ID. Keep every piece labelled. See PARTS_IN_SHEET.csv.
- All cut geometry fits inside approximately **1000 x 500 mm**, although the non-cut stock outline shows the full 8 x 4 ft sheet. If the bed is smaller than the sheet, the shop may prepare an appropriately sized blank or re-nest whole parts without scaling, splitting them or changing grain direction.

## Layer order

1. **TEST_CUT_FIRST**: cut these five pieces first. TEST_FIT has nominal slots 5.8, 6.0, 6.2, 6.4 and 18.3 mm. TEST_LAM1/2/3 are three 30 x 17 mm lamination samples. TEST_MOTOR is a motor-plate fit sample.
2. Check actual material thickness and kerf on the samples. The main design is nominal 6 mm. Its wing tongue has three plywood layers plus glue; the reference receiver gap is 18.3 mm. Do not cut the full set if the measured stack/joint cannot be made to fit. Do not fix a mismatch by scaling the drawing. Contact the team for a dimension adjustment.
3. **CUT_AIRCRAFT**: through-cut only after the material/fit check. Profiles are nominal; no kerf compensation has been applied. The shop must set its own measured inner/outer compensation and cut internal holes before releasing outer contours.
4. **LABEL_DO_NOT_CUT**: optional light marking only. Never through-cut the labels or instructions. If marking is unavailable, label each piece by hand before removing it from the sheet.
5. **STOCK_DO_NOT_CUT**: reference boundary only. Disable cutting on this layer.

## Changed motor parts

FMF has the corrected orientation of its four 3.2 mm holes on a 19 mm circle. FMT is now one connected slotted support that replaces both old FMT and old FMGB. **There is no separate FMGB in this order.** FK is unchanged. Do not mix old motor parts with this revision.

The corrected design clears four nominal 6 mm-diameter screw heads and a 6 mm-diameter, 60 mm-long straight driver. Use the supplied motor hardware after checking it on TEST_MOTOR. Screws pass through wood and thread into the motor's metal base. An 8 mm screw through 6 mm wood projects 2 mm; a 10 mm screw projects 4 mm. Measure real engagement and winding/bottoming clearance. Central shaft/retainer relief, if needed, is a measured drilling operation, not a guessed extra laser hole. Keep the propeller off during fit checks.

## After cutting

These are cutting blanks, not an assembled flight-qualified aircraft. Root-tongue rod grooves, edge dressing, adhesive joints and final sliding fit are workshop operations. Preserve the independent test pieces. Broader foam/control corrections are continuing separately; this file freezes the present plywood scope with the motor-access correction. Physical tests can still require a prototype revision.

Sheet verification: millimetre units; all 32 aircraft IDs exactly once; five test IDs; closed contours; no microscopic cut loops; at least 6 mm part spacing; original 8 x 4 ft stock boundary. All current plywood profiles are unchanged except FMF/FMT, with FMGB removed.
