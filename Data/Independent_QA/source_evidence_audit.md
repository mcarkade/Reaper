# Independent Reaper source evidence audit

Read-only review of existing R5E release worktree and local historical source, 2026-10-01.

## Established source facts

- Existing release `Build_Guide.pdf` is exactly 40 pages. Its text was locally extracted to `R5E_source_guide_text.txt` for searchable QA. R5E source was read from `Manufacturing/Engineering/_work/r5c_release_worktree`; primary dirty Repository was not edited.
- Part IDs A11 (left) and A21 (right) are the missed printed ailerons. Exact STL names are `A11_2W_10GYR_SUP_L0p2_B8.stl` and `A21_2W_10GYR_SUP_L0p2_B8.stl`.
- SHA256 A11: `31bff91bcf0d3b5612319cc6ef40a4998bacbf248f274dcc16e2e2d9577aa1ee`.
- SHA256 A21: `06e28dfe677f0e3cb67f9fc88ff7d9b1b2bd93ff72156e86293e33b199f5781d`.
- Each exact STL hash is identical in Repository, Package, release worktree, and original_r5 delivery_r5d and delivery_r5e. The files need delivery, not redesign.
- Independent Trimesh readback with existing .venv-cad: each aileron is one watertight, consistently wound body with positive volume. A11 dimensions 14.575581 x 74.084172 x 270.888634 mm, volume 132536.502602 mm3; A21 14.572871 x 74.060457 x 270.203979 mm, volume 132320.214804 mm3. The source left/right are slightly nonidentical and must not be replaced with a newly mirrored approximation. Delivered upright orientations need roughly 271 mm print height plus slice clearance.
- Existing print settings: PLA+, 2 walls, 10% gyroid, 0.2 mm layer, 0.4 mm nozzle, build-plate-only support, 8 mm brim. The source orientation has span upright; real printer height remains unestablished. Settings are metadata, not embedded in STL.
- R5E wood is nominal 6 mm stock with local reductions, not a command to thin every member to 5 mm. Source Data/Wood_Assembly_Datums.md records exact A43 gear-bay rebates (1 mm underside, 5 mm remaining) and smaller mating regions for A05/A07/A62. Other physical cut defects are unspecified; no generic recut remedy can be justified.

## Motor discrepancy requiring correction

Exact model documented in source guide and prior inventory: EMAX ECO II 2807 1300KV.

The existing official drawing `_work/electronics/emax-drawing.jpg` was visually inspected. It labels `4-M3` and a `diameter 19` pitch circle through the four bolt centres, equally spaced at 90 degrees and drawn diagonal to cable direction. This establishes nominal adjacent pitch `19/sqrt(2) = 13.435029 mm`; diagonal 19 mm. Drawing envelope diameter 33.9 mm, overall length 34 mm, M5 prop thread. Thread depth is not dimensioned.

R5B release incorrectly claims four holes on a literal 19 x 19 mm square. Current Data/MOTOR_MOUNT_R5B_CHECK.json reports centres X=+/-9.5, Z=-2.5+/-9.5 and diagonal 26.8700577 mm. Source correct_motor_mount.py intentionally changed the earlier PCD pattern using marketing text. The exact R5E PDF p28 repeats the square claim. This is a documented source inconsistency, not merely an inferred bad fit.

Manufacturer page still contains conflicting marketing wording `19*19mm hole pattern`; its linked drawing is the dimensional reference. Before final clamping, compare the real motor against a printed 1:1 drawing and measure thread engagement/winding clearance. A caliper measurement between opposite hole centres resolves 19 PCD versus 19-square immediately: 19 versus 26.87 mm. Supplied M3x8/M3x10 do not establish safe penetration through any revised stack.

Primary page checked during review: https://shop.emaxmodel.com/products/emax-eco-ii-series-2807-1300kv-1700kv-1500kv-brushless-motor-for-rc-drone-fpv-racing

Existing drawing URL: https://cdn.shopify.com/s/files/1/0469/7358/3518/files/ECOII-2807Motor_specifications_200926_-01.jpg?v=1602844068

