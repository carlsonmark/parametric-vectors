# parametric-vectors

Small tools that generate parametric vector files (SVG/DXF) for laser and CNC cutting.

Each tool is a single self-contained HTML file. Open it straight from disk, or host the
repo with GitHub Pages. There is no build step and nothing to install.

## Tools

### [Spherical Waffle Shelf](spherical-waffle-shelf/index.html)

An interlocking plywood shelf shaped like half an ellipsoid, flat against the wall.
Horizontal shelves are slotted from the back and vertical dividers from the front, and they
slide together.

- **Size:** width, height, depth, number of shelves and dividers (evenly spaced).
- **Material:** thickness and slot clearance (default +0.1 mm; tune it with a test cut).
- **Flat bottom (optional):** the bottom is cut off at a % of the height and replaced by a
  base plate. Divider tabs go through mortises in the base, and optional feet tab in underneath.
- **Back panel (optional):** an elliptical panel behind the shelves. Each shelf gets a tab
  on its back edge between every pair of dividers, and the tabs lock into mortises in the
  panel. The panel can be split into several pieces; the seams fall behind dividers.
- **Laser or CNC:** CNC mode adds dogbones to inside corners, sized to the endmill (1/8",
  1/4" or custom), and keeps pieces at least one endmill width apart.
- **Sheets:** presets for Trotec Speedy (730 × 430), Thunder Nova 51 (1300 × 900), and 4'×4'
  and 4'×8' plywood, or a custom size. Pieces are packed in rows across as many sheets as needed.
- **Labels:** optional engraved piece IDs in a single-stroke font (S1… bottom to top,
  D1… left to right, B base, F feet, P back panel).
- **Checks:** flags shallow pieces and short or edge-breaking joints, and can drop them.
- **Export:** one SVG per sheet in real mm, with cut lines in red (`#ff0000`) and labels in
  blue (`#0000ff`) on separate layers. Optional R12 DXF on `CUT` and `ENGRAVE` layers.
- **Saving and sharing:** settings live in the page URL after `#`, so bookmarks and links
  restore them. Every exported SVG/DXF also stores its settings; use
  *Load settings from SVG/DXF…* to get them back.

The 3D preview uses three.js from a CDN, so it needs internet access and WebGL. Everything
else works offline.
