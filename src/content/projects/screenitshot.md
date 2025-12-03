---
title: ScreenItShot
publishDate: 2025-12-01 00:00:00
img: /assets/screenitshot.png
img_alt: Screenshot of a PDF document rendered by screenitshot
description: |
  A Node.js tool that converts documents (PDF, DOCX, XLSX, PPTX, EPUB) to high-quality screenshots using browser-based rendering with pinned dependencies for reproducibility.
tags:
  - Documents
  - Screenshots
  - Automation
  - DevTools
link: https://github.com/xiaoyuanzhu-com/screenitshot
---

Turn any document into a pixel-perfect screenshot.

screenitshot uses Playwright and Chromium to render documents through battle-tested JavaScript libraries—PDF.js for PDFs, docx-preview for Word files, ExcelJS for spreadsheets. The result? Consistent, high-quality screenshots that look identical every time.

### Why Browser-Based Rendering?

Native libraries give inconsistent results. The JavaScript ecosystem has mature, well-maintained libraries for every format. By rendering in Chromium, you get the same quality as viewing in a browser—because that's exactly what's happening.

All dependencies are pinned. Chromium version, JS libraries, everything. Run it today or a year from now, get the same output.

### Supported Formats

**Documents** — PDF, DOCX, XLSX, PPTX, EPUB, Markdown, HTML, RTF

**Data** — CSV, JSON, GeoJSON, GPX

**Code** — Any source file with syntax highlighting, Jupyter notebooks

**Web** — URLs rendered with full JavaScript support

### How It Works

```bash
# Install globally
npm install -g screenitshot

# Convert a PDF
screenitshot document.pdf output.png

# Specific page
screenitshot presentation.pptx slide-3.png --page 3
```

Programmatic API for Node.js. Python wrapper available. Docker image for CI/CD pipelines.

Single self-contained HTML templates per format. No CORS issues. No external dependencies at runtime.
