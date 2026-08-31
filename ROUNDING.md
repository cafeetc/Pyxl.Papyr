# Pyxl.Papyr Rounding Rules

## Base system: Pyxl rounding

All coordinates and lengths use **Pyxl rounding** by default:

| Fraction | Rounds to |
|----------|-----------|
| .01 – .35 | ↓ whole |
| .35 – .64 | .5 |
| .65+ | ↑ whole |

Allowed values: 0.0, 0.5, 1.0, 1.5, 2.0, …

## Head lengths

Head piece measurements are displayed with **1 decimal place** for readability, but must land on the Pyxl grid (.0 / .5) unless covered by an exception below.

Example: cheek_jaw true distance = 3.905 pyxl → Pyxl rounds to **4.0 pyxl** (displays as 4.0)

## Exceptions — Quarter-head fractions

All quarter-head fractions bypass Pyxl rounding, in ALL pieces:

| n·H | pyxl @ H=33 | Exempt |
|-----|-------------|--------|
| 0.25H | 8.25 | ✓ |
| 0.50H | 16.5 | ✓ |
| 0.75H | 24.75 | ✓ |
| 1.25H | 41.25 | ✓ |
| 1.50H | 49.5 | ✓ |
| 1.75H | 57.75 | ✓ |
| 2.25H | 74.25 | ✓ |
| … | … | ✓ |

Rationale: H = 33 pyxl is not divisible by 4, so all quarter-head measurements fall between grid points. Rather than snapping asymmetrically, any measurement equal to n + 0.25/0.5/0.75 heads is whitelisted as exact.

General rule: if `value / H ≡ 0.25 or 0.5 or 0.75 (mod 1)`, exempt — use exact pyxl.

## Current uses

- Neck: spinal→adam = 8.25 pyxl (0.25H), adam→v = 8.25 pyxl (0.25H)
- Backbone: rib→navel = 8.25 pyxl (0.25H), navel→hip = 8.25 pyxl (0.25H)
- Hip: socket Y = 8.25 pyxl below sacrum (0.25H)
- Arm: shoulder→elbow = 49.5 pyxl (1.5H), elbow→wrist = 41.25 pyxl (1.25H), wrist→fingertip = 24.75 pyxl (0.75H)
- Leg: hip→knee = 66 pyxl (2.0H), knee→ankle = 66 pyxl (2.0H)
- Foot: ankle→sole = 8.25 pyxl (0.25H), heel→toe = 33 pyxl (1.0H), heel behind ankle = 8.25 pyxl (0.25H), ankle→toe = 24.75 pyxl (0.75H)

## Summary

| Domain | Rounding | Display precision | Exceptions |
|--------|----------|-------------------|------------|
| All pieces | Pyxl (.0/.5) | 1 decimal for head lengths | Quarter-head fractions exempt: n.25/n.5/n.75 H |

1H = 33.0 pyxl
