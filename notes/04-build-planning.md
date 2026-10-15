# Build Planning

![Page 40](../scans/page-40.jpg)
![Page 43](../scans/page-43.jpg)

## Page 40: Scaling laws and weight budget

**Scaling laws** describe how an object's properties change relative to its size. Normally, weight increases faster than surface area as an object gets bigger.

**Square-cube law:**
- Length scales as L
- Area (the surface of the wing) scales as L²
- Volume and weight scale as L³

**Example:** if I double the dimensions of the body, the wings only get 4x bigger (L²), but the weight gets 8x bigger (L³). That means the wings must flap harder to create enough lift as weight goes up.

**Weight of parts (estimates):**

| Part | Weight |
|---|---|
| ESP32 | ~9 g |
| DRV8833 motor driver | ~1.5 g |
| 3-6 V DC motor | ~5 g |
| 1S LiPo battery (380-500 mAh) | ~10-15 g |
| Wires | ~3 g |
| **Total (electronics)** | **~30 g** |

Body parts estimate: 30-70 g.

## Page 43: Component sizes and layout

| Component | Dimensions |
|---|---|
| Motor | 31 mm long, 12 mm [check: diameter or height], 17 mm [check: which section], shaft 3 mm wide and 10 mm long |
| ESP32 | 29 mm x 52 mm |
| DRV8833 motor driver | 18.5 mm x 16 mm |

**Layout sketch:** the electronics fit in a body about 100 mm long and 50 mm wide. Power flows from the battery to the DRV8833 to the motor, and the ESP32 controls the driver. The bottom sketch shows the rough body shape with the wings attached.

## Why this matters

My goal is to keep the whole ornithopter under 100 g. This page is how I check that the parts fit inside the body and that the weight is realistic before I print anything.

## Corrections / open questions

- Length scales as L¹. My note just says "L", which means the same thing.
- The 30 g total only covers the electronics. The frame, gears, wings, and screws still need to be added, which is probably what the "30-70 g" body estimate is for.
- The weights are estimates. I need to weigh the real parts on a scale and replace these numbers.
- The motor weight (~5 g) is for the 3-6 V motor. If I use the higher-RPM motor or buy a new one (see [05-gear-ratio.md](05-gear-ratio.md)), the weight and dimensions on page 43 may change.
- The 3 mm motor shaft matters for the gear design, because the 10T motor gear needs a bore that fits it.
- Wing size is not planned yet. The square-cube law suggests the wing area I choose will decide how much weight the ornithopter can lift, so this is the next thing to calculate.
- - **Possible switch to an ESP32-C3:** I might replace the ESP32 with an ESP32-C3 (with header pins), which would decrease the weight. 
