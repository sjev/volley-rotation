# Volleyball Rotation Board - Design

## 🎯 Goal
Digital whiteboard for visualizing volleyball rotations and checking rotation faults. Coach drags players, rotates, spots problems, done.

---

## ✅ Keep (From Current Implementation)

### Court
- Half-court, 6 zones (4-3-2 front, 5-6-1 back) with light borders
- Draggable colored chips (50px circles) with role labels
- Drag enlarges chip slightly
- Constrained to court bounds

### Controls (3 buttons only)
- **Rotate ←** (counterclockwise)
- **Rotate →** (clockwise)
- **Reset** (snap chips to zone centers)

### Rotation Logic
- Rotate buttons shift zone assignments (1→2→3→4→5→6→1)
- Chips move to their assigned zone centers on rotation buttons.
- Reset button snaps chips to their assigned zone centers

### Fault Detection
- Check 7 overlap rules (left-right per row, front-back per column)
- Highlight fault chips with red glow animation
- Status bar: "✓ Rotatie OK" (green) or "⚠ Rotatiefout + details" (red)

---

## ❌ Remove

- **Sidebar** (player list is redundant - info already on court)
- **Serve/Receive toggle** (unused, always receiving)
- **Naar Zones button** (duplicate of Reset)
- **Header bar** (wasted vertical space, title in browser tab is enough)

---

## 🎨 Player Roles

Use current Dutch labels from implementation:
- **SV** (Spelverdeler / Setter) - blue
- **PL1/PL2** (Passer-loper / Outside Hitter) - green
- **M1/M2** (Middenblokeerder / Middle Blocker) - red
- **D** (Diagonaal / Opposite) - yellow

6 players, no libero for now.

---

## 📐 Layout

```
[← ]  [→] [Reset]
┌─────────────────────────┐
│  4    │   3   │    2    │
│       │       │         │
├───────┼───────┼─────────┤
│  5    │   6   │    1    │
│       │       │         │
└─────────────────────────┘
[Status: ✓ Rotatie OK]
```

Single column layout, full width court, controls above, status below.
Use icons on buttons instead of text

---

## 🚫 Out of Scope

- Multi-language (keep Dutch only)
- 3-meter line (visual clutter)
- Libero substitution
- Serving positions
- Score tracking
- Statistics
