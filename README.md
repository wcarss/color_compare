# Color Compare

A small, single-page tool for comparing two colors side by side. Pick colors with the built-in picker or type any CSS color; the URL updates so you can share or bookmark a pair. You can also click the die in the middle to see a random pair!

![screenshot of the app](images/screenshot.png)

This project was mostly created by Opus 4.6 at my direction.

## Run it

Serve the folder with any static server, then open in a browser. For example,

```bash
python -m http.server
# → http://localhost:8000
```

## Features

- Two panels (left/right on desktop, top/bottom on mobile) with independent color inputs
- Color picker opens from the text field; type hex, names, `rgb()`, `hsl()`, etc.
- URL encodes both colors (e.g. `?left=bda5d8&right=1ee896`) for sharing
- Random color button; copy-to-clipboard per side
- Uses [hdr-color-input](https://www.npmjs.com/package/hdr-color-input) for the picker

## Tech

Plain HTML, CSS, and JavaScript, using [argyleink](https://github.com/argyleink)'s [css-color-component](https://github.com/argyleink/css-color-component) library instead of the native browser color input, because a) the browser input varies widely across browsers and OS's and b) on Chrome and Firefox it seemed to eat keydowns whenever it was open.
