# Design Decisions

My plan changed several times as I researched. This file records each change and why I made it.

## Decision 1: Gears or no gears?

**First idea (page 34):** no gears. I had a low-power 3-6 V DC motor (about 200-220 RPM), and using it directly seemed easiest.

**Changed to:** use a gear train.

**Why:** I kept imagining the mechanism with gears, and I find gears more interesting to design and build. A gear train also lets me tune speed and torque instead of depending on one motor's speed.

## Decision 2: Which flap rate to target?

**First idea (page 35):** model it on a budgie, which flaps about 15-17 times per second.

**Changed to:** 6 flaps per second.

**Why:**
- Many ornithopter builds are based on real birds, and the budgie was the one I saw most often.
- My ornithopter needs to weigh less than 100 g.
- Many ornithopters work best at roughly 5-10 flaps per second.
- 15-17 flaps per second is possible, but much harder to build and would stress the parts. 6 flaps per second is a realistic first target.

## Decision 3: Which motor?

**Considered (page 42):** buying a slower 300-500 RPM motor, so I wouldn't need gear reduction. It would be simpler and lighter, with more torque.

**Chosen:** keep the high-RPM motor I already have (12,000 RPM) and use a gear train and PWM speed control.

**Why:**
- Weight will load the motor and slow it down, so a low-output motor could be too weak to flap the wings.
- A high-output motor with gears gives me headroom, and PWM lets me tune the flap speed without worrying about weight slowing it down.
- I already own the motor.

## Summary

| Decision | Before | After |
|---|---|---|
| Mechanism | Direct drive, no gears | Gear train |
| Flap rate | 15-17 per second (budgie) | 6 per second |
| Motor | Low-RPM motor, no reduction | High-RPM motor + gears + PWM |

## Open questions

- **Motor speed:** my notes say 16,000 RPM, but I later said 12,000 RPM. I need to check the motor's label or datasheet since those are guesses based on Google information. With the 30:1 gear train on page 42, a 12,000 RPM motor gives about 400 RPM (about 6.7 flaps per second, no load), which is close to my 6 flap target.
- **Flap target:** page 41 says I would use 8 flaps per second with 10T : 58T gears, but I now plan for 6. 
- **Gears vs. a slower motor:** more gear stages add weight and friction. I haven't tested whether the gear train or a slower motor works better at under 100 g. I should test both if I can.
- **Real flap rate:** the RPM numbers are no-load. I'll measure the actual flap rate once the mechanism is printed and use PWM to adjust it.
