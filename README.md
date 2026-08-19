# What's here / relationships to other projects

[john-tech-writer.github.io/stack-project-docs](https://john-tech-writer.github.io/stack-project-docs)

*created 8.6.26*

*updated 8.14.26*

This repository / site / project is mainly intended to provide a general-purpose skeleton for creating a media stack for technical documentation. In this model, a GitHub repository anchors the core technical content, YouTube hosts video content, and Substack hosts narrative content. 

This stack models a robust workflow for known, well-researched technical authoring best practices:
  - Short overviews to provide context and explain concepts.
  - Illustrated procedures that clearly demonstrate tool use.
  - Short videos to give a general feel for a procedure and show specific moves difficult to capture in still photos or text.
  - Narrative content for a wider sense of context.
  - A notification hub for updates.

The media elements not only widen the audience reach of the repository, they also provide appropriate containers for content that doesn't fit the strictly technical nature of the repository.

This is a growing and evolving repository and will be updated regularly based on successive refactoring passes on real projects. The knowledge gained from real-work projects will be used to contiuously update this repository and add to it, making it a more useful toolkit as it grows and matures. All this project history is recorded in the [Changelog](docs/changelog.md).

## Relationship to other repositories

This repo / site were spun off from the vintage-reel-service-guides GitHub repo.

The files here were originally Vintage Reels' internal project docs. They are now being developed in a separate repo / site which provides a model and methodology for building multi-year how-to documentation with an integrated video and narrative stack. The Vintage Reels project is a living example of the model and methodology.

The built Vintage Reels site can be viewed at https://vintage-reel-service-guides.com

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

Or push to `main` and let `.github/workflows/deploy.yml` build and deploy automatically. It runs on every push regardless of your Pages settings — the one-time setup step is telling Pages where to find the result: Settings → Pages → Source → **Deploy from a branch** → branch `gh-pages` → folder `/ (root)` → Save. (Don't select "GitHub Actions" as the source — that's a different deployment method this workflow doesn't use.)

## Directory layout

See [Directory layout](docs/directory-layout.md)