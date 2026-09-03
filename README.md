# Little Kickers Football Kits — website & installable app

## What's in here
- `index.html` — the whole site (one file, easy to edit)
- `manifest.json` — makes the site installable as an app on phones
- `service-worker.js` — lets it work offline once installed, don't need to touch this
- `icons/` — placeholder app icon (green badge, "LK") — swap these for a real logo later

## Editing your kits
Open `index.html` and search for `id="kit-grid"`. Each kit is one block like this:

```html
<div class="kit-card">
  <div class="kit-shirt"><span class="num">10</span></div>
  <div class="kit-body">
    <div class="name">Kit name — e.g. Home 25/26</div>
    <div class="meta">Sizes: Kids 3-13, Adult S-XXL</div>
    <div class="row">
      <span class="price">£XX</span>
      <a class="order-link" href="#contact">Order →</a>
    </div>
  </div>
</div>
```

To add a kit: copy one whole block (from `<div class="kit-card">` to its closing `</div>`) and paste it in the list, then change the name, sizes, price and the number shown on the shirt graphic. To remove a kit, delete its block. There's no limit — the grid reflows automatically.

If you want a real photo instead of the plain shirt/number graphic, replace:
```html
<div class="kit-shirt"><span class="num">10</span></div>
```
with:
```html
<div class="kit-shirt" style="background:none;">
  <img src="kits/your-photo.jpg" alt="Kit name" style="width:100%;height:100%;object-fit:cover;">
</div>
```
and put the photo file in a `kits/` folder next to `index.html`.

## Contact section
Find `id="contact"` near the bottom and update the email link (currently a placeholder) with a real `mailto:` address if you want one, e.g.:
```html
<a href="mailto:you@example.com">
```

## Hosting it (so it can be installed as an app)
The "Add to home screen" install prompt only works once the site is served over `https://` — it won't trigger from a file opened straight off your computer. Since you already run Gellings' site on GitHub Pages, the easiest route is the same thing again:

1. Create a new GitHub repo (e.g. `little-kickers-kits`)
2. Upload all the files in this folder, keeping the folder structure (`icons/` included)
3. In the repo's Settings → Pages, set it to deploy from the main branch
4. Your site will be live at `https://<your-username>.github.io/little-kickers-kits/`

Once it's live, visiting the link on a phone will show an "Install" prompt (Android/Chrome) or you can use Share → "Add to Home Screen" (iPhone/Safari) to add it as an app icon.

## Note on branding
The design avoids using any official club crests or brand logos (Nike/Adidas/etc.) since those are trademarked — it uses plain shirt-number graphics instead. If you want real kit photos, use your own product photos rather than pulling official team logos/artwork onto the page.
