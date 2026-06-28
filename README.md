# BlackFin

A personal Jellyfin theme, forked from
[NeutralFin](https://github.com/KartoffelChipss/NeutralFin) by KartoffelChipss,
which is itself a fork of
[ElegantFin](https://github.com/lscambo13/ElegantFin) by lscambo13.

Sleek black & grey color scheme. This repo exists so I can make the look my own
while keeping the same general feel.

## Files

| File | Purpose |
| --- | --- |
| `theme/blackfin.css` | The working, human-readable theme. **Edit this one.** |
| `theme/blackfin-minified.css` | Generated minified build (run `npm run build`). |
| `src/neutralfin.original.css` | Pristine upstream copy, kept for reference / diffing. |
| `LICENSE` | GNU GPL-2.0 (inherited from upstream). |

## Install

In Jellyfin, paste **one** of the following into the Custom CSS box.

**Server-side** (applies to everyone): Dashboard → General → Branding → Custom CSS
**Client-side** (just you): Settings → Display → Custom CSS

### Option A — paste the CSS directly

Open `theme/blackfin.css`, copy the whole file, and paste it into the Custom
CSS box. Simplest, no hosting needed.

### Option B — import from a URL

Host `theme/blackfin.css` (or the minified build) somewhere public — e.g. push
this repo to GitHub and use jsDelivr — then import it:

```css
@import url('https://cdn.jsdelivr.net/gh/<your-user>/<your-repo>@latest/theme/blackfin-minified.css');
```

> For the original upstream theme the import is:
> `@import url('https://cdn.jsdelivr.net/gh/KartoffelChipss/NeutralFin@latest/theme/neutralfin-minified.css');`

For best results, enable **backdrops** in your Jellyfin display settings.

## Customizing

All the quick knobs live in a `BlackFin custom overrides` block near the top of
the `:root { ... }` selector in `theme/blackfin.css`. Set your values there
instead of hunting through the rest of the file. Common ones:

```css
:root {
    --activeColor: rgb(0, 160, 220);     /* focus / hover accent */
    --uiAccentColor: rgb(0, 160, 220);   /* links & highlights   */
    --btnMiniPlayColor: rgb(220, 40, 90);/* play button          */
    --textColor: rgb(245, 245, 245);     /* primary text         */
}
```

## Build (minified)

```bash
npm install
npm run build
```

This generates `theme/blackfin-minified.css` from `theme/blackfin.css`.

## License & credits

BlackFin is a modified version of NeutralFin (KartoffelChipss), which is a
modified version of ElegantFin (lscambo13). It remains licensed under the
**GNU General Public License v2.0** — see [`LICENSE`](./LICENSE). You are free
to use, modify, and redistribute under the same terms.

> Not affiliated with, endorsed by, or associated with the Jellyfin project.
