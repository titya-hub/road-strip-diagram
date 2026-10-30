# Road Strip Diagram Tool

A standalone road-strip diagram editor for creating, importing, and exporting road inventory diagrams.

## Run locally

Open [Road Strip Diagram Tool.html](./Road%20Strip%20Diagram%20Tool.html) in a recent browser. Keep the `symbols` folder beside the HTML file so the app can load its diagrams and export symbols.

## Deploy to Vercel

1. Import this GitHub repository from the Vercel dashboard.
2. Select **Other** as the framework preset.
3. Leave the build command empty and use `.` as the output directory.
4. Deploy. The root route is configured to open the diagram tool.

The app is static and does not require a server, build step, or environment variables.
