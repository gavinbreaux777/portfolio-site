# Portfolio site

Static HTML/CSS. No build step -- open `index.html` directly, or serve the
directory with any static server.

```
index.html        Overview and through-line
attribution.html  Call attribution case study (flagship)
tooling.html      Internal tooling case study
assets/site.css   Shared design system
```

## Before publishing

Search for `class="ph"` -- every amber dashed-underline placeholder needs
real content (name, contact links, repo links).

## Deploying

Static hosting, no build config needed. For Cloudflare Pages, connect the
repo and leave the build command empty with the output directory set to `/`.
