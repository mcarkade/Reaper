# Motor mounting and foam mass evidence

Checked 19 September 2026.

## Motor

Primary product: https://shop.emaxmodel.com/products/emax-eco-ii-series-2807-1300kv-1700kv-1500kv-brushless-motor-for-rc-drone-fpv-racing

Official manufacturer drawing linked by that page, downloaded and visually inspected:
https://cdn.shopify.com/s/files/1/0469/7358/3518/files/ECOII-2807Motor_specifications_200926_-01.jpg?v=1602844068

Local evidence: emax-drawing.jpg in this directory.

Drawing labels four M3 threads on diameter 19 mm pitch circle. Four holes are equally spaced at 90 degrees; drawing has them diagonal to cable direction. Thus adjacent square pitch is 19/sqrt(2) = 13.435 mm, with x/z coordinates (+/-6.718, +/-6.718) about shaft. A rotated pattern has coordinates (+/-9.5,0) and (0,+/-9.5). The manufacturer marketing wording says 19x19 mm, which conflicts with a literal interpretation of the drawing. Do not make a literal 19 mm square: compare a paper template against the physical motor before drilling. Thread engagement depth is not dimensioned; measure and select screw length to avoid winding contact.

Drawing additionally gives diameter33.9 mm, overall34 mm, M5 prop thread, and KV1300 mass47.6 g excluding silicone wire. Manufacturer recommends6-7inch propellers,3-6S. This does not qualify the user9inch prop at4S or validate40A ESC margin.

The requested reseller PDF could be indexed/opened by web but its direct download failed; the official image above provides clearer primary evidence.

## Foam

Primary vendor page: https://www.vortex-rc.com/product/fliteboard-pro1000x600mm-20-sheet-pack/

Vendor specification: 1000x600mm,5mm polystyrene XPS core laminated with paper,400g/m2 nominal areal mass. Derived whole-sheet nominal mass=1.0x0.6x400=240g; ten sheets=2400g before cutting. Use retained cut area times400g/m2 for nominal structure mass and then add glue, reinforcement and finish. This is product-specification-based planning, not measured batch mass. If material is not this exact FliteBoard Pro product, do not transfer the number. Weigh one user's full sheet to resolve batch/material difference.
