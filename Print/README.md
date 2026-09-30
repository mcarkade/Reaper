# Printing the missing and replacement parts / R5F

Print only these five files now: A44_L and A44_R outer ribs, A26 motor mount, A11 left aileron and A21 right aileron. Keep the other parts that are already printed; reprint them only if they fail inspection or their documented dry fit. N1 is the existing owned nose and is not a new print job.

A44_L/R use PLA+, 4 wall loops, 100% rectilinear infill, 0.2 mm layers, a 0.4 mm nozzle, 5 mm brim and supports off. Lay the broad face flat as supplied. Their installed shapes and interfaces are unchanged. Flat printing keeps the main in-plane rib loads in the layer plane. Test the PLA+/wood adhesive on a coupon, dry-fit the real rods and spars, and prove the completed wing under the agreed physical load before use. No polymer strength rating is established. Keep PLA+ below the actual spool's softening range; do not leave the aircraft in a hot vehicle.

A26 uses ASA, 6 wall loops, 100% rectilinear infill, 0.2 mm layers, a 0.4 mm nozzle, 8 mm brim and supports off. The forward broad face rests on the bed; the motor face points upward. Confirm an enclosed, ventilated ASA-capable printer and the exact spool profile before printing. Prusament's reference temperatures are about 260 C nozzle and 110 C bed; they are not an approved profile for the unknown workshop machine. Do not substitute PLA+ automatically. Actual motor seating, safe M3 engagement, supported metal washers, the ASA/wood bond, clamp creep, motor heat and thrust/torque proof remain physical gates. Read Data/A26_Printed_Motor_Design.md.

A11 and A21 are the exact unchanged existing aileron STLs. Their supplied upright orientation requires about 271 mm of printer height. Check the real machine; rotate in the slicer if required, keeping the geometry and scale unchanged. Confirm accessible support removal and the actual print before accepting it.

Use 100% scale in millimetres. STLs do not store slicer settings. Use 4 top and 4 bottom solid layers, and the appropriate manufacturer's spool temperatures. Inspect the actual printer slice. The following table also records the retained print settings for parts already on hand; it is not an instruction to print them again.

| Part | Material | Walls | Infill | Supports | Brim mm |
|---|---|---:|---|---|---:|
| A06 | PLA+ | 2 | 10% gyroid | build plate only | 8 |
| A11 | PLA+ | 2 | 10% gyroid | build plate only | 8 |
| A12 | PLA+ | 2 | 15% gyroid | build plate only | 8 |
| A21 | PLA+ | 2 | 10% gyroid | build plate only | 8 |
| A23 | PLA+ | 3 | 15% gyroid | off | 8 |
| A36 | PLA+ | 3 | 15% gyroid | off | 8 |
| A45 | PLA+ | 4 | 35% gyroid | off | 8 |
| A55 | PLA+ | 4 | 35% gyroid | off | 8 |
| HWR | PLA+ | 3 | 100% rectilinear | off | 5 |
| HWL | PLA+ | 3 | 100% rectilinear | off | 5 |
| HTR | PLA+ | 3 | 100% rectilinear | build plate only | 5 |
| HTL | PLA+ | 3 | 100% rectilinear | build plate only | 5 |
| HTRB | PLA+ | 3 | 100% rectilinear | off | 5 |
| HTLB | PLA+ | 3 | 100% rectilinear | off | 5 |
| FIT_COUPON | PLA+ | 3 | 100% rectilinear | off | 5 |
| A44_L | PLA+ | 4 | 100% rectilinear | off | 5 |
| A44_R | PLA+ | 4 | 100% rectilinear | off | 5 |
| A26 | ASA | 6 | 100% rectilinear | off | 8 |

Filename key: W = wall loops; GYR = gyroid; RECT = rectilinear; SUP = build-plate supports; NOSUP = supports off; L0p2 = 0.2 mm layers; B = brim width in millimetres. New filenames also state their material. Data/Print_Names_and_Settings.csv maps the exact names and orientations; Data/Print_Slices.json records reference slices and exact STL hashes. The reference printer does not establish the owner's printer fit. The fit coupon is available if not already qualified. Landing gear remains deferred and is not included in this print session.
