# Kit photos go here

Drop your kit photos in this folder (e.g. `home-kit.jpg`, `away-kit.jpg`).

Then in `index.html`, for the kit you want to show a real photo for, replace:

    <div class="kit-shirt"><span class="num">10</span></div>

with:

    <div class="kit-shirt" style="background:none;">
      <img src="kits/home-kit.jpg" alt="Kit name" style="width:100%;height:100%;object-fit:cover;">
    </div>

Use your own product photos rather than official team/brand imagery.

Tip: square-ish photos (roughly 1:1) will look best in the card.
