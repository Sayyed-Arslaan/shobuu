## shobuu — Personal Photo Gallery

A lightweight, responsive static photo gallery with a custom lightbox, captions, animated effects, and optional background music. Designed as a personal/romantic gallery (original author: SayyedArslaan) — easy to host anywhere that serves static files.

---

## Highlights

- Responsive grid gallery that adapts to any viewport.
- Click an image to open a polished lightbox with caption support and keyboard Escape-to-close.
- Captions are configurable in JavaScript (friendly, personal captions included).
- Cute animated effects: falling hearts, hover zoom, gradient borders and subtle motion.
- Optional looping background music (drop an MP3 named `music.mp3` into the root to enable).
- MIT licensed — free to reuse and modify.

## Demo / Preview

Open `index.html` in any modern browser. For best results serve the folder via a simple static server (see "Local preview" below).

If the demo images are missing, add your images to the `images/` folder and follow the naming guidance below.

## What's in this repo

- `index.html` — gallery page and markup.
- `style.css` — main styles and animations.
- `lightbox.css` — lightbox-specific styles.
- `script.js` — gallery builder, captions mapping, falling hearts, and lightbox interaction.
- `lightbox.js` — helper for lightbox open/close and keyboard support.
- `images/` — image assets (project expects images named by id like `10002.jpg`).
- `LICENSE` — MIT license.

## Installation / Local preview

You can simply open `index.html` in a browser. For a better, more accurate experience (audio and some browser behaviors), use a local static server.

Examples (run from the project root):

PowerShell (Windows)

```powershell
# Python 3
python -m http.server 5500

# or using Node (if available)
npx http-server -p 5500
```

Then open http://localhost:5500 in your browser.

## Usage & customization

1. Images
	- Drop your images into the `images/` folder.
	- The default `script.js` currently generates image filenames from `10002.jpg` up to `10062.jpg`. You can change the range in `script.js` (the for-loop) to match your filenames.

2. Captions
	- Captions are stored in the `captions` object inside `script.js`. Edit or replace those strings to match your needs.

3. Background music
	- Add a `music.mp3` file into the project root to enable background audio. Browsers may block autoplay; the script attempts to play on first user click.

4. Styles & theme
	- Tweak `style.css` and `lightbox.css` to adjust colors, spacing, animations, or fonts. The project already includes Google Fonts in `index.html` — swap or remove as desired.

5. Lightbox behavior
	- `lightbox.js` contains simple open/close functions and an Escape key handler. Extend it for next/previous navigation if you want arrow controls.

## Contract (quick)

- Input: a folder of images and optional `music.mp3`.
- Output: a responsive gallery page with clickable images, captions, and a lightbox overlay.
- Error modes: missing images will appear broken — ensure filenames/range in `script.js` match the files in `images/`.

## Edge cases to consider

- Empty `images/` folder: the gallery will be empty; consider adding a friendly fallback message.
- Large image files: optimize images for web (resize/compress) to improve load times.
- Autoplay blocked: modern browsers often block autoplay; the gallery plays audio on first user interaction.

## Contributing

Contributions are welcome. Small fixes, accessibility improvements, and performance optimizations are especially helpful. Create a PR or open an issue describing the change.

Guidelines:

- Keep changes focused and documented.
- Add small reproducible tests/examples if behavior changes.

## License

This project is licensed under the MIT License — see the `LICENSE` file.

## Author

SayyedArslaan

Contact / Questions: open an issue in this repository.

---

If you want, I can:

- Add usage screenshots or a short GIF preview (if you provide images to include).
- Add a simple script to auto-detect images in the `images/` folder instead of relying on numeric ranges.
- Improve accessibility (ARIA labels, keyboard navigation for the lightbox).

Tell me which of those you'd like next and I'll implement it.
