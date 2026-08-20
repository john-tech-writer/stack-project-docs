# Notes on project about and readme pages

These notes provide some guidelines for authring the all-important first few pages most people will encounter for a project - the README files / pages, the About snippets and pages, and the home / index page, which in many cases perhaps can be the About page (that turned out to be the logical case for the stack-project-docs repo).

Said P. about the Stack project: index.md (Home) is now unambiguously the About/orientation page — purpose, philosophy, origin story, direction. 

These notes are also focuses on the tools, etc. that go with the Vintage Reels project > Stack project, although in general these guidelines should apply to many other projects, at least as a starting point.

Most or all projects will include several basic files / text blocks or "surfaces" - each should do only one job:

  - **root README.md**: Renders inline on the repo's GitHub front page. Should be brief, tell "what's here" in terms of files, etc. and relationships to other repos, projects, etc. If this file is included in the project root it is pushed to the GH front page on the repo.

  - **GitHub repo description (titled "About")**: For people browsing repos on GitHub, should state purpose of repo in one sentence. Displays in profile's repo list and in search results. Authored in the GitHub repo front page About space. Should be less than 150 characters.
  
  "A model and methodology for building multi-year how-to documentation with an integrated video and narrative stack." Detailed description should go in the docs/index.md About page. For stack-project-docs the About page is the index / home page.

  - **docs/README.md**: What's in this folder, where's the built site, what's the tree. Only shows up if someone browses on the GitHub repo into /docs specifically (rare), should include the raw source / repo name, live site link, and folder map. Do not include in nav / yml. Also very brief.

  - **docs/index.md**: For people visiting the built site, should describe the site in detail - what it is, why it is, purpose, audience, philosophy, content model. For stack-project-docs this page is titled "About." This is the home / front page.