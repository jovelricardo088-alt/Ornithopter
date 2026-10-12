# Gears and Mechanism

![Page 32](../scans/page-32.jpg)

## What my notes say

**Goal of Phase 1:** convert the motor's rotation into a flapping motion.

**Gears** are mechanical parts with teeth that transmit motion. When one gear turns, the gear meshed with it turns too.

**Gear train:** multiple gears linked together to transfer power. A gear train lets me change torque, speed, or the direction of movement.

**How this applies to my ornithopter:** a DC motor supplies rotational motion, and the gear train carries it to the wings to create a flapping motion.

**Gear ratio** controls the trade-off between torque and speed.

**Why it matters:** high torque means I can move heavier wings with more force, but the flaps are slower.

## How this connects to my design

- Two meshed gears turn in opposite directions, which is what I want for wings that flap symmetrically.
- Each gear drives a connecting rod attached off-center, so the rod pushes and pulls the wing arm up and down. That crank-and-rod linkage is what actually turns rotation into flapping.
- The gears set how fast the wings flap and how much force they have.
- The gear ratio math is in [05-gear-ratio.md](05-gear-ratio.md).

## Corrections 

- In my original note I wrote that the gear train creates the flapping. More precisely, the gear train changes speed and torque, and the crank and connecting rod create the flapping motion.
- Gear ratio = teeth on the driven gear / teeth on the driving gear. A bigger ratio means slower output and more torque.
- Open question: more gear stages give me more reduction, but they add weight and friction. I need to test how much that matters at under 100 g.
