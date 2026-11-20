# 苏轼 · 赤壁赋

苏轼《赤壁赋》（台北故宫博物院藏） — a narrated deep-zoom reading, as a static page (in Chinese).

Su Shi's Ode on the Red Cliff (National Palace Museum, Taipei): Wen Zhengming's 36 characters at the head, Su Shi's 51 columns each with its modern reading, his postscript and the seals.

Live: https://youdata.github.io/su-shi-chibi/

The image pyramid is a tile folder (`chibi/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/su-shi-chibi/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → su-shi-chibi.json
rx export su-shi-chibi.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/su-shi-chibi --yes
```
