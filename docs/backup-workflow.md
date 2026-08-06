# Backup workflow

In each workflow doc pointing to this one add this pointer:
Backup step (summary):
At the end of this workflow, sync updated project folders to Dropbox as described in backup-workflow.md.

Dropbox project layout

Vintage Reel Service Guides Project/

  - Pictures/vintage reel service guides/...

  - Video/vintage reel service guides/...

  - vintage-reel-service-guides/ (repo)

  - vintage-reel-service-guides-workspace/ (project docs & reference)
  
  Dropbox project layout

Second machine (laptop) checklist

Before working on the laptop:
1. On the desktop, make sure Dropbox has finished syncing (no pending changes).
2. On the desktop, commit and push any repo changes to GitHub.
3. On the laptop, wait for Dropbox to finish syncing the Vintage Reel Service Guides Project folder.
4. In the repo on the laptop, run git pull so it matches the desktop.

While working on the laptop:
5. Edit files only in the local project folders under the Vintage Reel Service Guides Project wrapper.

When finished on the laptop:
6. Commit and push repo changes from the laptop to GitHub.
7. Leave the laptop on until Dropbox finishes syncing the Vintage Reel Service Guides Project folder.