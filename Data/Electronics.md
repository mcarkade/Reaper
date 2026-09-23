# Fit, wire and check the electronics

**Keep the propeller off. Follow pin labels, not wire colours.**

## Place the parts

Onboard: one FC, battery, ESC, motor, receiver, GPS/compass, airspeed board, pitot/two hoses and air radio; four MG90S control servos. Ground: FS-i6X transmitter and SiK ground radio. The fifth servo is spare; no steering servo.

| Item | Location and access |
| --- | --- |
| Battery | Lower nose tray; nonslip pad and two straps. Lift N1 + FSU1 together. Unplug, release straps, slide to Y-205, then lift. |
| M9N GPS/compass | Shelf above forward battery; antenna face up. Paired N1 + FSU1 removal. |
| Airspeed board | Under rear edge of battery tray; insulated pad. Paired covers off, battery out; slide board to Y-25, then lift. |
| Pitot and two hoses | Left-forward tray tab; front and side openings exposed. Label/disconnect hoses and release probe before paired cover lift. |
| SiK air radio | Two strips under centre wing fairing; antenna clear of carbon. Remove FCF; reach from above. |
| F405-WING V2 | Front of aft electronics deck, behind wing; long side across body. Remove FSU2. Keep USB/SD/plugs reachable. Read arrow before setting orientation. |
| FS-iA10B | Same deck, behind FC; active antenna ends clear of carbon/power wires. Remove FSU2; leave connector bend space. |
| ReadytoSky ESC | Across strips behind receiver, ahead of FF3; cooling face exposed. Remove FSU2; provide inlet/outlet and test with cover fitted. |
| Emax motor | Behind plywood firewall; supplied screws; mounting face Y590. Check screw engagement, shaft/hub/nut fit. |
| Left aileron MG90S | Left wing cradle. Label left root disconnect; keep service loop. |
| Right aileron MG90S | Right wing cradle. Label right root disconnect; keep service loop. |
| Left V-tail MG90S | Left rear tray beside tail root. Use rear fairing openings; keep wires clear of pushrod. |
| Right V-tail MG90S | Right rear tray beside tail root. Use rear fairing openings; keep wires clear of pushrod. |

FC long side runs across the body. Read its arrow/top face and configure the actual orientation. Keep USB/SD and plugs accessible. Coordinates are secondary references in electronics.json.

## Connect every circuit

| From  ->  to | Check |
| --- | --- |
| BAT main + / -  ->  FC PDB battery input + / - | Use battery-side pads; do not bypass current sensor. |
| FC PDB ESC output + / -  ->  ESC DC input + / - | Confirm actual board pad labels and polarity. |
| ESC three phases  ->  MOTOR three phases | To reverse, disconnect battery and swap any two phases. |
| FC S1 / G  ->  ESC PWM signal / ground | ESC BEC positive stays disconnected and individually insulated. |
| FC Vx  ->  FC Vx2 | Bridge labelled pads with power removed; keep Vx at 5 V. |
| FC S3 / Vx / G  ->  AIL_L signal / + / ground | SERVO3_FUNCTION=4 |
| FC S4 / Vx / G  ->  AIL_R signal / + / ground | SERVO4_FUNCTION=4 |
| FC S5 / Vx2 / G  ->  TAIL_L signal / + / ground | SERVO5_FUNCTION=79 initially |
| FC S6 / Vx2 / G  ->  TAIL_R signal / + / ground | SERVO6_FUNCTION=80 initially |
| RX servo iBUS signal  ->  FC RX2 | Use servo iBUS, not SENS; BRD_ALT_CONFIG=0. |
| FC 5V / G  ->  RX + / ground | Verify actual connector polarity. |
| GPS TX / RX  ->  FC RX3 / TX3 | Cross TX/RX; SERIAL3_PROTOCOL=5. |
| GPS DA(SDA) / CL(SCL)  ->  FC DA2 / CL2 | Compass I2C is required in addition to GPS UART. |
| FC 5V / G  ->  GPS 5V / G | Use regulated supply, not battery voltage. |
| ASPD SDA / SCL  ->  FC DA2 / CL2 | Share bus with compass; ARSPD_TYPE=1, ARSPD_BUS=1. |
| FC 5V / G  ->  ASPD 5V / GND | ASPD order: 5V-SCL-SDA-GND; verify connector orientation. |
| FC TX1 / RX1  ->  SIK RX / TX | Cross TX/RX; match baud; SERIAL1_PROTOCOL=2 if pair supports MAVLink2. |
| FC 5V / G  ->  SIK supply + / ground | Verify radio voltage, pinout and transmit draw. |
| PITOT front opening / straight rear tube  ->  ASPD total-pressure port | Standard kit: upper sensor nipple; check actual supplied diagram. |
| PITOT side holes / angled rear tube  ->  ASPD static-pressure port | Standard kit: lower nipple; no kinks or blocked side holes. |
| COMPUTER USB  ->  FC USB-C | Data cable; USB alone does not verify battery-powered rails. |
| COMPUTER USB  ->  SIK_GROUND USB interface | Verify actual ground-radio interface. |
| TX AFHDS 2A  ->  RX RC antenna | Bind and test channels/failsafe. |
| SIK_GROUND matched radio link  ->  SIK telemetry antenna | Match supported radio settings; attach antennas. |

