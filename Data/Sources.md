# Sources and limits

Checked 23 September 2026. Primary hardware references support dimensions and wiring; they do not prove this installed aircraft's performance.

Original exterior/design references: [original build video](https://www.youtube.com/watch?v=X-Q08HQq7fM) and [original Onshape design](https://cad.onshape.com/documents/da0c1a9f98b6358f736153b1/w/040544fbf77b8cf6608e2eb9/e/28c526eeb45b3f50fa69269f). Original design rights remain with its creator. This package adapts that supplied geometry for the prototype described here; these links preserve the prior project's design credit.

# Source and verification record

Checked 23 September 2026 against primary manufacturer/ArduPilot pages. Existing electronics guide and the owner-reported `EXACT_INVENTORY.md` supplied the part list; current owner decisions supersede its older plywood and steering notes. No device was connected during this document pass.

- [Matek F405-WING V2](https://www.mateksys.com/?portfolio=f405-wing-v2): V2 power ratings, Vx/Vx2 bridge, RX2 iBUS and `BRD_ALT_CONFIG=0`, S1–S10, UART/I2C mapping, V2 battery monitor values. The [ArduPilot F405-Wing page](https://ardupilot.org/plane/docs/common-matekf405-wing.html) contains older V1 physical/current details; use the V2 manufacturer page where they differ.
- [ArduPilot servo functions](https://ardupilot.org/plane/docs/servo-functions.html): 4 aileron, 70 throttle and individual `SERVOn_FUNCTION` configuration. [V-tail guide](https://ardupilot.org/plane/docs/guide-vtail-plane.html): 79/80 assignments, reversal and physical direction tests, combined pitch/yaw throw, transmitter mix disabled.
- [Matek M9N-5883](https://www.mateksys.com/?portfolio=m9n-5883): 4–5.5V GPS UART plus compass I2C, nominal 50mA, 38400 default, magnetic separation. [Matek ASPD-4525](https://www.mateksys.com/?portfolio=aspd-4525): 4–5.5V, I2C and JST-GH 5V/SCL/SDA/GND sequence.
- [ArduPilot serial port setup](https://ardupilot.org/plane/docs/common-telemetry-port-setup.html) and [SiK radio](https://ardupilot.org/plane/docs/common-sik-telemetry-radio.html): MAVLink serial setup, crossed UART and link checks. The actual owned radio's label, draw and cable mapping remain unverified.
- [ArduPilot airspeed setup](https://ardupilot.org/plane/docs/airspeed.html) and [parameters](https://ardupilot.org/plane/docs/airspeed-parameters-setup.html): MS4525 sensor setup and the limit of bench response. [Plane failsafe](https://ardupilot.org/plane/docs/apms-failsafe-function.html): RC and battery failsafe detection, configuration and bench checks.
- [Emax ECO II 2807 product](https://emaxmodel.com/products/emax-eco-ii-series-2807-1300kv-1700kv-1500kv-brushless-motor-for-rc-drone-fpv-racing): motor family and voltage scope. No manufacturer result was found proving the owned Gemfan 9045 three-blade/4S/40A ESC combination; current, thrust and temperature remain physical tests.

**Pending physical evidence:** photographed installed component labels and adapter pinout; ESC BEC meter result; FC 5V and Vx loaded readings; measured wire lengths; configured parameter export; control and failsafe bench video/log; pitot and compass health; current/thrust/thermal data; completed-airframe mass and CG. None is inferred from the documentation.

## Current placement evidence

- Matek F405-WING V2 manufacturer search result gives 54 x 36 x 13 mm; direct page access was blocked/redirected in this pass. The older 56 mm board dimensions are not used.
- [FlySky FS-iA10B](https://www.flysky-cn.com/ia10b-canshu) directly confirms 47 x 33.1 x 14.7 mm and 19.3 g, with two 150 mm antennas.
- [Matek M9N-5883](https://www.mateksys.com/?portfolio=m9n-5883) manufacturer search result confirms 32 x 32 x 10 mm; local manufacturer STEP is also available.
- [Matek ASPD-4525](https://www.mateksys.com/?portfolio=aspd-4525) directly confirms 3.5 g board mass, 4-5.5 V, 5 mA and 5V/SCL/SDA/GND connector sequence. Its 20 x 20 mm PCB was recorded in the earlier primary drawing review; 12 mm height is a conservative fit allowance, not a remeasured drawing dimension.
- `placement_probe.json` records mechanical register hash and exact box/clearance tests. These do not prove actual connector insertion or cooling. ESC and SiK dimensions remain provisional envelopes, not verified product measurements.


## Structure, stock and calculations

- [FliteBoard supplier description](https://www.vortex-rc.com/2016/10/20/fliteboard-lightweight-paper-laminated-foamboard-rc-planes-india/): paper-faced XPS, nominal-thickness discrepancy, paper strength contribution and adhesive compatibility. Measure the owned board; inner-face removal and shaping need a same-stock trial.
- [EMAX ECO II 2807](https://shop.emaxmodel.com/products/emax-eco-ii-series-2807-1300kv-1700kv-1500kv-brushless-motor-for-rc-drone-fpv-racing): motor family. Use the dimensional drawing's four holes on a19mm pitch circle, not a19mm square interpretation of listing text; actual motor fit remains a bench check.
- [EMAX-branded specification sheet, reseller mirror](https://pdf.direnc.net/upload/emax-eco-ii-2807-kv-fircasiz-drone-motoru.pdf):34mm total motor height includes14mm of shaft;1300KV nominal mass47.6g excluding silicone wires, and listed propeller range6-7in. The owned9in three-blade is outside that published range and requires measured qualification or a prop/setup change.
- [Gemfan9045-3](https://www.gemfanhobby.com/gemfan-9045-3-glass-fiber-nylon.html):9in diameter,4.5in pitch, three blades and M5 hub. The page's material variant differs from the owned carbon-nylon listing; weigh and inspect the actual prop. No located source tests the complete owned2807/1300KV/9045-three-blade/4S combination.
- [APC propeller technical advisories](https://www.apcprop.com/technical-information/technical-support-advisories/): manufacturer explanation of front-facing propeller orientation in pusher installations and matching blade leading edges to rotation. This is general orientation evidence, not a Gemfan-specific adapter or motor approval.
- [TowerPro MG90S](https://towerpro.com.tw/product/mg90s-3/): nominal servo envelope, mass and stall-torque specification. Stall torque is not a continuous operating target.
- [NASA lift equation](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/lift-equation/) and [induced drag](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/induced-drag-coefficient/): equations used for sensitivity scenarios. Maximum lift coefficient, drag, efficiency and actual material properties remain assumptions.
- [RC CAD wing structure](https://www.rccad2vr.com/rc-airplane-design-build-episodes/design-rc-airplane-wings-in-fusion-360-part3) and [Model Aviation carbon/balsa build](https://www.theparkpilot.org/match-stick-bailiff): construction examples for spar load paths and bonded reinforcement, not strength allowables for these parts.
- [DIY tied landing gear](https://www.flitetest.com/articles/alternative-landing-gear-fastening): builder uses ties around structural anchors on700–1000g wire-gear models. This supports the simple attachment method, not its strength or breakaway load on this aircraft. [Prusa PLA guidance](https://help.prusa3d.com/article/pla_2062) describes generic PLA impact/layer-fracture limitations; the owned PLA+ formulation has no landing-leg qualification here. Plywood is selected for simple stock use and replacement, not because harmless crash failure is guaranteed.

## DIY YouTube pass

Titles, channel information and descriptions/creator pages were checked. Playback and transcripts were not inspected, so there are no timestamp or footage-verification claims. These are practical references for the team to watch, not flight evidence for this design.

- [Julius Perdana: DIY MQ-9 Reaper2500mm](https://youtu.be/71IDoeHT1b4), with [creator build page](https://paper-replika.com/index.php/rc-foam-project/mq-9-reaper-2500mm-rc-plane?showall=1): closest form-factor example; different wing, tail, propulsion and mass. Its enlarged flying surfaces and front-set battery demonstrate why scale appearance alone cannot set flying dimensions or CG.
- [Julius Perdana: Reaper camera view](https://youtu.be/nE7LXNPCt2k): creator description reports two flights; footage was not independently reviewed here.
- [Marko Roolaid: Simple Lady wing construction](https://youtu.be/XWMOVTCkCvM) and [full build/maiden](https://youtu.be/goCgRIHl9Bc):2m balsa/carbon workmanship and assembly references. This is an unpowered high-start glider, so launch and performance do not transfer.
- [Experimental Airlines: Armin wing](https://youtu.be/karr67ZYho4): formed flat-bottom paper-faced foam wing construction. Board, section and dimensions differ; do not copy score dimensions or strength assumptions.
- [RCsean: twin-boom pusher build](https://youtu.be/fp0q7K6TTrk), with [creator build page](https://www.rcsean.com/p/albatros-fpv.html): accessible wing wiring, structural mounting points and prop protection. Its rubber-band retention and propulsion are different.
