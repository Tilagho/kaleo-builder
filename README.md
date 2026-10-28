# Kaleo Builder

Kaleo Builder is a single-page 3D builder for Home Depot–style materials: dimensional lumber (2x4s and the rest of the rack), sheet goods, and common hardware such as brackets, hangers, and deck blocks. Sizes are actual dimensions — a 2x4 is 1½″ × 3½″. Place parts, move and rotate them, cut joinery, and read a cut list with rough Maui price estimates.

This is a **mobile test preview**. It is the desktop builder, adapted so an iPhone can use it. The app is one static `index.html` (Three.js is inlined). There is no build step and no backend. GitHub Pages can publish the repository root as-is.

## Run it

- Pages: the site root is `index.html`.
- Locally: open `index.html`, or run `python3 -m http.server 8734` and visit http://127.0.0.1:8734/.

Work autosaves in this browser. **Save** downloads a `.json` file you can open later.

## On a phone

Below 1040px wide (current iPhones in portrait and landscape):

- The 3D view fills the screen. The header is one row: project name, undo, redo, and **Menu** (templates, new, open, save, PNG, print, help).
- **Parts** and **Details** live in a bottom bar. They open as sheets. In portrait the sheet covers about the lower two-thirds and the model stays visible above it. In landscape the sheet comes in from the side. Tap the view, or the bar button again, to close.
- One finger orbits, even if you start on a part. Pinch zooms. Two fingers pan. Tap a part to select it.
- With a part selected, **Slide** follows your finger across the ground. Left, Right, Back, Front, Up, and Down step by the current grid. The colored gizmo arrows are larger than on desktop.
- Tap a library part to add it, or press and drag it up out of the sheet onto the view to drop it at that spot.
- Tap targets are at least 44px. The layout uses safe-area insets and the visible viewport height, and the page does not scroll sideways.

Above 1040px the original three-column layout is back: library, view, inspector.

## Easier with a keyboard or mouse

These still work, and they are not the primary phone path:

- Keyboard shortcuts (undo, nudge arrows, R / T to rotate, Delete, F to fit, G / E / M for tools). The same actions are on screen.
- Right-drag and middle-mouse pan. On a phone, pan with two fingers.
- Dragging a part directly with one finger. On a phone that gesture orbits, so the part moves with Slide, the step buttons, or the gizmo.
- The freehand sheet-profile editor takes touch, but tight curves are easier with a mouse or stylus.
- Print plans opens the browser’s print dialog.
