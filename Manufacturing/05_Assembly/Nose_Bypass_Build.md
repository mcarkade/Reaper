# Nose gear spine bypass - manufacturing revision

The 3 mm vertical nosewire crosses the full 7.5 mm local height of the 5 mm centre spine. A notch alone would interrupt the spine. This revision deliberately replaces that local centre load path with two continuous side doublers, positively joined with four transverse M2 fasteners. The gear axis remains X=0, Y=-293.65 mm. The original external aircraft envelope is unchanged.

## Parts

- A62: use the two shapes in `A62_spine_bypass.step`, both cut from 5 mm aircraft plywood. The 3.4 mm gap runs Y=-295.35 to -291.95 mm and clears the 3 mm shaft by nominal 0.2 mm each fore/aft side. It is not an accidental broken part.
- A63/A64: two identical 2.5 mm aircraft-plywood doublers, each 72 x 10.7 mm. Installed ranges: Y=-329..-257, Z=-41.414..-30.714; left X=-5..-2.5, right X=2.5..5. Orient face grain along the 72 mm length. Do not substitute soft balsa.
- A37: revised printed mount has matching side-doubler pockets with nominal 0.15 mm fit clearance and the same four transverse hole axes. The main connected solid is retained; two disconnected thin pocket-floor slivers of approximately 3.7 mm3 each are omitted. A vertical diameter 3.2 mm pivot passage is provided at the original gear axis. All original exterior mount surfaces outside the recesses and holes are preserved.
- Four M2 machine screws with washers on both sides and locking nuts. The two stations inside A37 (Y=-302,-282) need approximately M2x40 to M2x45 screws; choose length from the actual printed width and washer/nut stack, leaving 1-2 threads past the locknut. Outer stations Y=-320,-264 need approximately M2x16. Do not use self-tapping screws into ply end grain.

All holes are diameter 2.2 mm on X-directed axes at Z=-37.964 and Y=-320,-302,-282,-264 mm. The two inner screws pass through the printed mount, both doublers and centre-spine pieces. The two outer screws join both doublers to the centre pieces. This provides two fasteners to each side of the interrupted centre spine.

## Assembly

Dry-stack the centre pieces and both continuous doublers on a flat alignment fixture. Install all four screws loosely, then insert the actual 3 mm nosewire through the axis and rotate it fully before bonding. Check that both spine pieces remain collinear and that the 3.4 mm gap is centred on the shaft. Bond the wood interfaces with a suitable wood adhesive while using the bolts as positive retention; keep adhesive out of the shaft passage. Tighten locknuts only enough to seat the stack without crushing printed plastic or plywood. Recheck free rotation after cure. Keep the joint accessible for inspection.

The source steel rod ends below A09. The root fabrication revision must extend the straight upper shaft through the steering bearing and steering-arm clamp; preserve the lower wheel geometry and gear axis. This bypass has at least 1 mm lateral clearance to the original shaft, so extending it vertically does not require a taller centre bridge. Match the final rod engagement to the actual bearing/steering hardware rather than retaining the source's disconnected upper end.

## Checked geometry and limits

Each doubler is one valid connected solid, the revised mount is one valid connected solid, and the centre spine is deliberately two valid solids before assembly. The doublers do not intersect A09, A37, A46, A56 or A59; minimum nominal clearances are about 1.0 mm to the steel shaft and 0.16 mm to the foam inner surface. Near-zero interface slivers below 0.01 mm3 arise from STEP coordinate tolerances at nominally shared wood faces; do not enlarge the design to chase these values. A62's existing foam contact is a separate pre-existing fit issue.

This is a concrete manufacturable joint geometry, not a demonstrated landing-load rating. Inspect the printed mount, bolt bearing, plywood quality, adhesive bond and full assembled gear motion on the ground before flight. No load-test result is claimed.
