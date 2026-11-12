# Road Strip Diagram Tool

A standalone road-strip diagram editor for creating, importing, and exporting road inventory diagrams.

Use the File menu to load, save, or share an editable JSON project. The project file includes the diagram, custom/deleted categories, label settings, and view scale. Share links carry compressed project data in the URL, so separate projects have separate links and do not overwrite each other. Save Project uses a location picker where supported; otherwise, the browser handles the download location. Reset to empty prompts you to clear without saving, save before clearing, or cancel.

The View menu resets zoom or jumps to the label controls. Landmark, Existing/Design Structure, and Existing/Design Side Drain are initially listed; use the dropdown to add other categories and × to remove them. Choose whether each listed category shows Type/Value, Station, or Sum. Selected sums are grouped by type and appear below the category heading (range categories show length by type; point categories show count by type). Showing sums does not change diagram row heights or widen the category heading column. Category and group headings are left-aligned and vertically centered in a column sized to fit the widest heading; enabling Type/Value or Station labels changes row height only, not the heading column width. Station labels are kept within their category rows, which expand as needed without stretching color strips. The Export menu separates printing from PDF and JPG export. Print opens the browser print dialog; Export PDF opens it with a suggested diagram filename. JPG export lets you choose an output folder where supported. Station axes begin at the lowest station used in the diagram; station headings are vertical and omit the `ST` prefix.

The input categories are grouped as Information (Boundary, Settlement, Terrain, Construction, and Maintenance), Existing (Pavement, Structure, and Side Drain), Design (Speed, Pavement, Structure, and Side Drain), and Road Health (IRI and FWD). Side Drain ranges can be assigned to LHS, RHS, or both sides of the dashed road-centerline reference; the LHS/RHS indicators appear in the category heading. Side Drain Dimension and Station labels can be toggled in the Labels controls; LHS dimensions appear above the drain, RHS dimensions between the centerline and drain, and station labels below the centerline with leaders. Dimension labels are spaced horizontally and connected to their ranges. Existing drains use thicker blue-gray lines and Design drains thicker aqua lines; Pipe Culvert is dotted, Box Culvert dashed, U-Ditch solid with a centered dash-dot mark, and Canals double-lined. The legend lists each drain type once regardless of side and abbreviates Existing and Design as Ex and De. IRI uses the Bad-to-Good condition list, while FWD accepts a numeric value in MPa for each range.

Pavement strip thickness scales with the entered road width. IRI color strips keep a compact, fixed height, and FWD uses a reduced vertical plot scale. Category headings are left-aligned and vertically centered in the left column, which fits the widest heading; sums are fitted within that column without changing its width. Side-road rows use only the height needed for their lines and enabled labels. Any category can be removed from the current project with the × button beside the category selector, including its associated items. Reset to empty is at the bottom of the input panel. Custom range categories can optionally use LHS, RHS, or both sides of the road, with side indicators shown above and below the road centerline and the selected side recorded in the item list. FWD ranges are plotted against a dashed gray, user-entered base line in MPa, with gray vertical connectors between measured values. Diagram labels are horizontal except station headings, Structure dimension and station labels, and Side Drain station labels. Crowded point labels use leader lines. Structure value and station labels are distributed along shared levels with leaders attached to the text edge nearest the structure; repeated range endpoints are shown once per category row.

## Run locally

Open [Road Strip Diagram Tool.html](./Road%20Strip%20Diagram%20Tool.html) in a recent browser. Keep the `symbols` folder beside the HTML file so the app can load its diagrams and export symbols.

## Deploy to Vercel

1. Import this GitHub repository from the Vercel dashboard.
2. Select **Other** as the framework preset.
3. Leave the build command empty and use `.` as the output directory.
4. Deploy. The root route is configured to open the diagram tool.

The app is static and does not require a server, build step, or environment variables.
