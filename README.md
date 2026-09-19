# MQ9 RC build

Shared files for the 2-metre airframe and electronics teams. **Revision 1 is a prototype fabrication handoff, not a flight release.**

## Start here

| Team / task | Open |
|---|---|
| Everyone | [Complete illustrated build guide](Build%20Guide/Complete_Build_Guide.pdf) |
| Fabrication and assembly | [Airframe guide](Build%20Guide/01_Airframe_Manufacturing_and_Assembly.pdf) |
| Electronics | [Wiring, placement and calibration guide](Build%20Guide/Electronics_Build_Guide.pdf) |
| Send to the workshop | [Revision 1 manufacturing ZIP](https://github.com/mcarkade/Reaper/releases/download/rev1/MQ9_Manufacturing_Rev1.zip) |
| Print cutting patterns | [Actual-size A4 templates](Manufacturing/Print_Templates) |
| Quantities / purchases | [Parts and materials list](Manufacturing/Complete_Parts_and_Materials.csv) |
| Record the physical build | [Build record](Build%20Guide/Build_Record.csv) |

The consolidated manual contains instructions and overviews. Cutting templates are separate. Print those at **Actual Size / 100%** and measure the calibration marks.

The paper set uses **7 plywood pages, 23 foam pages and 2 optional tail-tooling pages**. Parts that fit one usable A4 sheet stay whole; larger parts share tiled pages and spare space.

## What is included

- 22 plywood profiles for 31 pieces, native millimetre DXFs and sheet layouts.
- 33 developed foam patterns for 35 blanks, forming instructions and labelled assembly maps.
- 11 aircraft print meshes, a separate fit coupon and matching STEP geometry.
- Revised assembly, tube schedule, hardware references, parts lists and numerical verification.
- F405-WING V2 wiring, component placement, radio setup, calibration and bench checks.

Use this release as a set. Older AI packages, rejected trials, caches and installed tools are not published here. Start inside `Manufacturing` with `READ_ME_FIRST.txt` if using the unpacked files.

## Checked digitally; still to test physically

Profiles, quantities, selected mesh topology, source comparisons, foam development and PDF scale/registration have recorded checks. See the [verification summary](Build%20Guide/Reference/Verification_Summary.pdf).

The builders still need to qualify stock and printer fits, foam forming, assembled clearances, joints and landing gear, then record actual mass and balance. The 522 mm aft-nose mark is a provisional geometric reference. The owned 9-inch propeller / 40 A ESC combination remains unqualified. Follow the guides before powered or flight testing.

Record measurements and test results in the build record. When hardware or geometry changes, update the affected drawings, parts list and guide together; replace the workshop ZIP only after rechecking the changed files.

## Original model

Based on the supplied [build video](https://www.youtube.com/watch?v=X-Q08HQq7fM) and [Onshape model](https://cad.onshape.com/documents/da0c1a9f98b6358f736153b1/w/040544fbf77b8cf6608e2eb9/e/28c526eeb45b3f50fa69269f). Original STEP sources and the supplied transcript are retained for traceability. This repository documents the build revisions; it does not claim authorship of the original model or grant a new licence for it.
