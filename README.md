# Road Strip Diagram Tool

A standalone road-strip diagram editor for creating, importing, and exporting road inventory diagrams.

Use the File menu to load or save an editable JSON project. The project file includes the diagram, custom categories, label settings, and view scale. Reset to empty prompts you to clear without saving, save before clearing, or cancel.

The View menu resets zoom or jumps to the point-label controls. The Export menu provides PDF and JPG output. Station axes begin at the lowest station used in the diagram; station headings and point station labels are vertical and omit the `ST` prefix.

The input categories are grouped as Information (Boundary, Settlement, Terrain, Construction, and Maintenance), Existing (Pavement, Structure, and Side Drain), Design (Speed, Pavement, Structure, and Side Drain), and Road Health (IRI and FWD). Side Drain ranges can be assigned to LHS, RHS, or both sides of the dashed road-centerline reference; LHS is above the centerline and RHS is below it in increasing-station direction. Side Drain Dimension and Station labels can be toggled in the Labels controls. Existing drains use thicker blue-gray lines and Design drains thicker aqua lines; Pipe Culvert is dotted, Box Culvert dashed, U-Ditch solid with a centered dash-dot mark, and Canals double-lined. The legend lists each drain type once regardless of side and abbreviates Existing and Design as Ex and De. IRI uses the Bad-to-Good condition list, while FWD accepts a numeric value in MPa for each range.

Pavement strip thickness scales with the entered road width. Custom categories can be removed, including their associated items. FWD ranges are plotted against a dashed, user-entered base line in MPa. Diagram item labels are vertical; crowded point labels use two staggered columns with leader lines, and labels that still collide are omitted.

## Run locally

Open [Road Strip Diagram Tool.html](./Road%20Strip%20Diagram%20Tool.html) in a recent browser. Keep the `symbols` folder beside the HTML file so the app can load its diagrams and export symbols.

## Deploy to Vercel

1. Import this GitHub repository from the Vercel dashboard.
2. Select **Other** as the framework preset.
3. Leave the build command empty and use `.` as the output directory.
4. Deploy. The root route is configured to open the diagram tool.

The app is static and does not require a server, build step, or environment variables.
