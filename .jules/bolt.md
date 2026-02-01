## 2025-02-01 - Base64 Embedded in SVG Anti-Pattern
**Learning:** Found a 928K SVG file that was actually just a wrapper for a base64-encoded PNG. This is a common performance anti-pattern as it increases file size by ~33% due to base64 overhead and prevents efficient browser handling of the raster image.
**Action:** Always check large SVG files for base64 content. Extract the raster image and use it directly via CSS background-image or <img> tags to reduce asset size and improve performance.
