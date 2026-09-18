# zentium-dev.github.io

Portfolio site for **ZentiumDev**. The repo is named after the org, so GitHub
Pages serves it at the org root:

    https://zentium-dev.github.io/

## Publishing

Settings → Pages → Source: **Deploy from a branch** → `main` / `root`.
Nothing to build — HTML files plus images.

## Structure

    index.html                        landing page, lists the case studies
    projects/lottery-sri-lanka.html   Lanka Draw case study
    projects/vaxaware-global.html     VaxAware Global case study
    assets/lottery-*.jpg              810x1440, ~80 KB each
    assets/vax-*.jpg                  540x960, ~75 KB each

Images are downscaled JPEGs, not the original PNGs. The whole site is around
1 MB, which matters — most of the audience for this page is on Sri Lankan
mobile data.

## Adding another project

Copy an existing page to `projects/<name>.html`, keep the token block at the
top of the `<style>`, and add a card to the `.projects` grid in `index.html`.

The palette, the perforated dividers and the monospace spec sheet are what tie
the pages together, so they stay the same whatever the app's own branding is.
Each page gets **one** signature element of its own, in the hero, sharing the
`.scan` shape: an input resolving into a verdict. Lanka Draw scans a ticket
serial into a prize; VaxAware applies a schedule offset to a date of birth.
That one device is where a case study earns its personality — everything else
is house style.

## Writing a case study

The structure that works, in order: hero with the signature element, stack
spec sheet, an architecture walk-through, one code block showing the central
abstraction, then **problem cards**. The problem cards are the point. A list of
features says nothing a Play listing does not; a bug that only appeared in
production, and what it cost to find, is the part a reader cannot get anywhere
else.

## Notes

* No build step, no framework, no analytics. A case-study page that needs a
  toolchain is its own argument against the engineer who wrote it.
* Fonts load from Google Fonts. If you would rather not depend on that,
  self-host Archivo, Inter and IBM Plex Mono into `assets/fonts/`.
* Two disclaimers are on the pages deliberately and should stay: "not
  affiliated with NLB or DLB" on the Lanka Draw page, and "a scheduler and a
  record keeper, not medical advice" on the VaxAware page. Both repeat what the
  apps, their privacy policies and their Play listings already say.
