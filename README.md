# Penguin Data Visualization - 5 Ways

This project explores the visualization of the Palmer Penguins dataset (`penglings.csv`) using five different technologies. The goal was to create a consistent scatter plot across all platforms, mapping Flipper Length to the x-axis, Body Mass to the y-axis, Species to color, and Bill Length to point size.

## 1. R + ggplot2
The baseline visualization was created using R and the `ggplot2` library. This method provided the design standard for the subsequent implementations.

!R ggplot2 Screenshot

- **Technical Achievement:** Used the `guides()` function to explicitly control legend ordering, ensuring "Species" and "Bill Length" appeared in the correct order.
- **Design Achievement:** Implemented a custom color palette (`#fe9013`, `#9932cc`, `#018b8b`) and a clean grey background with white grid lines to set the project's visual standard.

## 2. D3.js
A web-based version built from scratch using SVG elements.

!D3.js Screenshot

- **Technical Achievement:** Implemented complex axis logic using `tickValues` and `tickFormat` to display labels only on major increments (every 10 for X, every 1000 for Y) while maintaining minor grid lines. Managed SVG layering to ensure grid lines remained behind the data points.
- **Design Achievement:** Replicated the `ggplot2` aesthetic exactly, including the specific grey background color and white grid line weights.

## 3. Python Turtle
A low-level, procedural approach to data visualization.

!Python Turtle Screenshot

- **Technical Achievement:** Developed a custom coordinate scaling system to map raw data values (ranging from 170-230 for flipper length and 2700-6300 for body mass) to the pixel-based Turtle canvas.
- **Design Achievement:** Manually drew the background, axes, and labels using turtle movements, maintaining visual consistency with the high-level libraries.

## 4. Altair (Python)
A declarative statistical visualization library for Python.

!Altair Screenshot

- **Technical Achievement:** Utilized Vega-Lite `labelExpr` to conditionally hide axis labels, achieving the specific "label every 10/1000" requirement while keeping the grid dense.
- **Design Achievement:** Used `configure_view` and `configure_axis` to globalize the theme, ensuring the plot area and grid matched the project's visual identity.

## 5. SAS

!Fifth Tool Screenshot

- **Technical Achievement:** iughoiugvb.
- **Design Achievement:** hubihoghvbighu.

---

## Overall Technical Achievements
- **Cross-Platform Data Cleaning:** Handled `NA` values consistently across R, JavaScript, and Python to ensure data integrity in all plots.
- **Asynchronous Loading:** Successfully implemented top-level `await` for CSV loading in the D3 module, avoiding common race conditions.
- **Normalization Algorithms:** Created reusable logic for mapping quantitative variables to visual properties like circle radius and color hex codes across procedural and declarative tools.

## Overall Design Achievements
- **Visual Unity:** Despite using vastly different rendering engines (SVG, Canvas, Grid-based, Procedural), the final outputs maintain a unified "brand" through consistent use of typography, color, and spacing.
- **Perceptual Sizing:** Fine-tuned the size scales in each tool so that the variation in Bill Length is visually distinct without causing excessive occlusion.
- **Transparency for Density:** Applied a consistent 0.8 alpha transparency to all points, allowing the viewer to perceive data density in overlapping regions.

## How to Run

### R Method
Open `r_method.rmd` in RStudio and knit to HTML.

### D3 Method
Host the directory locally (e.g., `python3 -m http.server`) and open `d3_method.html` in a browser.

### Turtle Method
Run `python turtle_method.py` from your terminal.

### Altair Method
Run `python altair_method.py` to generate `altair_method.html` and host locally.

### R Method
Open `sas_method.SAS` in SAS and run.
```
