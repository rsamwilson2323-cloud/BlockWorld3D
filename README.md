# 🧱 BlockWorld 3D Builder

> **A creative, browser-based 3D voxel world builder powered by HTML, CSS, JavaScript, and Three.js.**

BlockWorld 3D Builder lets you create and customize a miniature block world directly in your web browser. Place blocks, remove them, repaint them with different colors, explore your creation from different angles, and export your world to a JSON file.

**No game engine installation. No backend server. Just your browser and your creativity.**

---

## ✨ Features

- 🧱 **3D Block Building** — Place blocks on the ground or beside existing blocks.
- 🎨 **12-Color Palette** — Choose from a range of colorful block materials.
- 🗑️ **Remove Blocks** — Delete individual blocks from your world.
- 🖌️ **Repaint Blocks** — Change the color of existing blocks.
- 🔎 **Inspect Tool** — View a selected block's color and coordinates.
- 🌎 **Demo World** — Load a sample world to explore the building features.
- ↶ **Undo** — Reverse your recent building, removal, or repaint actions.
- 🖱️ **Orbit Camera** — Drag to rotate the camera around your world.
- 🔍 **Zoom Controls** — Use the mouse wheel to zoom in and out.
- ▦ **Grid Toggle** — Show or hide the building grid.
- 🌤️ **Shadow Toggle** — Enable or disable block shadows.
- 💾 **Export World** — Save your creation as a JSON file.
- 📂 **Import World** — Load a previously exported JSON world.
- 📊 **Live Statistics** — Track the number of blocks and colors used.
- 🌑 **Modern Dark UI** — Dark interface with purple accents and a clean editor layout.
- 📱 **Responsive Layout** — Adapts to different screen sizes.

---

## 🖥️ User Interface

BlockWorld provides a 3D viewport alongside building tools, a color palette, world statistics, and settings.

```text
┌───────────────────────────────────────────────────────────┐
│  🧱 BLOCKWORLD 3D                         ↶ Undo  ↓ Export│
├───────────────┬───────────────────────────┬───────────────┤
│ BUILD TOOLS   │                           │ WORLD SETTINGS│
│               │                           │               │
│ ▦ Place       │       3D WORLD            │ Blocks:  24   │
│ ⌫ Remove      │                           │ Colors:   4   │
│ ◈ Repaint     │     🧱  🧱  🧱             │               │
│ ⌖ Inspect     │   🧱  🧱  🧱  🧱           │ Selected block│
│               │                           │ Grid / Shadow │
│ COLOR PALETTE │                           │               │
│ 🟩 🟦 🟪 🟧   │                           │ CONTROLS      │
│ 🟥 🟨 🟦 ⬜   │                           │ Import JSON   │
└───────────────┴───────────────────────────┴───────────────┘
```

*The diagram is a simplified illustration of the interface.*

---

# 🚀 Quick Start

## 1. Clone the Repository

```bash
git clone https://github.com/rsamwilson2323-cloud/BlockWorld3D.git
```

## 2. Enter the Project Folder

```bash
cd BlockWorld3D
```

## 3. Run BlockWorld

The main application is:

```text
index.html
```

Try opening it in a modern browser. If the browser blocks JavaScript modules when opening the file directly, start a local server from the project folder:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

Three.js is loaded from jsDelivr, so an internet connection is required to load the 3D engine.

### Recommended Browsers

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Other modern browsers with WebGL and ES module support

---

# 🧰 Building Tools

## 🧱 1. Place Block

Select **Place block**, choose a color, and click in the 3D world.

- Click empty ground to place a block on the ground grid.
- Click an existing block's face to place a block next to it.
- The editor prevents placing two blocks in the same grid position.
- Building is limited to the editor's defined world area.

## 🗑️ 2. Remove Block

Select **Remove**, then click a block to delete it from the world.

## 🎨 3. Repaint Block

Select **Repaint**, choose a color from the palette, and click an existing block to change its color.

## 🔎 4. Inspect Block

Select **Inspect**, then click a block to view its color and grid coordinates.

---

# 🎨 Color Palette

Choose from 12 built-in colors:

| Color | Hex |
|---|---|
| Meadow Green | `#72D6A1` |
| Sky Blue | `#65BAFF` |
| Royal Purple | `#9A83FF` |
| Sunset Orange | `#FF9B68` |
| Rose Pink | `#FF7EAA` |
| Lemon | `#F5D76E` |
| Ocean Teal | `#38C9C2` |
| Cloud White | `#E9EFFF` |
| Stone | `#8996AD` |
| Cherry Red | `#F05D72` |
| Wood | `#AD7955` |
| Night | `#313C5B` |

The selected color is used when placing new blocks or repainting existing blocks.

---

# 🖱️ Camera & Keyboard Controls

| Input | Action |
|---|---|
| Drag with mouse | Rotate the camera around the world |
| Mouse wheel | Zoom in or out |
| Click | Use the selected building tool |
| `Q` | Rotate the view left |
| `E` | Rotate the view right |
| `Esc` | Switch back to Place Block |
| `Ctrl + Z` / `Cmd + Z` | Undo the last supported action |
| Reset View button | Return the camera to its default view |

