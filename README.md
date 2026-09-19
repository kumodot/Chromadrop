<p align="center">
  <a href="https://kumodot.github.io/Chromadrop/"><img src="og-image.png" alt="Chromadrop" width="820"></a>
</p>

<p align="center">
  <b>Pull color palettes from any image and copy the values straight into your 3D app.</b><br>
  Free, single HTML file, runs 100% in the browser. Nothing is uploaded.
</p>

<p align="center">
  <a href="https://kumodot.github.io/Chromadrop/"><b>▶ Open Chromadrop</b></a> ·
  <a href="https://ko-fi.com/msouza3d"><b>☕ Support Marcelo Souza</b></a>
</p>

---

![Chromadrop main view](docs/screenshot-app.jpg)

## Features (v0.8)

- **Smart pins**: auto extract (weighted k-means in CIELAB) drops numbered pins on each dominant color. Controls for max colors, min coverage % and "snap to flat" (exact colors for flat art). Sliders update live.
- **Edit pins freely**: drag any pin to resample, click empty space to add one, select and press `Del` to remove. Pins you add or move are kept when you re-extract. Adjustable sample radius and loupe.
- **Remove similar**: drops auto colors that are too close to each other or to your pins (adjustable ΔE).
- **Auto names**: every color gets a short, unique, single-word name (`sage`, `jaffa`, `trout`...) from the nearest match in OKLab. Edit a name to lock it; "Auto-name" refreshes all.
- **Click to copy**: HEX, RGB 0-255, sRGB 0-1, Linear 0-1, HSV. Wrap styles: plain, Python tuple, VEX `{}`, `c4d.Vector()`, GLSL `vec3()`.
- **Blocks view**: the image rebuilt with only your palette colors, with mosaic block size and a cleanup filter that eats small specks. Export as PNG.
- **Copy all**: HEX / RGB / sRGB / Linear lists, Python list, VEX `vector[]`, CSS vars, JSON.
- **Exports**: ASE (Adobe Swatch Exchange), GPL (GIMP / Krita / Inkscape), JSON, CSS.

## Share

![Chromadrop share window](docs/screenshot-share.jpg)

One window, five tabs:

- **PNG card**: image + palette strip or grid, names, HEX / RGB / Linear labels, dark or light theme. Download or copy straight into a chat.
- **Markdown**: table for GitHub, Notion, Obsidian.
- **Slack**: ready-to-paste message with an aligned value block.
- **Plain text**: works anywhere.
- **Link**: the palette lives in the URL, no upload. Whoever opens it can drop their own image and see it rebuilt with your palette in Blocks view.

## Run

- **Online**: <https://kumodot.github.io/Chromadrop/>
- **Local**: double-click `Run_Chromadrop.bat`, or open `Chromadrop_v0.8.html` in any modern browser. No install, no build.

Load images with Open, drag and drop, or `Ctrl+V`. Shortcuts: `E` extract, `B` blocks view, `Del` remove selected pin, `Esc` deselect.

## Notes on color space

sRGB 0-1 is the image value divided by 255. Linear 0-1 has the sRGB curve removed, which is what renderers use internally. If a 3D app's color field shows display values (most UI pickers do), use sRGB. If you type into a raw vector or parameter in a linear workflow, use Linear.

## Credits

Color names come from the [xkcd color survey](https://xkcd.com/color/rgb/) (CC0) and the [color-name-list](https://github.com/meodai/color-names) "short" list, Copyright (c) 2017 David Aerne, MIT License. Both filtered to short, single-word names.

---

<p align="center">
  Marcelo Souza / Kumodot.art - 2026 // <a href="https://instagram.com/msouza3d">@Msouza3d</a> · <a href="https://github.com/kumodot">GitHub</a><br>
  <a href="https://ko-fi.com/msouza3d">☕ Support Marcelo Souza on Ko-fi</a>
</p>
