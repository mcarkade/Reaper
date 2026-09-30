# R5F mechanical changes and physical gates

The local electronics evidence and manufacturer ECOII-2807 drawing identify EMAX ECO II2807 1300KV, four M3 threads on a19mm pitch circle. R5B/R5C changed this to a literal19mm square; that was wrong. R5F keeps the original motor axis and6mm thickness, prints A26 in ASA and uses the actual drawing pattern. The source A26 flank slots were5mm high while A43 is nominal6mm: the replacement locally makes those two slots6mm. Its keel slot remains nominal6mm. Actual sheet thickness and kerf still need measuring, so no physical fit is claimed.

Current A62_A protrudes13.015mm beyond the motor mounting face. That volume overlaps the manufacturer's Ø33.9mm motor envelope by823.136mm³. Trim only this projection flush to A26's aft face (worldY582.650mm); forward wood and firewall joint remain. The earlier integration trim script recorded the same plane; current correction was independently calculated from released source geometry. Retain already cut stock and use CAD/Secondary_Removal/A62_A_AFT_TRIM.step to locate the removal. Do not cut the whole frame again.

A44_L/R replace two plywood ribs with unchanged6mm installed shapes. PLA+,4wall loops and100%rectilinear fill are a conservative solid-rib starting point, not a verified strength rating. Lay the broad face flat to keep rod-seat/spar loads in the layer plane. The actual wing needs fit, adhesive-coupon and proof-load tests before use. Sand only marked glue surfaces, remove dust, use an epoxy rated for PLA/wood and cure for its full label time while the wing is held square. Do not assume wood glue adheres to plastic.

Before motor installation, provide actual wood thickness at the receiving joints, a photo of where A26 catches if it still does, and safe M3 engagement depth measured on the actual motor. Paper-check the exact hole pattern and confirm its label. Four screws must clamp fully with washers without touching windings. Existing square holes are not to be enlarged into the new pattern: replace the small A26 plate. Propulsion combination4S/9045 three-blade/40A ESC still requires measured thrust/current/temperature testing; manufacturer drawing recommends6–7inch propellers and does not qualify this combination.


A26 is printedASA per Data/A26_Printed_Motor_Design.md; historical wood A26 is superseded. No standalone laser-cut motor mount is released.
