# Stack Project Docs

[john-tech-writer.github.io/stack-project-docs](https://john-tech-writer.github.io/stack-project-docs)

created 8.6.26

This site's main purpose is to provide a general-purpose skeleton for creating a GitHub
repository for technical documentation which is also linked to a media stack - YouTube video
and Substack narrative content. This models a robust workflow for authoring how-to procedural
docs, conceptual / overview docs, and reference docs, and organizing the content so it is easy
to navigate.

The media stack elements provide a ready-made audience platform for the more technical
documents that live in the repository.

This skeleton / model is suitable for a wide range of projects, from hardware-oriented
maintenance and repair work to software-based workflows. The project documents here were
developed over the course of about six months in parallel with a real demo project, which can
be viewed at [vintage-reel-service-guides.com](https://vintage-reel-service-guides.com).

The documents include not only general guidelines and structure, but also prompts to help
kick-start the process of authoring content. They also include more specific, concrete
instructions for tool use, for example, how to use Shotcut to create and edit videos.

This is a growing and evolving repository and will be updated regularly based on successive
refactoring passes on real projects. The knowledge gained from real-work projects will be used
to continuously update this repository and add to it, making it a more useful toolkit as it
grows and matures.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve
```

## Publish to GitHub Pages

Manual, same as the reel site:

```bash
mkdocs gh-deploy
```

Or push to `main` and let `.github/workflows/deploy.yml` build and deploy automatically —
one-time setup: Settings → Pages → Source → GitHub Actions (or leave on the `gh-pages` branch
if you'd rather keep triggering `mkdocs gh-deploy` by hand; either works with this workflow file
present, it just won't run unless Actions is selected as the source).

## Folder layout

```
docs/
  index.md                       # Home — this is project-workflow.md
  README.md                      # Orientation to this docs set
  directory-layout.md
  naming-slugs.md
  parking-lot.md
  volume-planning.md
  image-workflow.md
  image-lists.md
  audio-video-workflow.md
  backup-workflow.md
  substack-standards-series.md
  skeletons-templates-workflow.md
  repo-skeletons/
    overview-skeleton.md         # verbatim reel-repo template — see note below
    service-guide-skeleton.md    # verbatim reel-repo template — see note below
  img/
    screen-shots/
    screencasts/
  stylesheets/
    extra.css
mkdocs.yml
requirements.txt
```

## Note on `repo-skeletons/`

`overview-skeleton.md` and `service-guide-skeleton.md` are the actual templates used to draft
new reel overview/service-guide pages on the `vintage-reel-service-guides` repo. They're
published here verbatim (bracket placeholders and all) rather than genericized, since
genericizing them isn't the point yet — they're reference copies of the real working templates.
Expect MkDocs' link/image checker to warn on their `[maker]`/`[model]`/`[link]` placeholder
paths during build; that's expected and not a real broken link in this repo.
