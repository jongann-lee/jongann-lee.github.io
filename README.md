# Jongann Lee — personal website

Academic portfolio built with [al-folio](https://github.com/alshedivat/al-folio) and Jekyll. The production address is **https://jongann-lee.github.io/**.

## Edit the content

| Content                                      | File                                     |
| -------------------------------------------- | ---------------------------------------- |
| Biography, education, research interests     | `_pages/about.md`                        |
| Experience and honors                        | `_pages/experience.md`                   |
| Project descriptions, dates, images, reports | `_projects/*.md`                         |
| Publications                                 | `_bibliography/papers.bib`               |
| Web CV                                       | `_data/cv.yml`                           |
| Downloadable original CV                     | `uploads/JongannLee_CV.pdf`              |
| Contact and social links                     | `_pages/contact.md`, `_data/socials.yml` |
| Site settings                                | `_config.yml`                            |

Experience currently uses a plain template page. Structured education, experience, interests, and honors are retained in `_data/cv.yml` for a future presentation choice. The CV navigation link opens the original PDF directly. The downloadable PDF is maintained separately.

## Preview locally

Install Ruby 3.3.5, Bundler 4.0.6, and Node 20 or later, then run:

```sh
bundle install
npm ci
bundle exec jekyll serve
```

Open **http://localhost:4000/**. This personal site uses an empty `baseurl`; template examples using `/al-folio` do not apply to this site.

## Validate

```sh
npm run lint:prettier
npm run lint:style-contract
bundle exec al-folio upgrade audit --no-fail
bundle exec jekyll build
```

## Publish

This is the staging repository. Its workflow builds the site but only publishes when installed in **`jongann-lee/jongann-lee.github.io`**. Keep the existing production repository and its Git history. Transfer the reviewed source there and remove its old Hugo source and deployment workflow. Set GitHub Settings → Pages → Deploy from a branch → `gh-pages` → `/ (root)`.

See [migration details](docs/PORTFOLIO_MIGRATION.md) for the preserved URLs and content mapping. No publishing or repository rename has been performed.

The template documentation remains in [`docs/`](docs/README.md).