Use regulated 5V for electronics and separate Vx at 5 V for servos; grounds are common. Bridge Vx to Vx2 with power removed. Insulate ESC BEC positive. Manufacturer budgets are 2 A for electronics and 5 A continuous/6 A peak for servos; test actual loads.

Leave unused S2/S7-S10 functions at 0; unused 9V/12V/video pads stay empty. The battery balance plug is not an FC supply. Label wing disconnects and both hoses. Keep power wires together, away from sensors and battery travel. Measure the long battery-to-PDB route; follow the ESC maker's input-lead/capacitor guidance.

## Calibrate in order

Use **Mission Planner (Windows)**. Use a USB data cable to the FC, choose its COM port and Connect. Disconnect the Mission Planner link before Install Firmware; reconnect afterwards. Screens vary by Mission Planner release: SETUP may be INITIAL SETUP; CONFIG may be CONFIG/TUNING. Connect to the FC to reveal hardware settings.

If the new FC has no ArduPilot bootloader, follow the Matek/ArduPilot first-install procedure before Mission Planner firmware updates.

| Setup task | Mission Planner menu |
| --- | --- |
| Firmware | SETUP > Install Firmware (link disconnected) |
| Board rotation and named parameters | CONFIG > Full Parameter List; search parameter, edit, Write Params, then reboot if required |
| Accelerometer / level | SETUP > Mandatory Hardware > Accel Calibration |
| Compass | SETUP > Mandatory Hardware > Compass |
| Radio inputs | SETUP > Mandatory Hardware > Radio Calibration |
| Output functions and limits | SETUP > Mandatory Hardware > Servo Output; Full Parameter List for exact SERVOx_* values |
| Flight modes | Flight Modes under Mandatory Hardware or CONFIG, depending on release |
| Battery monitor | SETUP > Optional Hardware > Battery Monitor; Full Parameter List for exact BATT_* values |
| Airspeed | Optional Hardware > Airspeed (SETUP; older docs say CONFIG), or Full Parameter List for ARSPD_* |
| Airspeed zero | Choose PREFLIGHT CALIBRATE, then Do Action in the ground-station action controls; location varies |
| Failsafes | Mandatory Hardware > Failsafe where available; Full Parameter List for exact RC/battery action parameters |

**MANUAL:** Pilot commands control the surfaces through the configured output mixing, without attitude stabilization. **FBWA:** Flight controller stabilizes roll and pitch; sticks command bank/pitch and the pilot still controls throttle. It is not automatic navigation.

