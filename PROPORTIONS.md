# Pyxl.Papyr.Puppyt — Head-to-Toe Proportional Guide

**1H = 33.0 pyxl · 1 pyxl = 10px render**

**Rounding:** Pyxl grid (.0/.5) — quarter-head fractions (n.25/n.5/n.75 H) exempt.

---

## HEAD — 1.0H / 33 pyxl

| Landmark | Y (pyxl) | Y (H) | Note |
|----------|-----------|-------|------|
| crownpoint | -14 | -0.42H | Top of skull |
| browpoint | 0 | 0 | Origin. Eye line |
| leftpoint / rightpoint | 0 | 0 | Ear level. ±12.5 x |
| cheekpoint | 4 | 0.12H | Zygomatic. ±9.5 x |
| jawpoint | 7 | 0.21H | Masseter corner. ±7 x |
| nasalpoint | 14 | 0.42H | Skull base. Spinal attach |
| chinpoint | 19 | 0.58H | Chin bottom |

**Head pieces:**

| Piece | W × H (pyxl) | Note |
|-------|--------------|------|
| Skull | 25 × 28 | Ellipse |
| Faceplate | 21.5 × 18 | Triangle |
| Jaw | 14 × 12 | Rect |

---
## NECK — 0.5H / 16.5 pyxl

| Landmark | Y (neck-local) | Note |
|----------|----------------|------|
| spinalpoint | 0 | Skull attach (mates nasalpoint) |
| adampoint | 8.25 | 0.25H below spinal |
| vpoint | 16.5 | 0.5H below spinal. Torso attach |

| Piece | W × H |
|-------|-------|
| Neck | 9w (top) → 11w (bottom) × 16.5h |

---
## TORSO — 1.5H / 49.5 pyxl

| Landmark | Y (torso-local) | Note |
|----------|-----------------|------|
| left_shoulderpoint / right_shoulderpoint | -49.5 | ±18.75 x. 1.5H span (Vitruvian) |
| left_collarpoint / right_collarpoint | -49.5 | ±4.5 x. Mates 9 pyxl neck top |
| vpoint / collarpoint | -49.5 | (0, -49.5). Neck attach |
| navelpoint | 0 | Origin. Waist junction |

| Piece | W × H |
|-------|-------|
| Torso | 37.5w (shoulders) → 29w (navel) × 49.5h |
| Torso side length | 53 pyxl |

---
## BACKBONE — 0.5H / 16.5 pyxl

| Landmark | Y | Note |
|----------|---|------|
| ribpoint | 0 | Xiphoid. Origin |
| navelpoint | 8.25 | 0.25H below rib |
| hippoint | 16.5 | 0.5H below rib. Hip attach |

| Piece | W × H |
|-------|-------|
| Backbone | 2 × 16.5 |

---
## HIP — 1.0H / 33 pyxl

| Landmark | X, Y (hip-local) | Note |
|----------|------------------|------|
| sacralpoint | 0, 0 | Origin. Backbone attach. ∞ center |
| left_hippoint / right_hippoint | ±18.75, -16.5 | Iliac crests. 1.5H span |
| left_socket / right_socket | ±9.375, 8.25 | Femur attach. 0.25H below sacrum |

| Piece | W × H |
|-------|-------|
| Hip (∞) | 37.5 × 33 — crest-to-socket = 1.0H |

---
## ARM — 3.5H / 115.5 pyxl (shoulder → fingertip)

| Segment | Length | Joint → Joint |
|---------|--------|---------------|
| Upper arm (humerus) | 49.5 pyxl / 1.5H | shoulderpoint → elbowpoint |
| Forearm (radius/ulna) | 41.25 pyxl / 1.25H | elbowpoint → wristpoint |
| Hand | 24.75 pyxl / 0.75H | wristpoint → fingertip |

| Bone | Shaft | Joint balls |
|------|-------|-------------|
| Humerus | 2.5 pyxl | shoulder 3.5r → elbow 3.0r |
| Forearm | 2.0 pyxl | elbow 3.0r → wrist 2.5r |
| Hand | 3.0 pyxl, 8w palm | wrist 2.5r → fingertip 2.0r |

---
## LEG — 4.25H / 140.25 pyxl (hip socket → sole)

| Segment | Length | Joint → Joint |
|---------|--------|---------------|
| Thigh (femur) | 66 pyxl / 2.0H | hippoint → kneepoint |
| Shin (tibia/fibula) | 66 pyxl / 2.0H | kneepoint → anklepoint |
| Foot | 33 pyxl L / 8.25 pyxl H | anklepoint → toepoint |

| Bone | Shaft | Joint balls |
|------|-------|-------------|
| Femur | 3.5 pyxl | hip 4.5r → knee 4.0r |
| Shin | 3.0 pyxl | knee 4.0r → ankle 3.0r |
| Foot | 3.0 pyxl | ankle pivot, heel 2.5r |

Foot geometry: ankle (0,0) → heel (-8.25, 8.25) → toe (24.75, 8.25). Total heel→toe = 33 pyxl / 1.0H.

---
## FULL FIGURE STACK

| Segment | pyxl | Heads | Cumulative (crown=0) |
|---------|------|-------|----------------------|
| Crown → brow | 14 | 0.42H | 14 |
| Brow → nasal | 14 | 0.42H | 28 |
| Nasal → chin | 5 | 0.15H | 33 | ← **1.0H — head complete** |
| Chin → v (neck) | 16.5 | 0.5H | 49.5 |
| V → navel (torso) | 49.5 | 1.5H | 99 |
| Navel → hip sockets | 16.5 | 0.5H | 115.5 | ← **3.5H — crown to hip sockets** |
| Hip sockets → knee | 66 | 2.0H | 181.5 |
| Knee → ankle | 66 | 2.0H | 247.5 |
| Ankle → sole | 8.25 | 0.25H | 255.75 | ← **7.75H — crown to sole** |

**Total figure height: 255.75 pyxl / 7.75H**

| Measurement | pyxl | Heads |
|-------------|------|-------|
| Shoulder span | 37.5 | 1.14H |
| Hip span (crests) | 37.5 | 1.14H |
| Hip socket span | 18.75 | 0.57H |
| Arm reach (shoulder → fingertip) | 115.5 | 3.5H |
| Leg length (hip socket → sole) | 140.25 | 4.25H |
| Head width | 25 | 0.76H |
| Neck width | 9 → 11 | 0.27H → 0.33H |
