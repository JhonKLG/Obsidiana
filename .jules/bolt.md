## 2024-05-20 - SVG with Embedded Base64 Image
**Learning:** Embedding large, base64-encoded raster images inside an SVG is a significant performance anti-pattern. The SVG provides no benefit and bloats the file size, blocking rendering.
**Action:** In the future, when I find an SVG used only to display a raster image, I will extract the raster image, optimize it, and reference it directly in the CSS or HTML. I will then delete the redundant SVG.
