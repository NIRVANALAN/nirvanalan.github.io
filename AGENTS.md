# Repo Notes

- Preserve original visible and commented content. Prefer commenting out old material over deleting it.
- Keep the homepage style simple and academic, close to Jon Barron / Shangchen Zhou rather than a heavily designed landing page.
- `data/bib/*.bib` is the source of truth for BibTeX. Do not replace it with large inline citation blobs.
- Keep section order aligned with the current homepage:
  1. profile
  2. about me
  3. news
  4. selected publications
  5. academic services
  6. invited talks
  7. visitor map
- `Academic Services` and `Invited Talks` must stay at the bottom, immediately before the visitor map.

# Publication Ordering

- There is no separate `Earlier Publications` section anymore. Older papers should be integrated into the main selected-publications area and classified with the same category/tag system.
- Selected publications are auto-sorted in `index.html` from `data-*` attributes on each `.publication` item.
- Selected publications also use `data-tags` for visible tag pills and top-of-section filtering.
- For `Preprint Papers`, use `data-sort-strategy="author-rank-year"` on the wrapper so papers sort by:
  1. `data-author-rank` ascending
  2. `data-year` descending
  3. `data-title` ascending
- For `Conference and Journal Papers`, use `data-sort-strategy="year-author-rank"` on the wrapper so papers sort by:
  1. `data-year` descending
  2. `data-month` descending (conference month, e.g. NeurIPS=12, ECCV=9, ICML=7, CVPR=6, ICLR=4; optional, defaults to 0)
  3. `data-author-rank` ascending
  4. `data-title` ascending
- When adding or editing a selected publication, always set:
  - `data-year`
  - `data-author-rank`
  - `data-title`
  - `data-tags` (exception: Magnifier has no tags on purpose and only shows under All)
- Current publication tags in use:
  - `preprints`
  - `world-models`
  - `video-generation`
  - `3d-generation`
  - `3d-4d-reconstruction`
  - `spatial-intelligence`
  - `3d-correspondence`
- `3d-avatars` was merged into `3d-generation`; do not reintroduce it.
- Topic/filter order should remain:
  1. `world-models`
  2. `video-generation`
  3. `spatial-intelligence`
  4. `3d-4d-reconstruction`
  5. `3d-generation`
  6. `3d-correspondence`
  7. `preprints`

# Author Rank

- `data-author-rank="1"` means Yushi is first author.
- `data-author-rank="2"` means Yushi is second author.
- Continue similarly for later positions.

# About / News

- The thesis should be referenced with the title in plain text plus a `[PDF]` link, not by making the whole title the link.
- News uses a simple scrollable list near the top of the page, in the style of Fangzhou Hong's homepage.
