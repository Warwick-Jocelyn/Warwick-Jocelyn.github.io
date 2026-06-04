# Maintenance Notes

Personal cheatsheet for keeping the site up to date. Not rendered as a public page.

## Links

- Repo: https://github.com/Warwick-Jocelyn/Warwick-Jocelyn.github.io
- Live site: https://warwick-jocelyn.github.io
- Template: [Academic Pages](https://github.com/academicpages/academicpages.github.io) (Jekyll)

## Set up on a new machine

```bash
gh auth login -h github.com    # device-code flow in any browser
gh auth setup-git              # use gh as git credential helper
git clone https://github.com/Warwick-Jocelyn/Warwick-Jocelyn.github.io.git
```

## Where to edit what

| Change | File |
|---|---|
| Top navigation menu | `_data/navigation.yml` |
| Sidebar identity (name, photo, bio, email, LinkedIn, Google Scholar) | `_config.yml` &rarr; `author:` |
| Sidebar "open to collaboration" line | `_includes/author-profile.html` (`.author__availability`) |
| Homepage text (Research Interests, News, Teaching) | `_pages/about.md` |
| Publications list | `_pages/publications_visual.html` + thumbnails in `images/pubs/` |
| Services / reviewing page | `_pages/services.md` |
| Avatar image | `images/profile.png` |

## Publish

```bash
git add <changed files>
git commit -m "..."
git push origin main          # GitHub Pages rebuilds in 1–2 minutes
```

## Local-only assets (NOT in this repo)

These live in the parent folder `2026_Personal_Website/` on the work machine and are not backed up by git:

- `Bio.txt` — bio draft
- `Jocelyn_CV.tex` — CV LaTeX source
- `CV_profile.png`, `IMG_4314.jpg` — high-res personal photos
- `representive_imgs_for_paper/`, `pictures_for_publications/` — full-resolution paper figures, used as source when adding new publication thumbnails

Keep a backup of these (private repo / OneDrive / Drive) so future edits aren't blocked.
