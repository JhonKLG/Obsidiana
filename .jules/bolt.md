## 2025-02-04 - Base64 in SVG Anti-pattern
**Learning:** Found a 928KB SVG file that was primarily a base64-encoded PNG. This is a performance anti-pattern as it increases file size by ~33% and adds parsing overhead.
**Action:** Always check large SVG files for base64 content and extract them to standalone PNG/WebP files when they are used as background images.