Propulsion remains unqualified: drawing recommends 6-7 inch props, whereas owned prop is 9045 9-inch three-blade on 4S with nominal 40 A ESC. No measured current/thrust/temperature result is in source.

## Electrical evidence and manual checks

R5E pp30-36 name F405-WING V2, M9N-5883, ASPD-4525, FlySky FS-iA10B, ReadytoSky 40 A, GenX RKI-4897 4S 5200 mAh, RKI-1980 SiK pair, five MG90S (fifth gear later). These later exact names supersede older draft notes saying sensor SKUs were unknown, while hardware label and keyed-connector readback remain required.

Current primary manuals were fetched and checked during this audit:

- https://www.mateksys.com/?portfolio=f405-wing-v2 : MatekF405-Wing target ArduPlane >=4.4; servo Vx defaults 5 V, 5 A continuous/6 A peak. Vx2 on S5-S9 is unpowered unless bridged to Vx (onboard BEC) or separately powered (gap open). iBUS uses RX2 with BRD_ALT_CONFIG=0. V2 current scale is 66.7 A/V; voltage multiplier 11.0. Older general ArduPilot board page says 31.7 and is not the V2 authority.
- https://www.mateksys.com/?portfolio=m9n-5883 : 4-5.5 V, 50 mA, TX->FC RX, RX->FC TX, DA->SDA and CL->SCL; flat compass mounting; keep 10 cm from power lines/ESC/motors/iron. Compass has QMC5883L or QMC5883P depending revision; no invented magnetic offset. R5E nominal placement centre Y=-360 with battery Y=-260 does not prove wire separation or magnetic acceptance.
- https://www.mateksys.com/?portfolio=aspd-4525 : 4-5.5 V, 5 mA, JST-GH order 5V/SCL/SDA/GND. Both pressure tubes must be identified and tested; no pin order inferred from generic box.
- https://ardupilot.org/plane/docs/guide-vtail-plane.html : propeller removed during setup, no transmitter V-tail mixing, explicit servo functions/reversals, physical MANUAL and stabilized directions; combined pitch/yaw endpoints checked for binding.

Source output plan is S1 throttle/function70; S3 left and S4 right aileron/function4; S5/S6 left/right V-tail functions79/80; optional S7 function26 for later gear. This is a starting assignment, not tested aircraft firmware. Neither installed firmware readback nor live hardware calibration was performed in this audit.

R5E says source servo envelopes and provisional 10 mm lever arms are illustrations only. Actual MG90S tabs/arms, pivot pins, captive bends, horn bonding and fasteners need real dry fit. Do not choose exact spoke/thread/screw dimensions from a picture.

## Beginner guide sequence omissions to avoid

- Old guide's skin closure pp23-25 occurs before explicit controls/electronics pp26-35; new sequence must show install/route/test before closure.
- Each assembly action needs an evolving CAD view and identifiable part IDs; one picture shared by three distinct actions does not prove those intermediate fits.
- Printed roots and rails need explicit wood mating and retention; zero interference is not joint proof. N1 already printed; most cutting is finished; no blanket fabrication redo.
- Adhesive brand and ambient cure are not documented. Specify material compatibility, offcut coupon, contact preparation, clamp and full-cure label times; do not invent fixed numeric cure for unidentified glue.
- Landing gear and S7 are deferred after midsems. Structural gear bay members may be installed now, but steering, gear attachment, ground clearance, taxi and flight acceptance remain later gated tasks.
- 20%-chord CG (nominal Y74 mm) is geometric starting point, not validated stability limit. Measurements with final installed mass and pilot acceptance are required.
- Existing Physical_Checks.csv has all statuses NOT DONE. Digital geometry/bench checks cannot become claims of flight readiness, measured thrust or structural capacity.

## Open physical evidence

Necessary actual evidence includes motor base label/pattern match and safe thread depth; rear-frame part thickness/fit if it differs from revised source; real servo tabs and fasteners; printer envelope; adhesive specification; actual pivot/rod fits; loaded servo rail behavior; firmware readback; measured mass/CG; structural joint and exact propulsion proof. Ask only for the specific missing measurement at its dependent step; continue independent work.
