# Changelog

## Unreleased

- The web shell saves the picture: a button in the control bar and F9 download the current frame as a PNG at the program's own resolution, without scaling or CRT filter, named after the window title and the time.

## 0.1.23

- The program decides how the web shell shows it. A raylib program that sets `FLAG_WINDOW_RESIZABLE` runs at native resolution: the display fills the free space and the canvas follows it, one canvas pixel per CSS pixel, so nothing is enlarged into big pixels. Programs with a fixed resolution are scaled as before, with sharp pixels, or smoothly when they set `window.PIXELRAM_SCALING = 'smooth'`.

- Add a first-pass optional OpenCrystalCaves / Crystal Caves web port with a bundled shareware fallback
- Add `clear()` for indexed framebuffers and `clear_rgb()` for direct-color framebuffers
- Use `clear()` in the animation example and document the clear → draw → present frame pattern

## 0.1.0

Initial PixelRAM release.

- Indexed 8-bit, RGB565, RGB24 and RGBA32 software framebuffers
- Direct framebuffer access
- `set_pixel()` and `get_pixel()` helpers with safe out-of-bounds behavior
- RGB pixel helpers
- 88 built-in palettes shared with Pixelflow Canvas
- Keyboard transition queue suitable for game-engine ports
- Absolute and relative mouse input
- Native and WebAssembly-aware timing and presentation
- Fire demo derived from the Pixelflow Canvas teaching example
