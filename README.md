# UIX Icons

13,491 free icons on a 24 px grid, in three styles, MIT licensed. Browse and search them at [icons.pagestro.com](https://icons.pagestro.com).

| Style | Folder | Font |
|---|---|---|
| Regular Rounded | `svg/stroke-regular-rounded/` | `uix-icons-regular` |
| Regular Sharp | `svg/stroke-regular-sharp/` | `uix-icons-sharp` |
| Solid | `svg/solid/` | `uix-icons-solid` |

Every SVG uses `viewBox="0 0 24 24"` and `currentColor`, so it takes the text colour of whatever it sits in.

## Install

```sh
npm install @uix-ui/icons          # SVG files, sprites, search data
npm install @uix-ui/icons-react    # React components
```

## CDN

Single SVG files from jsDelivr, served from the npm package:

```html
<img src="https://cdn.jsdelivr.net/npm/@uix-ui/icons/svg/stroke-regular-rounded/home.svg" width="24" height="24" alt="Home">
```

Or straight from this repository, pinned to a release tag:

```html
<img src="https://cdn.jsdelivr.net/gh/mdrakibshekh/uix-icons@v0.1.0/svg/solid/home.svg" width="24" height="24" alt="Home">
```

## Icon font

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/mdrakibshekh/uix-icons@v0.1.0/css/uix-icons.css">

<i class="uix uix-home"></i>             <!-- Regular Rounded -->
<i class="uix uix-sharp uix-home"></i>   <!-- Regular Sharp -->
<i class="uix uix-solid uix-home"></i>   <!-- Solid -->
```

`css/uix-icons.css` loads all three fonts; each font is only downloaded when a page uses it. If you need a single style, link `css/uix-icons-regular.css`, `css/uix-icons-sharp.css` or `css/uix-icons-solid.css` instead and use `class="uix uix-home"`. The fonts come as woff2, woff and ttf in `fonts/`. Codepoints are in `codepoints.json` and stay the same from one release to the next. Size the icons with `font-size` and colour them with `color`.

From the next npm release the same files are also at `https://cdn.jsdelivr.net/npm/@uix-ui/icons/css/uix-icons.css`.

## SVG sprite

```html
<svg width="24" height="24"><use href="sprite/sprite-stroke-regular-rounded.svg#home"/></svg>
```

## React

```jsx
import { Home, Search } from '@uix-ui/icons-react/stroke-regular-rounded';
import { Home as HomeSolid } from '@uix-ui/icons-react/solid';

<Home width={20} height={20} className="text-gray-700" />
```

Each style is its own entry point, and unused icons are tree-shaken away.

## Metadata

`icons.json` lists every icon with its category, tags and synonyms, which is handy for building your own search.

## Licence

MIT, see [LICENSE](LICENSE). The UIX Icons name and logo are not covered by the licence.
