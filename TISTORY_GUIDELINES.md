# Tistory Tool Development Guidelines

## Project Goal
Develop a collection of premium, interactive tools to be embedded into Tistory blog posts via code insertion.

## Technical Requirements
- **Format**: Single-file HTML (HTML + Inline CSS + Inline JS).
  - Use an IIFE `(function(){ ... })();` for JavaScript to prevent global scope pollution.
  - Wrap the entire tool in a unique ID container (e.g., `<div id="tool-name">`).
  - **Dynamic Loading**: If using heavy libraries (e.g., `jsPDF`, `ffmpeg.wasm`), load them dynamically via JS only when the tool is used.
- **CSS Scoping**:
  - All CSS rules **MUST** be scoped to the unique container ID (e.g., `#tool-name .btn`).
  - Use scoped CSS variables for theming (e.g., `#tool-name { --bg: #1e1e1e; }`).
- **Responsiveness**: Mobile-first or responsive design using `flex` or `grid`.

## Design Aesthetics
- **Theme**: Dark Mode (Default).
- **Color Palette** (Lumora Dark Theme):
  - Background: `#1e1e1e` (Main), `#262626` (Cards/Panels).
  - Border: `#3a3a3a`.
  - Text: `#e8eaed` (Primary), `#9aa0a6` (Secondary/Muted).
  - Accent: `#7aa2ff` (Soft Blue) for primary actions and highlights.
  - Hover States: Slight brightness increase or transform (e.g., `translateY(-1px)`).
- **Components**:
  - **Cards**: `border-radius: 16px`, `box-shadow: 0 8px 24px rgba(0,0,0,.35)`.
  - **Buttons**: Rounded corners (`10px`), subtle transitions.
  - **Inputs**: Dark background (`#1f1f1f`), rounded corners (`8px`).

## Directory Structure
- `converters/[tool-name]/index.html`: The main tool file.

## Workflow
1. Create a directory for the new tool.
2. Develop `index.html` following the scoped style.
3. Test locally.
4. Final output should be copy-paste ready for Tistory's HTML block.
