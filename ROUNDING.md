# Pyxl.Papyr — Coordinate Rounding Rules

All coordinates in pyxl units. 1 pyxl = 10px render.

Snap targets: 0.00, 0.25, 0.50, 0.75, 1.00

| Fractional part | Direction | Snap to |
|-----------------|-----------|---------|
| 0.00 – 0.12    | ← down    | 0.00    |
| 0.13 – 0.24    | → up      | 0.25    |
| 0.25           | = exact   | 0.25    |
| 0.26 – 0.37    | ← down    | 0.25    |
| 0.38 – 0.49    | → up      | 0.50    |
| 0.50           | = exact   | 0.50    |
| 0.51 – 0.62    | ← down    | 0.50    |
| 0.63 – 0.74    | → up      | 0.75    |
| 0.75           | = exact   | 0.75    |
| 0.76 – 0.87    | ← down    | 0.75    |
| 0.88 – 0.99    | → up      | 1.00    |

Cutoffs: 0.125, 0.375, 0.625, 0.875 — slight bias toward rounding down.

Visual:

```
0.00 ············· 0.25 ············· 0.50 ············· 0.75 ············· 1.00
←←←←←←←←←←←←|→→→→→→→→→→→|←←←←←←←←←←←←|→→→→→→→→→→→→|←←←←←←←←←←←←|→→→→→→→→→→→→|←←←←←←←←←←←←|→→→→→→→→→→→→
0.00  0.12 0.13   0.25   0.26   0.37 0.38   0.50   0.51   0.62 0.63   0.75   0.76   0.87 0.88   1.00
     ↑                  ↑                  ↑                  ↑                  ↑
  ← down            ← down            ← down            ← down
         → up               → up               → up               → up
```

The ← down intervals (0.26–0.37, 0.51–0.62, 0.76–0.87) round down from above.
The → up intervals (0.13–0.24, 0.38–0.49, 0.63–0.74, 0.88–0.99) round up from below.
Exact snap values (0.00, 0.25, 0.50, 0.75) stay as-is.

Applies to all keystone coordinates, shape points, and bone lengths in Pyxl.Papyr blueprint JSONs.