---

# 🌎 Demo World

Use **Build demo** to generate a sample block world. It includes a colorful ground area and raised structures, giving you a quick way to explore the editor before creating your own design.

Use **Clear world** when you want to start fresh. The app asks for confirmation before clearing the blocks.

---

# 💾 Export & Import Worlds

## Export World

Click **Export world** to download your current creation as a `.json` file. The export contains the world name and each block's position and color.

Example structure:

```json
{
  "app": "BlockWorld 3D Builder",
  "version": 1,
  "name": "My Little World",
  "blocks": [
    {
      "x": 0,
      "y": 0,
      "z": 0,
      "color": "#72d6a1"
    }
  ]
}
```

## Import World

1. Click **Import world JSON**.
2. Select a JSON file previously exported from BlockWorld.
3. The editor loads valid blocks and updates the world name and statistics.

**Tip:** Keep a copy of your exported JSON file as a backup of your creation.

---

# ⚙️ World Settings

- **World name** — Give your creation a custom name.
- **Show grid** — Toggle the visible building grid.
- **Soft shadows** — Toggle shadows for the directional light and blocks.
- **Blocks placed** — See the total number of blocks currently in the world.
- **Colors used** — See how many different block colors are in use.
- **Reset view** — Restore the camera's default position.

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| 🌐 HTML5 | Application structure |
| 🎨 CSS3 | Dark theme, layout, and responsive styling |
| ⚡ JavaScript (ES Modules) | Building tools and application logic |
| 🧊 Three.js | 3D scene, camera, lighting, geometry, and rendering |
| 🖱️ Pointer & Keyboard Events | Camera controls and block interactions |
| 📦 JSON | World export and import |
| 💾 Blob & File APIs | Downloading and loading world files |
| 🌐 WebGL | Browser-based 3D rendering |

---

# 📂 Project Structure

```text
BlockWorld3D/
│
├── 📄 index.html
└── 📄 README.md
```

### `index.html`

Contains the main application, including:

- HTML interface
- CSS styling
- Three.js scene and renderer
- Lighting, camera, floor, and grid
- Block placement, removal, repainting, and inspection
- Color palette and world statistics
- Undo, demo world, and clear-world actions
- JSON import and export
- Camera, keyboard, and responsive controls

### `README.md`

Project overview, setup instructions, features, controls, and usage guide.

---

# 🏗️ How It Works

BlockWorld represents the world as a collection of colored cubes positioned on a 3D grid.

```text
User Action
    ↓
Selected Building Tool
    ↓
Raycasting Detects Clicked Surface
    ↓
Calculate Block Grid Position
    ↓
Update 3D Scene
    ↓
Refresh World Statistics
```

Three.js renders the scene in the browser. Raycasting helps identify which block or ground surface the user clicked, while each block stores its grid coordinates and color.

---

# 🔐 Privacy & Data

- The application does not require a project-specific backend or database.
- World export creates a JSON file in the browser for the user to download.
- Import reads the selected JSON file in the browser.
- Three.js is loaded from a third-party CDN, so an internet connection is needed to load the 3D library.
- Avoid importing JSON files from untrusted sources.

---

# 💻 Requirements

- A modern desktop or mobile browser
- WebGL support enabled
- Internet access to load Three.js from jsDelivr
- Optional: Python, only if you need to start the simple local HTTP server

No game engine installation or database setup is required.

---

# 🔮 Future Improvements

Potential ideas for future versions:

```text
□ Custom block textures
□ More block shapes
□ Terrain generation
□ Trees, water, and landscape tools
□ Day/night cycle
□ First-person exploration mode
□ Keyboard-based movement
□ Copy and paste blocks
□ Multi-block selection
□ Drag-to-build mode
□ Undo/redo history panel
□ World thumbnails
□ Autosave and local storage
□ Mobile touch controls
□ Shareable world files
□ More advanced lighting and effects
```

*These are possible future enhancements, not features currently included.*

---

# 👨‍💻 Author

## Sam Wilson

**B.E. CSE — Artificial Intelligence & Machine Learning**

GitHub:  
https://github.com/rsamwilson2323-cloud

---

# ⭐ Repository

**BlockWorld3D**

https://github.com/rsamwilson2323-cloud/BlockWorld3D

If you enjoy the project, consider giving the repository a ⭐ on GitHub!

---

# 📜 License

No license information was provided with this README. Add a `LICENSE` file and update this section if you choose to distribute the project under a specific open-source license.

---

# 🚀 Quick Start

```bash
git clone https://github.com/rsamwilson2323-cloud/BlockWorld3D.git
cd BlockWorld3D
python -m http.server 8000
```

Open `http://localhost:8000` in your browser, choose a building tool, and start creating your own 3D world.

---

# 🧱 Build → 🎨 Customize → 🌎 Explore → 💾 Export

**Your world. Your blocks. Your creativity.**
