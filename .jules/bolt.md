# Bolt's Journal - Critical Learnings

## 2025-02-05 - Base64 SVG Anti-pattern
**Learning:** Embedding large raster images as base64 strings inside SVG files increases file size (due to base64 encoding overhead) and adds decoding complexity for the browser.
**Action:** Extract base64 raster images from SVGs and reference them directly as binary files (e.g., .png) in CSS or HTML.

## 2025-02-05 - Handling Filenames with Spaces
**Learning:** Standard `for` loops in bash fail on filenames with spaces.
**Action:** Use `find -print0 | xargs -0` or similar robust patterns to identify and process assets with spaces in their names.
