# GangForge — DTF Gang Sheet Builder

A free, browser-based tool for laying out **DTF (direct-to-film) gang sheets**. Drop in your artwork, set quantities, and GangForge automatically nests everything onto roll-width sheets at full print resolution — then exports print-ready PNGs.

No installation, no account, no internet required after the page loads. Everything runs locally in your browser, so your artwork never leaves your computer.

**▶ Use it now:** _add your GitHub Pages link here, e.g._ `https://charmady33.github.io/gangforge/`

If GangForge saves you time, tips are appreciated: **https://www.paypal.com/paypalme/clarkmccoy33** 💛

---

## Features

- **Automatic nesting** — packs your designs onto the sheet for minimum length, rolling onto extra sheets when needed.
- **True-shape interlock** — nests by each design's real silhouette (not just its bounding box) so irregular art fits tighter.
- **Rotation** — off, 90°, 45°, 30°, 15°, or free any-angle.
- **Auto-expand gap** — you set a *minimum* gap; GangForge widens it where there's room, without losing any images or adding sheets.
- **Auto-fill** — flag a design to fill leftover space with extra copies.
- **Quantities** — set how many of each design you need.
- **Add-design dialog** — name art, set the exact print size, and use the built-in **shirt placement guide** (Adult S–3XL and Youth/Kids sizes for full front, full back, left chest, and neck label).
- **Duplicate for a different size** — make a second design from any piece at a new size.
- **Manual editing** — click a piece on the sheet to select it, then drag to move or use the handle to rotate. A warning fires if a move breaks your minimum gap.
- **Per-sheet length** — each sheet can be Max length, Fit to art, or a Custom length.
- **Inches or centimeters** — switch units anytime.
- **Wasted-space readout** — shows how tightly the current layout is packed.
- **Full-resolution export** — single sheet exports as PNG, multiple sheets as a ZIP, all at the chosen DPI with correct physical size embedded.
- **Save / open jobs** — save a layout and reopen it later; export/import job files to move them between computers.

---

## How to use it

1. Open the app (your GitHub Pages link, or open `index.html` locally in a browser).
2. **Sheet Setup** — pick your roll width (22", 23", etc.), max sheet length, DPI, and units.
3. **Add Designs** — drop in PNG/JPEG art. In the dialog, name it, set the printed size (or click a spot on the shirt guide), and set the quantity.
4. Hit **Auto-nest**.
5. Tweak pieces by hand if you like, set each sheet's length, then click **Create Gang Sheet(s)** to export.

> **Tip:** Transparent PNGs give the best results and let true-shape interlock work properly.

---

## Where files are saved

- **Saved jobs (browser):** stored inside your browser on that computer. Use **Export Gang Forge** to save a `.gangjob.json` file you can back up or move, and **Import Gang Forge…** to load it.
- **Saved jobs (desktop app):** saved as `.gangjob.json` files in **Documents → GangForge Jobs**.
- **Exported gang sheets:** download to your browser's Downloads folder (PNG or ZIP). The desktop app asks where to save.

---

## Run it as a desktop app (optional)

The repo includes `gangforge-desktop.zip`, an Electron wrapper that runs GangForge as a native Windows/Mac/Linux app with file-based job saving.

1. Install [Node.js](https://nodejs.org) (LTS).
2. Unzip `gangforge-desktop.zip` and open a terminal in the `gangforge-desktop` folder.
3. Run:
   ```bash
   npm install
   npm run dist
   ```
4. The installer/app appears in the `dist/` folder.

> **Windows note:** if the build fails with a "required privilege is not held" / symlink error, either run the terminal **as Administrator** or turn on **Developer Mode** (Settings → Privacy & security → For developers), then delete `%LOCALAPPDATA%\electron-builder\Cache\winCodeSign` and build again.

---

## A note on nesting

GangForge uses a fast **skyline packer**: it stacks pieces onto the top profile of the layout and nestles shapes into that surface. It does a great job for most gang sheets, but it does not do full jigsaw-style nesting (tucking pieces under overhangs or into enclosed pockets). For irregular art, expect some unavoidable empty film between shapes — that's normal.

---

## License

[MIT](LICENSE) — free to use, modify, and share. Built by Clark McCoy.
