## 2025-02-03 - Raster images embedded in SVGs
**Learning:** Found a performance anti-pattern where large PNG files are base64-encoded and embedded inside SVG files. This increases file size (due to base64 overhead) and requires the browser to parse XML before decoding the image.
**Action:** Identify such SVGs, extract the raw base64 data to a standalone raster file (PNG/JPG), and update CSS/HTML to reference the raster file directly. Use `grep -oP '(?<=base64,)[^\"]*' "file.svg" | base64 -d > "file.png"` for extraction.
