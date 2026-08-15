# Naming and slugs

Disciplined naming of directories and files keeps large projects more manageable. Consistent naming standards make it easier to locate files, especially over the course of a multi-volume, multi-year project.

As this project goes through iteratations and refactors it's expected that the naming conventions and standards will evolve.

All reels and other project content sources are assigned a slug for easy and consistent identification across all directories and usages.

## Slugs

Each reel gets a *slug* that is used consistently across folders and filenames.

As needed other items can be assigned slugs, for example, source documents about reels: `maker and reel docs/penn-700-series-manual.pdf`

Generally the slugs should be as specific as possible while keeping them as short as possible while still providing a clear idea of the file content.

### Pattern

  - Base:
`[maker]-[model]`
Example: `penn-720`

  - If there is a model number or size:
`[maker]-[model]-[model-number]`
Example: `pfleuger-pelican-1020`

  - If there is a variant:
`[maker]-[model]-[model-number](if applicable)-[variant]`
Example: `zebco-33-hudson-bay-red`

### Rules

  - In filenames slugs come first
  - All lowercase
  - For files that are or likely will be pushed to the repo, use hyphens between all words and codes, no spaces - for some documents, e.g., project development docs, spaces may be used
- In general do not use production years - *may* be used to distinguish variants

### Where slugs are used - examples

Project folder
  - Overview: `docs/[maker]/[slug]-overview.md`
  - Service guide: `docs/[maker]/[slug]-guide.md`

Workspace
  - Substack drafts: `.../substack/[slug]/[slug]-welcome-bench.md`
  - `maker and reel docs/maker/[slug]-manual.pdf`

Media folders
  - Pictures: `Pictures/vintage reel service guides/[maker]/[model]/[slug]-[desc].jpg`
  - Video: `Video/vintage reel service guides/[maker]/[model]/[overview / service guide / #]/[slug]-[desc].[mlt / mkv / rpp / wav / mp4 / txt]`