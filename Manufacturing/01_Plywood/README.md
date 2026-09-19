# Plywood

22 profiles produce 31 pieces. Follow the [cutting register](manufacturing_register.csv) for quantities.

| Stock | Pieces |
|---|---:|
| Nominal 5 mm plywood | 24 |
| 3 mm plywood | 4 |
| 2.5 mm plywood | 3 |

Two A44 ribs have a finished CAD thickness of 4.990 mm and use nominal 5 mm stock. Measure stock and check fit before production.

- [Individual DXFs](Individual_DXF) are grouped by finished thickness. Cut the register quantity, not one of each file.
- [Sheet layouts](Sheet_Layouts) arrange the required quantities. The shop may rearrange them while preserving dimensions and grain along the long axes of spars.
- [Positioned STEP parts](Positioned_STEP) show assembled locations.
- [Paper templates](../Print_Templates/README.md) support manual marking.

DXF units are millimetres. Cut only **CUT** layers. Labels, stock outlines and sanding guides are not cutting paths. Establish kerf compensation with the actual machine and a tab/slot coupon. Do not scale parts to fit stock.

The register includes both wings. A62F/A62R form the split spine with two A63-profile cheeks, installed as A63/A64. Do not count the assembled A62 STEP reference as another cut part. Follow the [nose joint instructions](../05_Assembly/Nose_Bypass_Build.md).

Use A24/A44 sanding guides to finish edges to the skin while preserving the tube bores. Check the A26 motor pattern against the actual motor. See the [profile atlas](../../Build%20Guide/Reference/Manufacturing_Profile_Atlas.pdf) and [assembly guide](../../Build%20Guide/01_Airframe_Manufacturing_and_Assembly.pdf).
