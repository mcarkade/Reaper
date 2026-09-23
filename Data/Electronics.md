# Electronics and four-surface controls

Use four MG90S servos: two ailerons and two V-tail surfaces. The fifth servo is a spare. The fixed nose wheel has no servo. Keep the propeller removed during wiring, setup, control-direction and failsafe tests.

## Power

Connect the GenX 4S pack through the F405-WING V2 battery/PDB input and current sensor to the ESC feed. Verify the real connector polarity and wire ratings. The FC's 9–30 V input and 100 A continuous current-sensor rating do not qualify the 40 A ESC or the motor/9045 three-blade combination. Their current, thrust and temperature on 4S remain unmeasured.

Use the regulated 5 V rail for the receiver, GPS/compass, airspeed sensor and air radio only after their voltage and combined current are checked against the FC's 2 A rating. Keep the separate Vx servo rail at its default 5 V for the MG90S, pending label checks and a simultaneous four-servo loaded test. Matek rates Vx at 5 A continuous/6 A peak. Bridge Vx to Vx2 when using this internal servo supply; otherwise S5–S9 have no servo positive supply. Confirm voltage and polarity at every servo plug under load. Never put 4S battery voltage on a 5 V or Vx device.

The ReadytoSky ESC listing conflicts between “Opto” and “5 V/3 A BEC”. With the ESC disconnected from the FC, meter its actual signal-lead wires to determine whether the positive is powered. For this plan, connect only signal and common ground to S1/G; insulate any ESC BEC positive separately. Do not parallel the ESC BEC with FC 5 V, Vx or Vx2. A failed servo-rail load test requires a deliberately isolated supply redesign, not another parallel feed.

## Connections

Use `connections.csv` as the harness record. Its wire-length cells stay blank until the harness is routed on the finished structure. Verify connector pin order with a meter; matching plug shapes do not establish pin compatibility.

| FC connection | Device and initial setup |
| --- | --- |
| S1, G | ESC signal and ground; `SERVO1_FUNCTION=70` |
| S2 | Unused; `SERVO2_FUNCTION=0` |
| S3, Vx, G | Left aileron; `SERVO3_FUNCTION=4` |
| S4, Vx, G | Right aileron; `SERVO4_FUNCTION=4` |
| S5, Vx2, G | Left V-tail; initial `SERVO5_FUNCTION=79` |
| S6, Vx2, G | Right V-tail; initial `SERVO6_FUNCTION=80` |
| S7–S10 | Unused; functions 0, no steering servo |
| RX2, 5V, G | FS-iA10B servo iBUS output, not SENS; `BRD_ALT_CONFIG=0` |
| TX3/RX3, 5V, G | M9N GPS UART: TX connects to the other device's RX; `SERIAL3_PROTOCOL=5` |
| DA2/CL2, 5V, G | M9N compass and ASPD-4525 shared I2C; `ARSPD_TYPE=1`, `ARSPD_BUS=1` initially |
| TX1/RX1, 5V, G | SiK air radio crossed UART; `SERIAL1_PROTOCOL=2` if the actual pair supports MAVLink2 |

M9N needs both UART for GPS and I2C for its compass. Its documented supply is 4–5.5 V. The ASPD connector sequence is 5V, SCL, SDA, GND; confirm orientation on the actual harness. Check that both I2C devices are detected. The actual SiK variant, supply draw and cable mapping remain unverified; do not substitute the seller's conflicting radio-power labels for a reading from the real unit.

## Physical placement and service

FEQ is a 68 x 90 mm deck in the aft service bay, at Y248 to 338. The FC centre is (0,270,13.5), receiver (0,315,14.35), with 2 mm mounting allowances. Their verified bare dimensions are 54 x36 x 13 mm and 47 x 33.1 x 14.7 mm. The bodies have a 10.45 mm fore-aft gap. The FC's long side runs across the body; check its arrow and configure board orientation accordingly. Remove FSU2 for plug and USB/SD service. Actual connector bend radii still need a dry fit.

