# Body and tail: 6 mm plywood conversion

22 non-wing balsa parts become actual 6 mm plywood through-cuts. Estimated mass changes from 22.50 g to 100.88 g (+78.38 g), using balsa 160 kg/m3 and plywood 600 kg/m3. Weigh actual parts. This is not structural qualification.

Existing plywood frame, TROOT, N1 and FCF remain unchanged. GPS shelf top stays Z52; posts shorten to meet underside Z46. FF2 grows aft; FF3 grows forward and has through-notches for the thicker trays.

## Former assembly datums

Measure aft from FK_F front tip Y-335 to each former FRONT face:

| Group | Parts sharing front plane | Front station (mm) | Installed front Y (mm) |
|---|---|---:|---:|
| FF0 | FF0R, FF0U, FF0L | 204.50 | -130.50 |
| FF1 | FF1 | 329.50 | -5.50 |
| FF2 | FF2R, FF2U, FF2L | 568.65 | 233.65 |
| FF3 | FF3 | 718.65 | 383.65 |

Align front faces, not centres. FF2R/L were moved aft 0.5 mm to align with FF2U; cutting outlines did not change. Replace old guide stations 205/330/568.65/719.65 mm. Exact coordinates and numerical plane agreement are in assembly_datums.json.

TRS/TLS remain intact at Y450..456. Align face grain with the inclined spine axis. Widen the inner tail-foam spine pockets 1 mm aft. Revised FTF locally clears the spines and raised servo/tray positions, removing 419.50 mm3 and remaining one solid. Global minimum remaining wall is not established; inspect sliced openings and the first print.

MTR/MTL stay on Z0 and now end at Z6. ETR/ETL rise 1 mm. Fit local FSU2 and fixed-tail foam relief without forcing the cover. Existing exterior foam templates remain applicable; internal relief is assembly work. Original 0.0224 mm nominal servo seating discrepancy remains: lightly dress the seat to the actual servo.

Right tail servo-axis reference: (63.85, 411.1, 12.115) mm; mirror X for left. Neutral spoke pin spacing: 88.250 mm before bend allowances. Centre servo before measuring. Keep combined rudder/elevator travel inside +/-20 degrees. Both tail controls clear at 41 sampled positions each; 82 exposed straight-rod positions clear. Actual factory arms and retained bends remain unmodeled. Horn lateral shift is -1.684 to +0.453 mm; physically sweep both ends through full mixed travel to check binding.
