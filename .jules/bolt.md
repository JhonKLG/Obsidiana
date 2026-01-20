## 2024-06-25 - SVG with embedded base64 raster image
**Learning:** Embedding large base64 encoded raster images inside SVG files is a performance anti-pattern. It increases the size of the initial document and blocks the browser from discovering and loading the image until after the CSS/SVG is parsed.
**Action:** Extract the raster image, save it as a separate file (e.g., .png), and reference it directly from the CSS using `background-image`. Delete the original SVG to save space.
