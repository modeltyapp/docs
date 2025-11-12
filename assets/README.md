# Assets Directory

This directory contains images and media files referenced throughout the Modelty documentation.

## Required Images

Upload the following images to this directory to complete the documentation:

### Overview & Ecosystem

- **ecosystem-flywheel.png** - Diagram showing the compounding flywheel: wallet → ops → vault → more money
  - Referenced in: `index.mdx`, `products/overview.mdx`

### Product Images

- **oruon-dashboard.png** - Screenshot of Oruon wallet dashboard interface
  - Referenced in: `index.mdx`, `products/oruon.mdx`

- **oruon-subwallets-topology.png** - Diagram showing sub-wallet structure and relationships
  - Referenced in: `products/oruon.mdx`

- **sasha-signal-loop.png** - Diagram showing Ops AI signal processing: signals in → guidance out
  - Referenced in: `index.mdx`, `products/ops.mdx`

- **rmc-triage.png** - Diagram showing Vault leak detection workflow: detection → evidence → takedown
  - Referenced in: `index.mdx`, `products/removemycontent.mdx`

### Strategy & Architecture

- **moat-layers.png** - Diagram showing three moat layers: money, integrity, workflow
  - Referenced in: `strategy/moat.mdx`

- **architecture-highlevel.png** - High-level system architecture diagram
  - Referenced in: `company/architecture.mdx`

- **roadmap-swimlanes.png** - Quarterly roadmap showing parallel development lanes
  - Referenced in: `company/roadmap.mdx`

## Image Specifications

### Recommended Specifications

- **Format:** PNG (with transparency) or JPG
- **Resolution:** 1200px width minimum (for high-DPI displays)
- **Aspect Ratio:** 16:9 for diagrams, variable for screenshots
- **File Size:** Optimize for web (<500KB preferred)

### Style Guidelines

- **Color Palette:** Use Modelty brand colors
  - Primary: #7C3AED (purple)
  - Light: #A78BFA
  - Dark: #5B21B6
- **Typography:** Clean, professional fonts (Inter, SF Pro, or similar)
- **Style:** Modern, minimal, consistent across all diagrams

## Creating Images

### Tools Recommendations

- **Diagrams:** Figma, Excalidraw, Mermaid, or similar
- **Screenshots:** Native tools + editing software for annotations
- **Flowcharts:** Lucidchart, Draw.io, or Mermaid

### Placeholder Strategy

Until actual images are available:
- Documentation will render with broken image indicators
- Alternative: Create simple placeholder diagrams with the structure indicated
- Consider using Mermaid diagrams inline where appropriate

## Uploading to GitBook

1. Navigate to your GitBook project
2. Go to the Assets section in the left sidebar
3. Upload images to maintain the same file paths
4. Alternatively, commit images to this directory and sync with GitBook

## Notes

- All image paths in the documentation use the `/assets/` prefix
- Ensure filenames match exactly (case-sensitive)
- Images are optimized and compressed before upload
- Consider CDN caching for large images
