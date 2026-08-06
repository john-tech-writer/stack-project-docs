# Directory layout

## 1. Project folder

Local clone of `vintage-reel-service-guides` repository on Github

- `vintage-reel-service-guides/`
  - `.git/`
  - `.github/`
  - `docs/`
    - `img/`
      - `[maker]/`
        - `[model]/`
          - `[slug]-[image-desc].jpg`  ← final images used in repo
    - `[maker]/`
      - `[slug]-overview.md`  ← final docs used in repo
      - `[slug]-service-guide.md`
      - `penn-spinfisher-series.md`  ← example-other *reel-specific* docs used in repo
    - `about.md`
    - `index.md`  ← repo landing page
    - `references.md`
    - `baitcasting-reels.md`
    - etc.  ← generic (*non-reel-specific*) docs used in repo
  - `site/`  ← built site files

## 1a. Project docs (own repo, own site)

As of 8.6.26, `project-docs/` moved out of the `vintage-reel-service-guides` repo and into its
own sibling repo/site, `stack-project-docs`, so this material is actually browsable instead of
just sitting pushed-but-unpublished. Same account, same MkDocs + GitHub Pages wiring, published
at `john-tech-writer.github.io/stack-project-docs` (no custom domain).

- `stack-project-docs/`  ← files for planning, organizing, and maintaining the repo and workflow
  - `.git/`
  - `.github/workflows/deploy.yml`  ← auto-publish on push to `main`
  - `mkdocs.yml`
  - `docs/`
    - `index.md`  ← this is `project-workflow.md`, serves as the site home page
    - `orientation.md`  ← this is `README.md`, renamed because MkDocs treats README.md as an
      alias for index.md and silently drops it when both exist in the same folder
    - `directory-layout.md`  ← this file
    - `naming-slugs.md`
    - `parking-lot.md`
    - `volume-planning.md`
    - `image-workflow.md`
    - `image-lists.md`
    - `audio-video-workflow.md`
    - `backup-workflow.md`
    - `substack-standards-series.md`
    - `skeletons-templates-workflow.md`
    - `repo-skeletons/`
      - `overview-skeleton.md`
      - `service-guide-skeleton.md`
    - `img/`
      - `screen-shots/`
      - `screencasts/`
    - `stylesheets/extra.css`
  - `site/`  ← built site files

## 2. Workspace

Active working documents that do **not** go in the repo

- `vintage-reel-service-guides-workspace/`
  - `general referece docs/`
    - `general-reference.md`  ← writing references
    - `reel collection.docx`
  - `how-to class outlines/`
  - `maker and reel docs/`
    - `baitcasting-general/`
    - `[maker/]`
      - `[slug]-[desc].[ext]`
    - `penn/`  ← for example
      - `penn production archive.pdf`
    - etc.
  - `project development-background/`
    - `audio-troubleshooting-win.docx`
    - `design-badge notes.docx`
    - `docs-mermaid-flowcharts-mkdocs.docx`
    - `photo-lighting-fixing glare-polarizing.docx`
    - `README.md`← describes purpose for this folder and file naming conventions
    - `video-adding-audio-shotcut.md`
    - `z-review of first vid-burke drama ideas--other bits--old version.md`
    - etc.  ← 30+ docs, mostly .docx
  - `reel-balanced tackle disc/`
    - `garcia 3000-4000 disc.pdf`  ← for example
    - etc.
  - `substack/`
    - `[slug]/`
      - `[slug]-new-arrival.md`
      - `[slug]-production-notes.md`
      - `[slug]-field-stories.md`
      - `[slug]-new-publication`
    - `youtube/`
    - `[slug]/`
      - `[slug]-overview script.docx`
      - `[slug]-disassembly script.docx`
      - `[slug]-reassembly script.docx`
      - `[slug]-youtube desc.docx`  ← descriptions for all YT vids
    - `templates`
      - `overview-script template-example.docx`
      - `service-script template-example.docx`  ← for both service vids
      - `youtube desc template-example.docx`

## 3. Pictures

All raw and edited photos

- `Pictures/vintage reel service guides/`
  - `assets-badge-banners/`
  - `field trips/`
    `- [place]`
  - `fish images/`
    - `[common-name]-[mods].jpg
  - `jigs/`
  - `workspace-bench/`
    - `notebook pages/`
    - etc.
  - `[maker]/`
    - `[model]/`
      - `[slug]-[desc].jpg`

## 4. Video

All captured footage and edits

- `Video/vintage reel service guides/`
  - `audio test files/` - for trying different render settings from Reaper
  - `cleaning-lubricating/` - all files for this reference service video
  - `[maker]/`
    - `[model]/`
      - `[slug] overview/` - all files for overview
      - `[slug] service guide [#]/` - all files for a service video - each video gets its own folder - file types:

        - mlt - Shotcut project file - `[slug] [overview / service guide / #].mlt`
        - txt - chapter markers exported from Shotcut
        - mp4 - **final** audio / video output from Shotcut - `[slug] [overview / service guide / #] final.mp4`
        - wav  - **final** audio VO / fx files rendered from Reaper - `[slug] [overview / service guide / #] rendered.wav`
        - rpp - Reaper project file
        - mkv  - raw video files from Guvcview - `[slug]-[overview- / service guide- / #].mkv` - filenames include hyphens to denote their origin from the workbench ubuntu laptop

      - `Media` - Reaper media files - wav **source** files for the project
  - `substack/` - mp4 shorts generated by substack from posts
  - `templates/`  - mlt overview and service guide templates for Shotcut projects

File types:

  - mlt - Shotcut project file
  - txt - chapter markers exported from Shotcut for YouTube chapters, currently (8.1.26) service guides only
  - mp4 - final audio / video output from Shotcut ready for YouTube
  - wav - audio VO and fx files rendered from Reaper / audio source files (Media folder)
  - rpp - Reaper project file
  - mkv - raw video files from Guvcview, filenames include hyphens