GPS centre remains (0,-300,59) on FGPS. The airspeed board is under the aft end of FBT at (16,-60,-20), reached from the open tray rear edge after removing the battery. Attach it with an insulating pad and ties/tape as appropriate; keep its ports and connectors accessible. Its 12 mm height is a fit allowance, not a measured sensor package. Check actual pressure-tube lengths and bends before closing the lower skin.

The ESC allowance is turned across the body at (0,365,15), 65 x 32 x 16 mm, supported by two simple strips FES0/FES1 and pads/ties. This keeps its body entirely ahead of rear former FF3 and permits upward removal through FSU2. Route its wires below the curved cover; real plug and wire bends remain a trial-fit item. Provide an inlet and outlet around the real ESC during fitting, then test temperature with the actual covers in place. The model does not certify cooling.

The provisional SiK position is (0,180,16), 28 x 60 x 18 mm, tied on top of FTM0/FTM1 with a 2 mm insulating allowance. Its board dimensions, antenna and current demand still need confirmation. FCF must remain removable to service it. These ESC and radio sizes are provisional equipment envelopes, not verified product dimensions.

Keep the battery positive and negative together. Route their service loop along the body clear of the pack's full travel and the compass. The nominal pack-to-PDB run is over 400 mm before bends; measure it and follow the actual ESC maker's input-lead/capacitor guidance before extending the DC wiring. The FC-to-ESC section is now about 95 mm before routing. Do not assume that a shorter final section qualifies the whole supply path.

Label left/right wing-root connectors and provide strain relief plus enough service loop to remove each wing. Keep tail leads clear of pushrods. Support the receiver's active antenna ends away from carbon and high-current wiring; support the radio antenna independently. Wiring must not obstruct the battery's slide to Y-205 and vertical removal.

## Propeller-off setup

1. Inspect labels, soldering and polarity. Check for shorts. Confirm the actual V2 board and the supported MatekF405-Wing ArduPlane firmware; record the installed version. The established V2 baseline is ArduPlane 4.4 or newer. USB alone does not verify all battery-powered rails.
2. Apply the output map, ordinary PWM settings and documented board orientation. S1/S2, S3/S4 and S5/S6 share timer groups; do not mix incompatible DShot/PWM settings within a group.
3. Use a plain FS-i6X airplane model with transmitter V-tail mixing disabled. Bind the iA10B, select servo iBUS and verify all radio channels in calibration.
4. Centre servo arms and fit the four retained spoke pushrods. In MANUAL: right roll gives right aileron up/left down; pitch-up gives both tail trailing edges up; right yaw moves both V-tail surfaces right. If only one V-tail axis is wrong, review 79/80 assignment; if both axes are wrong, review that output's reversal. Physical response determines the final settings.
5. In FBWA with centred sticks, right roll of the aircraft must command left aileron up/right down; nose-up tilt must command both tail surfaces down. Check the documented V-tail yaw response. Test combined pitch/yaw corners, aileron limits, neutral return, binding and four-servo rail voltage. Save the final parameters; no throw is flight-approved by this document.
6. Start V2 battery monitoring with `BATT_MONITOR=4`, `BATT_VOLT_PIN=10`, `BATT_CURR_PIN=11`, `BATT_VOLT_MULT=11.0`, `BATT_AMP_PERVLT=66.7`. Calibrate against a meter and known load. Do not use the older board's 31.7 current scale.
7. Check GPS fix, compass orientation, telemetry and airspeed detection. Apply only gentle pitot pressure, inspect tube routing, and confirm a near-zero still-air response. This is not an airspeed-ratio or stall-speed calibration. Resolve unreliable readings before airspeed-dependent modes.
8. Enable and configure RC-loss and battery failsafes for the actual operating area. Verify transmitter-loss detection, mode change and recovery with the propeller off. Test the selected battery actions and throttle cut. Healthy GPS/home and a suitable path are prerequisites for RTL, not a guarantee of safe recovery.

Before powered taxi or flight, record installed mass/CG, actual motor current/thrust/temperature, loaded rail readings, control checks and real prop/gear clearance. Neither a wiring document nor a fitted landing gear proves takeoff readiness.
