## 2025-01-24 - SVG Raster Wrapper Anti-pattern
**Learning:** Found a 928KB SVG file (`fondo.svg`) that was actually just a container for a large base64-encoded PNG. This adds unnecessary parsing overhead and increases file size.
**Action:** Extract base64 data to a native raster format (PNG/JPG) and reference it directly in CSS/HTML instead of using the SVG wrapper.
