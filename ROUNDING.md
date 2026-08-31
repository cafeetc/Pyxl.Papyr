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

## Exceptions

The following head-fraction values are allowed to bypass Pyxl rounding, in ALL pieces (head and body):

| Fraction | pyxl @ H=33 | Rounds to |
|----------|-------------|-----------|
| 0.25H | 8.25 | exempt — use 8.25 |
| 0.75H | 24.75 | exempt — use 24.75 |

Rationale: H = 33 pyxl is not divisible by 4, so quarter-head measurements fall between grid points in both Pyxl and head rounding systems. Rather than snapping asymmetrically, 0.25H / 0.75H are whitelisted as exact values.

Current uses:
- Neck: spinal→adam = 8.25 pyxl (0.25H), adam→v = 8.25 pyxl (0.25H)
- Backbone: rib→navel = 8.25 pyxl (0.25H), navel→hip = 8.25 pyxl (0.25H)
- Hip: socket Y = 8.25 pyxl below sacrum (0.25H)

## Summary

| Domain | Rounding | Display precision | Exceptions |
|--------|----------|-------------------|------------|
| All pieces | Pyxl (.0/.5) | 1 decimal for head lengths | 0.25H = 8.25, 0.75H = 24.75 |

1H = 33.0 pyxl
