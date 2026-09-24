# Print settings

Use owned PLA+, a 0.4 mm nozzle, 0.2 mm layers, 4 top and 4 bottom solid layers, and 100% scale in millimetres. Treat the supplied orientation as a starting point; inspect strength, holes, supports and bed fit in the actual slicer. Use the spool's temperature range and inspect the actual printer's slice before printing. N1 nose is already printed; its reference file is not a new print job.

| Part | Walls | Infill | Supports | Brim mm |
|---|---:|---|---|---:|
| A06 | 2 | 10% gyroid | build plate only | 8 |
| A11 | 2 | 10% gyroid | build plate only | 8 |
| A12 | 2 | 15% gyroid | build plate only | 8 |
| A21 | 2 | 10% gyroid | build plate only | 8 |
| A23 | 3 | 15% gyroid | off | 8 |
| A36 | 3 | 15% gyroid | off | 8 |
| A45 | 4 | 35% gyroid | off | 8 |
| A55 | 4 | 35% gyroid | off | 8 |
| HWR | 3 | 100% rectilinear | off | 5 |
| HWL | 3 | 100% rectilinear | off | 5 |
| HTR | 3 | 100% rectilinear | build plate only | 5 |
| HTL | 3 | 100% rectilinear | build plate only | 5 |
| HTRB | 3 | 100% rectilinear | off | 5 |
| HTLB | 3 | 100% rectilinear | off | 5 |
| FIT_COUPON | 3 | 100% rectilinear | off | 5 |

Filename key: W = wall loops or shells; GYR = gyroid; RECT = rectilinear; SUP = supports from build plate only; NOSUP = supports off; L0p2 = 0.2 mm layers; B = brim width in mm. STLs do not store slicer settings: enter these values in the slicer.

Print the fit coupon first. Measure and try the actual rods, spokes and slots. Then print the 14 files in Individual. Grouped layouts were removed after the workshop found they cost more supports/time; arrange each part in the actual slicer. Only HTR and HTL need horn supports.

Data/Print_Names_and_Settings.csv maps every output name and orientation; Data/Print_Slices.json records the checked geometry hashes and reference slicing results. The unconfirmed printer must fit each envelope with brim and support clearance. A09 and A37 gear fittings are excluded until the bought gear is measured.
