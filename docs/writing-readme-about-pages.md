# Writing project README and About pages

These notes provide some guidelines for authoring the all-important first few pages / text blocks / surfaces that most people will encounter in a project or site - the README and About pages. Most projects will include these files, or at least files that serve similar functions.

These notes are also focused on the tools, like GitHub, used for the Vintage Reels and Stack projects, although in general these guidelines should apply to many other projects, at least as a starting point.

Critically, each of these files should do only one job:

  - **root README file**: Lives in the project's root dir. This file is pushed to the repository and renders inline on the repo's GitHub front page. Should be brief, describe the repo, what it's for and relationships to other repos. For an example repository-level orientation README, see the [GitHub root README](https://github.com/john-tech-writer/stack-project-docs/blob/main/README.md).

    It should include instructions for local preview and publishing to GitHub Pages. Should include a directory layout or refer to a separate file. Do not include in nav / yml. Should include an update line up front so readers know it's current.

  - **docs README file**: Distinct from the root README, lives in the project's `/docs` folder. Should very briefly describe what's in the folder or link to a separate file, the working approach, and maintenance.

    Note that if both index.md and README.md files are present in `/docs`, MkDocs treats README.md as a competing index-page name and omits it from the generated site. If you want to make a docs README file viewable in the generated site, assign a different filename, like orientation.md.

    This file is only discoverable if someone browses on the GitHub repo into `/docs` specifically, which is rare. It should include the repo name and live site link. Do not include in nav / yml. Should include an update line up front.

    The following code block shows an example documentation-set orientation README:

```
# README

*updated 8.14.26*

This folder contains the content files for the stack-project-docs GitHub repository.

The built site can be viewed at https://john-tech-writer.github.io/stack-project-docs

## What lives here - key files

See [Directory layout](directory-layout.md)

## Working approach

The files here are authored locally as Markdown (md) files in Notepad ++ and pushed to the repository.

## Maintenance

This README will be updated when major files are added, renamed, moved, or removed and / or if this folder’s purpose changes.
```

  - **About text block / GitHub repo description**: For people browsing repos on GitHub, should state purpose of repo in one sentence. Displays in profile's repo list, on the repo GitHub front page, and in search results.

    This text block is authored in the GitHub repo front page About space. Should be less than 150 characters. Detailed description should go in an About page. For example, for the Stack repo: "A model and methodology for building multi-year how-to documentation with an integrated video and narrative stack."

  - **About page**: For people visiting the built site, should describe the site in detail - what it is, why it is, purpose, audience, philosophy, origin story, direction, content model. In many cases the About page may be the logical home page - for example, this is the logical case for the stack-project-docs repo - see the About... page on the built site [Stack Project Docs home page](https://john-tech-writer.github.io/stack-project-docs). Note that this means the page titled "About..." must be named `index.md` so that it will be the Home page for the built site. Simply, the About / Home / index functions can all live in one page.
