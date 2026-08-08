# Portfolio site

Static HTML/CSS. No build step -- serve the directory with any static server
(directory URLs like `/work/breauxs-roadside/` need a server, not `file://`).

```text
index.html                     Homepage -- intro and two links, kept short
resume/index.html              Web resume
work/index.html                Side projects listing
work/breauxs-roadside/         Roadside overview + its two case studies
  index.html                   Engagement overview
  attribution/index.html       Call attribution case study (flagship)
  tooling/index.html           Internal tooling case study
assets/site.css                Shared design system
assets/gavin-breaux-resume.pdf Downloadable resume
```

Nav order is Home / Resume / Side Projects on every page; pages inside a project
append their own tabs after those three.

The homepage is deliberately thin: a positioning line and two cards. Evidence --
screenshots, figures, the chronological arc -- lives inside the project, not
above it. Anything added to the homepage should earn its place against that.

`work/index.html` is a real listing, so a new project is a card there plus a
directory beside `breauxs-roadside/`. Don't point the Side Projects tab straight
at a single project.

## Placeholders

`.ph` renders text as amber with a dashed underline, for content that still
needs writing. There are none in the site right now -- `grep -r 'class="ph"'`
should stay empty before publishing.

## Keeping the resume in sync

The page at `resume/index.html` and the download at
`assets/gavin-breaux-resume.pdf` are maintained separately. Update both when
experience changes, or they will drift.

## Deploying

Static hosting, no build config needed. For Cloudflare Pages, connect the repo
and leave the build command empty with the output directory set to `/`.

## Related repositories

The projects these case studies describe live in their own repos:

- `Breauxs-Roadside/breauxs-roadside-assistance-website` -- customer-facing site
- `Breauxs-Roadside/tire-inventory` -- the internal web app
- `gavinbreaux777/Terrible-Traffic`, `gavinbreaux777/Cam_Tracking_Pi` -- side
  projects, listed on the resume
