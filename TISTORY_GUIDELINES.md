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
  - Use scoped CSS variables for theming.

## Design Aesthetics (Lumora Dark Theme)
All tools must adhere to the `img-compressor` reference design.

### Color Palette (CSS Variables)
```css
#tool-id {
    --bg-main: #1e1e1e;       /* Main Background */
    --bg-card: #262626;       /* Card/Panel Background */
    --bg-input: #2a2a2a;      /* Input/Select Background */
    --border: #3a3a3a;        /* Border Color */
    --text-primary: #e8eaed;  /* Main Text */
    --text-secondary: #9aa0a6;/* Subtext/Muted */
    --accent: #a78bfa;        /* Primary Accent (Purple) */
    --accent-hover: #c4b5fd;  /* Accent Hover */
    --success: #4ade80;       /* Success State */
    --danger: #ff7a94;        /* Error/Danger State */
    --shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
    --radius-card: 16px;
    --radius-input: 8px;
    --font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, Roboto, sans-serif;
}
```

### Core Components
1.  **Container**: `max-width: 600px~800px`, `border-radius: 16px`, `box-shadow` included.
2.  **Header**:
    -   Title `h2` with optional badge (background: `rgba(167, 139, 250, 0.15)`, color: `--accent`).
    -   Subtext description.
3.  **Inputs**:
    -   Dark background (`#2a2a2a`), Border (`#444`).
    -   Focus state: `border-color: var(--accent)`.
    -   **Custom Select**: Use custom-built dropdowns instead of native `<select>` for better styling and height control.
4.  **Buttons**:
    -   Primary: Background `--accent`, Text Dark.
    -   Secondary: Transparent, Border `--border`.
5.  **Scrollbars**:
    -   Slim (8px), dark track, thumb hover update.

### Usage Guide (Mandatory)
Every tool must include a "How to Use" section at the bottom.
-   **Title**: `🛠️ 사용 방법` (16px, Bold)
-   **Steps**: List of steps with number badges.
    -   Number Badge: Circle, background `rgba(167, 139, 250, 0.2)`, text `--accent`.
    -   Content: Title (strong) + description.
    -   Hover Effect: Light border/box glow.

## Directory Structure
- `converters/[tool-name]/index.html`: The main tool file.

## Workflow
1. Create a directory for the new tool.
2. Develop `index.html` following the scoped style and variable naming.
3. Test locally.
4. Final output should be copy-paste ready for Tistory's HTML block.
