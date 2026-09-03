# Measurement Wheel

## Proportiyn.Penny

The Proportiyn.Penny is a circular measurement tool for Pyxl.Papyr.Puppyt rigs.

A straight line through the center of the circle (a diameter) is divided into equal parts and can be rotated to any angle. Each subdivision count is named after a coin.

---

## Coin Divisions

| n | Coin | Center is mark? |
|---|------|-----------------|
| 1 | Penny | No |
| 2 | Half Dollar | Yes |
| 3 | Tremissis | No |
| 4 | Quarter | Yes |
| 5 | Nickel | No |
| 6 | Sixpence | Yes |
| 7 | Sevenpence | No |
| 8 | Eightpence | Yes |
| 9 | Ninepence | No |
| 10 | Dime | Yes |

### Coin Notes

- **Tremissis** — Late-Roman / Byzantine gold coin, literally one third of a solidus.
- **Sixpence** — British coin (six pence, "tanner"), circulated until 1980.
- **Sevenpence / Eightpence / Ninepence** — Extend the pence pattern from sixpence — not themselves commonly minted denominations.
- **Dime** — From the French *disme*, "tenth part."

---

## Geometry Model

The diameter line is divided into *n* equal parts.

- When *n* is **even**, one division point falls exactly on the center, and marks (measured from the center outward) land at q = 1, 2, … n/2.
- When *n* is **odd**, the center sits between two marks instead. The nearest marks sit half a segment off-center, at q = 0.5, 1.5, …

This same diameter-division principle applies to every Proportiyn.Penny — only the subdivision count changes.

---

## Machine-readable

See `proportiyn_penny.json` for the full schema with per-division marks, measurements, and coin notes.
