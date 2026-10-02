# Reaper R5G wood assembly

The current full requested recut set contains 37 nominal 6 mm plywood pieces, including A26 and reinforced A44_L/R. Use the single combined R5G DXF, part map and complete beginner guide. Physical stock thickness/kerf, receiver batch, actual motor mounting and assembly fit remain unverified.

The DXF describes laser stock, while CAD/Parts contains the finished assembly geometry. Shallow rebates and sacrificial allowances require the exact illustrated secondary operation. Do not through-cut their bounding boxes or thin an entire part. Grain is carried through each flattening/nesting transform: all current panel grain vectors are parallel to stock X; A18 is intentionally rotated 90 degrees.

Current fit corrections:

- A18: the user confirmed 0.5 mm total clearance, implemented as a 0.25 mm normal inset of opposed upper A12 receiver-facing perimeter edges. Its inner opening, bottom keel interface and 6 mm thickness are unchanged. Delivered adapted A12 has a 6.30 mm axial slot; the raw original source has a 2.5 mm slot and cannot accept 6 mm stock. Verify the actual print batch and insertion order before bonding. Installed CAD noninterference does not prove insertion; straight translation probes are blocked, so the actual tilt/order fit remains a required check.
- A01_L/R: extremely thin source toe/shelf extensions are removed along the retained spar contact planes; the 5 mm rear-rod hole, its axis and broad spar contacts remain. Fixture the original rear-spar height and foil alignment during bonding because the removed shelf previously acted as a register.
- A62_A: laser length is 482.650 mm, with the prior 13.015 mm aft trim incorporated. A18's nominal 6 mm notch, Z-31 floor and 30 mm² nominal seat remain. A62_F source length is 529.070452 mm and its local A54 seat still needs the source side relief.
- A44_L/R: retain the reinforced front-rod seat and servo-bay roof. The entire original trailing taper and A53 bond footprint are restored. A 3 mm minimum vertical web protects that thin tail during laser cutting. Pare only the sacrificial underside allowance to the supplied finished profile before bonding A53 or closing the skin; do not shorten the trailing tip. Manual actual servo/retainer hole placement and local foam relief remain required. Exact removal STEP and non-laser paring templates are supplied.
- A26: plywood plate with zero motor screw holes; [motor fit notes](A26_Motor_Mount.md) govern actual rear-frame dry-fit, real-motor marking, hardware engagement and loaded qualification.


## Assembly order and retained datums

1. Join A62_F and A62_A at world Y100 mm on a straight flat jig. A62_DL and A62_DR bond on opposite faces from Y40 to Y160 mm. Align their lower edges with the keel at Z-41.7139 mm. Each lap bonds to the full 7.5 mm-high keel band for 60 mm on each half, about 450 square mm per half per face. The butt ends locate the halves; the side laps transfer load. Cure to the actual adhesive instructions before loading.
2. Dry-fit A13/A43 horizontal frames, body formers and keel with frame upper face Z0. Complete local relief before bonding; do not thin the whole frame or former. Install the original gear crossmembers/crossplate, but defer actual landing-gear hardware until after midsems. Their presence does not prove purchased-gear attachment, steering clearance or load spreading.
3. A18 occupies Y454.5 to Y460.5 mm. Prove the actual adapted A12 receiver insertion/order and service access before glue. A26 occupies Y576.65 to Y582.65 mm, motor axis X0/Z-2.5 mm. R5G A26 has zero motor screw holes. Dry-fit the actual rear frame/keel/receiver first, then hand-mark the real motor. A62_A ends flush at Y582.65; do not repeat the previous 13.015 mm trim. Check driver, heads, washers, wiring, seating and safe thread depth using actual hardware rather than nominal CAD cylinders.
4. Join rear wing spar halves at X+360 mm on the right, mirrored on the left. Two 100 mm face laps span X310 to X410 mm, giving 50 mm overlap per half and about 300 square mm contact per face per half. Keep the spar straight in a jig through full adhesive cure.
5. Assemble each wing's front spar, joined rear spar, A01 rear-rod support and inner/middle/outer ribs. Fixture A01's original rear-spar height because its fragile shelf is removed. Both whole 5 x 1000 mm rods cross the fuselage: front axis Y60.4543/Z15.6325 mm and rear Y100.5004/Z15.0705 mm, each spanning X-500 to X500. Do not cut or butt-join them. Current A44 has a closed front-rod seat with a 3 mm ligament; plan axial rod insertion before bonding/skin closure.
6. Pare only A44's sacrificial underside tail allowance to the supplied full finished taper before bonding A53. Preserve the whole tip and reinforced servo-bay roof, mark actual servo/retainer holes after fitting, and qualify the local foam relief. No claim of loaded capacity follows from the geometric contact area.
7. Fit wooden aileron endplates to the unchanged revised printed controls and fixed rails. A53's inboard datum remains about X493 mm, with its 6 mm thickness extending outboard; the control was previously shortened to suit. Outer plates extend away from the moving controls. The 2 mm holes are pilots: align/ream to the real short bicycle-spoke pivots on the common hinge line and provide positive pivot retention. A friction fit alone is insufficient.
8. Dry-fit the source foam around the finished frame, preserving outer paper and making only documented internal relief. Inspect joints, installed controls, wire routing and service access before closure. Weigh the completed structure before physical balance/performance acceptance.