| Step | Action | Pass; otherwise fix |
| --- | --- | --- |
| 1. Inspect and power | Prop off. Check labels, soldering, polarity and no +/G short. Meter disconnected ESC lead; insulate any BEC positive. Set Vx=5 V and bridge Vx2. | **Pass:** Correct polarity and about 5 V at every low-voltage plug on battery power; no unexpected heating. **If not:** Disconnect; correct pins/short/jumper. Never parallel ESC BEC with FC 5V or Vx. |
| 2. Firmware and orientation | In Mission Planner, load supported stable ArduPlane MatekF405-Wing (V2 needs 4.4+); record version. Read fitted FC arrow/top face; set AHRS_ORIENTATION in Full Parameter List. | **Pass:** Displayed attitude follows nose-up/right-roll correctly; USB/SD remain accessible. **If not:** Fix target or board rotation first; do not compensate with servo reversal. |
| 3. Accelerometer | Mission Planner Accel Calibration: disarmed, complete all six positions, holding still at each prompt. Then use Calibrate Level in intended level flying attitude. | **Pass:** Calibration accepted; level aircraft displays level. **If not:** Repeat on firm support; check orientation. Level-only is not full calibration. |
| 4. Compass | Mission Planner Compass: calibrate outdoors away from metal/tools, with GPS/compass fixed in final orientation. Reboot if requested. | **Pass:** Accepted calibration; smooth heading changes matching known directions. **If not:** Move magnetic wiring/material; correct orientation and recalibrate. |
| 5. Radio | Plain FS-i6X airplane model; transmitter V-tail mix off. Bind iA10B and select servo iBUS/RX2. In Radio Calibration, move all sticks/switches. Assign MANUAL and FBWA in Flight Modes. | **Pass:** Inputs match sticks, reach endpoints and centre reliably; modes switch correctly. **If not:** Fix input map/reversal or iBUS port, before changing surface outputs. |
| 6. Output map and neutral | Set SERVO1_FUNCTION=70 (ESC); SERVO3_FUNCTION=4 (left aileron); SERVO4_FUNCTION=4 (right aileron); SERVO5_FUNCTION=79 (left V-tail); SERVO6_FUNCTION=80 (right V-tail). Set SERVO2_FUNCTION and SERVO7_FUNCTION through SERVO10_FUNCTION to 0. Use compatible PWM. Secure centred arms; adjust pushrods before trim. | **Pass:** Four surfaces neutral; no steering output; motor stopped at minimum/disarmed. **If not:** Correct output map/linkage/trim. Shared timer pairs must use compatible protocols. |
| 7. Direction and travel | MANUAL: right roll gives right aileron up/left down; pitch-up gives both tail trailing edges up. Right yaw, viewed from behind: left tail trailing edge up/right; right tail down/right. FBWA: tilt right gives left aileron up/right down; nose-up tilt gives both tails down. Test mixed corners. | **Pass:** Correct responses; no buzz/binding/horn movement. Initial ceilings: ailerons +/-15 degrees, total mixed V-tail +/-20 degrees, subject to real linkage. **If not:** Wrong direction: output reversal. V-tail one mixed axis wrong: exchange 79/80; both wrong: reverse output. Reduce MIN/MAX if binding. |
| 8. ESC and motor | Identify ESC protocol/manual after RC/output setup. If its PWM manual specifies high/low teaching: prop off, FC on USB, battery disconnected; select MANUAL and arm as required, set throttle high, connect battery, wait specified calibration tone, then lower throttle immediately. Wait confirmation; disconnect and restart at low throttle. DShot/CAN needs no endpoint calibration. | **Pass:** Maker acknowledgement; normal reboot gives stopped idle and smooth start. Brief restrained test confirms pusher rotation. **If not:** Stop on unknown type/tones. Follow actual ESC manual, not Copter motor wizard. Power off before phase swapping. |
| 9. GPS and telemetry | Obtain GPS fix outdoors. Connect ground SiK to computer; match baud/protocol. Check radio telemetry without FC USB. | **Pass:** Healthy fix, plausible position and continuously updating radio data. **If not:** Check TX/RX crossing, power, antennas, baud and protocol. |
| 10. Airspeed | Set ARSPD_TYPE=1 and ARSPD_BUS=1. Loosely cover pitot against wind at startup; warm at least 1 minute, then use PREFLIGHT CALIBRATE > Do Action to zero. Uncover; apply gentle airflow/pressure. | **Pass:** Healthy sensor; near-zero still air, rise with airflow, return afterwards. Small 0-3 m/s noise can be normal. **If not:** Check supply, I2C, hoses/leaks/kinks; repeat zero without wind. Do not blow hard. This does not calibrate airspeed ratio. |
| 11. Battery and rail load | Start BATT_MONITOR=4; BATT_VOLT_PIN=10; BATT_CURR_PIN=11; BATT_VOLT_MULT=11.0; BATT_AMP_PERVLT=66.7. Calibrate against meter/known safe load. Move four servos together under representative load. | **Pass:** Voltage/current agree with reference; no reset/dropout; loaded rails remain within device ratings. **If not:** Fix V2 scales/current-sensor path or resistive joints. Failed capacity needs isolated supply review, not parallel BEC. |
| 12. Failsafes and save | Set throttle cut, THR_FAILSAFE=1 and selected RC-loss/low/critical-battery actions. Prop off: switch transmitter off, wait the configured loss timer, then restore it. For a bench battery-trigger check, temporarily set the trigger above measured pack voltage; record action, then restore normal thresholds and reboot. Do not deeply discharge the pack. | **Pass:** Ground station detects each loss/trigger, applies chosen action and recovers as planned. Throttle cut stops motor. Save parameters/results. **If not:** Correct receiver loss reporting or action/timer settings. Held-last throttle fails. Confirm short/long actions separately; ground tests do not prove the airborne RTL path. |

