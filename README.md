# rufuspaschal.com

Personal website for **Rufus Paschal** — Toronto security and public-safety professional and
law-enforcement graduate. Built as a static [Jekyll](https://jekyllrb.com/) site and hosted on
GitHub Pages with a custom domain.

## Structure

| Path | Purpose |
|------|---------|
| `_config.yml` | Site settings |
| `_layouts/default.html` | Base page template (meta, SEO, JSON-LD, header/footer) |
| `_includes/` | Reusable partials (`header`, `footer`, `picture`) |
| `assets/css/style.css` | Navy + gold theme (responsive, dark-mode aware) |
| `assets/images/` | Optimized photos (WebP + JPG) |
| `assets/resume/` | Downloadable resume PDF |
| `index.html`, `story.html`, `experience.html`, `community.html`, `employers.html`, `contact.html` | Pages |
| `CNAME` | Custom domain (`rufuspaschal.com`) |

## Local preview

```bash
gem install bundler jekyll
jekyll serve
```

Then open http://localhost:4000.

## Updating images

Source photos live in `../Photos`. Re-run the processor to regenerate optimized assets:

```bash
python ../scripts/process_photos.py
```

## Updating the resume

Regenerate the resume, then copy the PDF into `assets/resume/`:

```bash
python ../scripts/generate_resume.py
```