## Fixed body stations

| Member | World assembly datum, mm |
|---|---|
| A13 front horizontal frame | Upper face Z0; original front end near Y-435.01 |
| A34 front former | Forward face Y-130 |
| A54 body former | Forward face Y-5 |
| A25 gear crossmember | Forward face Y125 |
| A48 gear crossmember | Forward face Y142.7 |
| A16 body former | Forward face Y233.65 |
| A04 rear body former | Forward face Y384.65 |
| A18 tail carrier bulkhead | Aft face Y460.5 |
| A26 plywood motor firewall | Aft face Y582.65 |

## Local fitting: stock versus finished shape

Secondary_Dimensions.json and CAD/Secondary_Removal show actual removal regions. A depth interval spanning 0 to 6 mm does not mean remove an entire rectangular bounding box: the region can combine a through-notch edge with an adjacent shallow rebate. Removal solids are finishing tools, not extra aircraft pieces.

- A43: local seats at Y125 to131, Y142.7 to148.7, Y233.65 to239.65 and Y384.65 to390.65 mm. At the first two remove 1 mm locally from the underside, retaining 5 mm. Body-former seats retain about 5 mm at representative patches; one original curved rear patch samples 4.83 mm. Stop at the illustrated mating shape, preserving surrounding full thickness. Do not force a curved source patch into an invented uniform 5 mm plane.
- A05_R/L: root and middle-rib notch/tab relief at X53 to59 and X247.35 to253.35 mm, mirrored on the left. The removal combines edge and face fitting. Do not apply one blanket sanding depth; use the mating rib and finished geometry as the stop.
- A07_R_I/L_I: corresponding root/middle-rib stations; representative tabs retain 5 mm locally while the rest stays 6 mm.
- A62_F: A54 seat at Y-5 toY1 mm. Local side relief retains 5 mm (nominally 0.5 mm per side); retain the surrounding keel band and match the actual former. A62_A's aft cut is already incorporated into its current stock profile.
- A53_R/L and A07_R_O/L_O: source edge wedges around 0.03 mm and 0.015 mm respectively. Dress only if the actual dry-fit needs it; preserve the source outline and pivot-support material.
- A44_L/R: use the exact underside-tail removal and the non-laser 1:1 paring templates. The source A53 bond footprint is restored at about 30.614 square mm per side. Actual bond quality and structural proof loading remain required.

These are geometric attachment datums, not plywood/adhesive/fatigue allowables. Actual joints, wing/frame, hardware, propulsion, balance and operation require the guide's physical gates.
