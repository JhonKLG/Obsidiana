## 2026-02-02 - SVG Base64 Performance Anti-pattern
**Learning:** Found a large SVG (928KB) being used as a background image. It was actually just a wrapper for a large base64-encoded PNG. This is a performance anti-pattern because:
1. Base64 encoding increases file size by ~33% compared to binary.
2. The browser has to decode the base64 string before it can render the image, adding CPU overhead.
3. SVG parsing of large text strings is slower than loading a direct raster image.

**Action:** Always check large SVGs for embedded base64 data. If the SVG doesn't contain significant vector paths, extract the base64 to a standalone PNG/JPEG and reference it directly in CSS.
