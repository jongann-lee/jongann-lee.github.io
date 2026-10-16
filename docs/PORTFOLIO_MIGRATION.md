# Portfolio migration

The Hugo portfolio has been migrated to al-folio. Biography and dates are preserved as supplied; update them when ready.

- Biography: `_pages/about.md`
- Experience and honors: `_pages/experience.md`
- Structured education, experience, interests, and honors: `_data/cv.yml` (retained for a future presentation choice)
- Project text, links, order: `_projects/` (Markdown projects and standalone HTML research pages; see `docs/RESEARCH_PAGES.md`)
- Publications: `_bibliography/papers.bib`
- CV navigation link: `_pages/cv.md`, with `nav_url: /uploads/JongannLee_Resume.pdf` and `nav_new_tab: true`; opens the résumé directly in local preview and production
- Primary downloadable résumé: `uploads/JongannLee_Resume.pdf`; the older CV remains at its original URL for existing links
- Contact: `_pages/contact.md`, `_data/socials.yml`

Five project detail URLs, their attachments, the publication detail URL, and `/uploads/` downloads retain their original paths. The full old Hugo source (including demo posts, sample publications, demo slides, and draft policy placeholders) is backed up separately; those template examples are not published on the new site.

## Local preview

Use Ruby 3.3.5, Bundler 4.0.6, and Node 20 or later.

```sh
bundle install
npm ci
bundle exec jekyll serve
```

Open `http://localhost:4000/`. This personal site uses an empty baseurl, overriding the starter documentation's `/al-folio` example.

## Publishing at the original address

The production repository is `jongann-lee/jongann-lee.github.io`, served at `https://jongann-lee.github.io/`. The migrated source replaces Hugo while preserving the original repository history. Continue editing in this personal-website folder; its `origin` points to the production repository after migration. The previous staging remote is retained as `staging`.

The sole active workflow, `.github/workflows/deploy.yml`, builds the site with Ruby, Node, and Jekyll on each push to `main`, then uploads and deploys the result using GitHub's official Pages actions. Settings → Pages → Source stays set to GitHub Actions; no `gh-pages` branch, repository rename, or domain change is needed. Pull requests build without deploying. Unrelated upstream template maintenance workflows have been removed.

After previewing and checking an update locally:

```sh
git add <changed-files>
git commit -m "Update portfolio"
git push origin main
```

Monitor the Deploy site workflow in GitHub Actions. The old Hugo checkout is an archive; do not push from it.
