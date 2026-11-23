# How heavy is that money? · ¿Cuánto pesa esa plata?

Type one of those huge amounts from the news and see it as physical cash: kilos of banknotes, briefcases, stacks taller than buildings, and elephants on a scale.

Escribí una de esas cifras enormes que salen en las noticias y mirala como plata física: kilos de billetes, maletines, pilas más altas que edificios y elefantes en una balanza.

**Live:** https://fpradomacat.github.io/how-heavy-is-that-money/

## Features

- One input, one currency picker: USD, EUR, ARS, GBP, MXN and BRL
- Understands `183,000,340`, `2.5 million`, `900k`, `1kk`, `1kkk`, `1.2 billion`, `183.000.340`, `2,5 millones` and `3 billones`
- Pick the banknote denomination; the result changes a lot with it
- FAQ answering common searches (how much does $1 million weigh, etc.)
- Weight, volume, stack height, length, area, counting time and per-person split (by the currency's own country), each matched to a real-world object
- English (default) and Spanish, remembered between visits
- **Share:** generates a PNG card (post 4:5, story 9:16, link 1.91:1) with the native share sheet on mobile, plus a link that reopens the same amount (`?a=183000340&c=USD&d=100&l=en`)
- Open Graph / Twitter tags with a preview image (`og-image.jpg`), so pasted links show a card in WhatsApp, X, LinkedIn, etc.
- Light and dark mode, responsive, respects `prefers-reduced-motion`

## How the weight is calculated

`banknotes = amount ÷ denomination` and `weight = banknotes × weight per note`.

- **USD:** exact. Every US note weighs 1 g and measures 156 × 66.3 mm (Bureau of Engraving and Printing).
- **EUR, ARS, MXN and BRL:** official sizes from each central bank. Weights are commonly cited values, or are estimated from the note's area and typical banknote paper (≈97 g/m²).
- **GBP:** estimated from the Bank of England's 0.85 g £10 polymer note.

Comparisons are approximate. The point is to grasp the scale, not to appraise.

## Tech

Plain HTML, CSS and vanilla JavaScript in a single `index.html`. There are no dependencies and no build step, and the illustrations are inline SVG.

```bash
# run locally
open index.html        # or: npx serve .
```

## Deploy

GitHub Pages → Settings → Pages → Deploy from branch → `master` / `root`.

## SEO

- Static English text in the HTML, a FAQ section, `canonical` + `hreflang` (EN / ES via `?l=es`) and JSON-LD (`WebApplication` + `FAQPage`)
- `sitemap.xml`, to submit in Google Search Console
- Open Graph / Twitter image: `og-image.jpg` (1200×630, ~50 KB, small enough for WhatsApp previews)

## Author

Made by Fede · Instagram [@soypradito](https://instagram.com/soypradito)

If it helped you, you can [buy me a coffee](https://buymeacoffee.com/soypradito) ☕

## License

MIT
