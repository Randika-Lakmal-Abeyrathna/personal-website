# randika.me

Source for my personal website, **[randika.me](https://randika.me)**: who I am, where I've worked, and how
to get in touch, plus a couple of interactive extras.

**No framework and no build step.** Everything is plain HTML, CSS and JavaScript, with fonts and libraries
self-hosted, so the site loads fast and will still work years from now.

## What's on it

| Page | What it is |
|---|---|
| [`index.html`](index.html) | The main site: intro, experience, how my team uses AI, skills, education and contact. Includes my CV as a PDF. |
| `index.html#sys` | **A live system demo.** Requests flow from users through an API gateway to three Spring Boot instances and an Oracle database. You can trigger a traffic spike, crash a server or fix a slow query, and watch throughput, tail latency and errors change. |
| [`world.html`](world.html) | **Career Street**, a small 3D town built with three.js. Walk around, and every building is a place I've worked or studied. |

## Built with

- **HTML, CSS and vanilla JavaScript** (two self-contained pages)
- **three.js** for Career Street, vendored in `assets/vendor/three` and loaded through an import map
- **Self-hosted fonts:** Newsreader, IBM Plex Sans and IBM Plex Mono
- `IntersectionObserver` for scroll animations; light and dark themes from `prefers-color-scheme`
- **Accessibility and performance:** respects `prefers-reduced-motion`, preloads key fonts, and has been
  through an accessibility audit
- **SEO:** canonical URLs, Open Graph tags, JSON-LD structured data, `sitemap.xml` and `robots.txt`

## Running locally

There's nothing to install. Serve the folder with any static server (`world.html` uses ES modules, so
opening the file directly won't work):

```bash
npx serve .
# or
python -m http.server 8000
```

## Credits

3D models by [Kenney](https://kenney.nl) (CC0), sky HDRI from [Poly Haven](https://polyhaven.com) (CC0)
and the water normal map from the three.js examples (MIT). Full details are in
[`assets/CREDITS.txt`](assets/CREDITS.txt).