Save the parameter file and measured results. These bench checks do not approve takeoff. Propulsion, structure, actual mass/CG and runway checks remain separate.

**Still unknown:** real connector orientations/colours; FC arrow direction; ESC BEC/protocol; radio voltage/draw; fitted cable lengths/cooling; actual pitot port diagram; motor/prop current, thrust and temperature; site-specific failsafe actions and thresholds.

Sources: [Matek V2](https://www.mateksys.com/?portfolio=f405-wing-v2) ; [ASPD-4525](https://www.mateksys.com/?portfolio=aspd-4525) ; [M9N-5883](https://www.mateksys.com/?portfolio=m9n-5883) ; [Accelerometer](https://ardupilot.org/plane/docs/common-accelerometer-calibration.html) ; [Compass](https://ardupilot.org/plane/docs/common-compass-calibration-in-mission-planner.html) ; [Radio](https://ardupilot.org/plane/docs/common-radio-control-calibration.html) ; [V-tail](https://ardupilot.org/plane/docs/guide-vtail-plane.html) ; [ESC](https://ardupilot.org/plane/docs/common-esc-calibration.html) ; [Pitot](https://ardupilot.org/plane/docs/airspeed.html) ; [Airspeed zero](https://ardupilot.org/plane/docs/calibrating-an-airspeed-sensor.html) ; [Failsafes](https://ardupilot.org/plane/docs/apms-failsafe-function.html) ; [SiK](https://ardupilot.org/plane/docs/common-sik-telemetry-radio.html).

Menu and mode references: [Mission Planner setup menus](https://ardupilot.org/planner/docs/mission-planner-initial-setup.html); [Mission Planner parameter menus](https://ardupilot.org/planner/docs/mission-planner-configuration-and-tuning.html); [Battery monitor screen](https://ardupilot.org/plane/docs/common-power-module-configuration-in-mission-planner.html); [Airspeed setup](https://ardupilot.org/plane/docs/airspeed-parameters-setup.html); [MANUAL mode](https://ardupilot.org/plane/docs/manual-mode.html); [FBWA mode](https://ardupilot.org/plane/docs/fbwa-mode.html).
