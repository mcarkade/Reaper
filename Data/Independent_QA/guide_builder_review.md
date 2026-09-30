# Independent beginner-guide builder review

Initial R5F 60-page draft read end to end as instructions. Critical CAD views rendered and independently inspected at pages6,12,15,17,20,23,25,28,29,30,32,33. Layout in these selected views was readable, labels identified real part IDs, intermediate CAD frames were present, and electrical tables/foldout contained actual nets. Author owns complete final-page visual inspection.

## Concrete defects sent to author and resolved in the final PDF

1. Servo arms required electrical centering in Steps16/19 before FC wiring/configuration, with no tester or temporary setup instructions. Requested verified standalone5V tester, explicit signal/positive/ground, factory-arm installation after centre, or open-install return gate.
2. Step29 demanded simultaneous four-servo FC movement before firmware target/output assignment in Step32. Requested configure/readback and loaded-servo/physical directions before final skin closure. Outer skins should remain a dry fit until that gate passes.
3. SiK was wired but no MAVLink port/serial baud, radio paired settings readback or live connection test was given. Provided current primary manual-based UART1 SERIAL1_PROTOCOL1/MAVLink1 (or2 if radio firmware supports), SERIAL1_BAUD57/57600, matching AIR/local and GROUND/PC serial rates, NetID/AirSpeed matching, Mission Planner disconnected SiK LoadSettings/CopyRequiredItemsToRemote/SaveSettings when needed, then GROUND COM connection and live aircraft attitude update. Antennas attached before radio power. No assumed range/power qualification.
4. V-tail control directions only said 'required combination'/'oppose disturbance'. Requested explicit upright-CAD observations from rear looking nose: pitch-up both trailing edges up; pitch-down both down; yaw-right both shift aircraft-right, yaw-left both aircraft-left. Stabilized nose-up calls both down, nose-down both up. Do not use the incorrect proposed left-down/right-up for yaw-right; on this upright CAD, rightward local motions are left-up/right-down (geometric inference from plane normals and official ArduPilot direction).
5. Stale authoring-process caption on motor step said corrected A26 is shown only after source supplied; remove. Previous wood-firewall instructions/atlas/printlist must become current printed ASA A26.

## Verified source basis

- https://ardupilot.org/plane/docs/common-telemetry-port-setup.html
- https://ardupilot.org/copter/docs/common-configuring-a-telemetry-radio-using-mission-planner.html
- https://ardupilot.org/copter/docs/common-sik-telemetry-radio.html
- https://ardupilot.org/plane/docs/guide-vtail-plane.html
- https://www.mateksys.com/?portfolio=f405-wing-v2

Safe baseline is instruction/manual validation, not live aircraft firmware readback. No hardware was connected in this review.

## Final status

Final file: `guide/Reaper_Beginner_Assembly_R5F.pdf`, 62 pages, SHA256 `c447e04c19fdf4245faa0bc62e60989b00cee0a18daafdf7e16ddc898199d883`.

Independent visual inspection covered every final page 33–62, plus printed-motor pages 29–30. Author inspected every page 1–32. After the final view/reference corrections, QA independently re-inspected all changed pages 20, 21, 27, 30, 31, 34, 39 and 41. Pages 54 and 56 were additionally inspected individually to establish that suspected atlas-label clipping in contact sheets was a display artefact, not a PDF defect. No unresolved layout or instructional defect was found in this scope.

The exact final PDF incorporates the five corrections above. Configuration/readback, safe servo power, actual directions and failsafe checks precede final wing/body closure. The earlier skin step is dry fitting. Servo centering provides a verified standalone 5 V tester procedure and a return gate if no tester exists. Printed ASA A26, unchanged ailerons, actual pin/net maps, SiK pair/live connection checks, removable service covers and landing gear after midsems are explicit. Structure/CG and exact-propulsion acceptance remain physical gates; old 20%-chord CG is only a starting position. Unspecified adhesive cure follows its actual product label and successful joint coupons.

Independent machine readback in `final_pdf_independent_readback.json` confirms 62 bookmarks, all assembly STEP 01–36 exactly once with embedded CAD images, 123 annotation destinations resolving to actual page xrefs, and a working Contents return on each page. PyMuPDF 1.27 labels these ReportLab /Dest annotations LINK_NAMED; QA resolved the raw /Dest page xrefs, rather than assuming only LINK_GOTO objects are internal navigation. Image presence is not substituted for the visual inspection recorded above.

Remaining limitations are physical, explicitly preserved by the guide: motor base/boss flush seating and safe M3 penetration; actual cut thickness and tab seating; usable ASA printer/material and cured ASA-to-wood bond; retained root/control hardware; loaded voltage, controller/receiver readback, propulsion heat/thrust/vibration and structural tests. No hardware/software configuration on the real aircraft or propulsion tests were performed by this audit, and this audit does not authorize flight.
