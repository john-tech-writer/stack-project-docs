# Substack workflow

In Substack > Posts > Drafts > open the skeleton for the type of post being drafted > select all / copy > back to posts > Create > Article > paste > start drafting in Substack / paste into a new md doc > save in workspace `substack/[series short title]/[slug]-[title].md

The local md files are useful for sharing with P. for draft reviews. They are also saved as the final canonical version of each post. Most authoring can be done on substack.

There will be a good bit of back and forth between the Substack draft and local draft. After the local file is finalized and the post scheduled / published, append -final to filename.

## Detailed workflow

9.15.26: The following bullets describe where drafts are started and saved as they move through the workflow to finished, published, and archived posts. 

  - **Substack skeletons** - in Substack `/posts / drafts [SKELETON] [series name]: [title pattern]` Starting form for new posts. Open, copy, paste into new article / post. Should be occasionally re‑synced if the skeleton changes.

  - **Substack posts** - in Substack `/posts / drafts [series name]: [title]` > `/posts / [scheduled or published] [series name]: [title]` Draft, scheduled, and published versions of posts on Substack.

  - **Local copies of posts** - in workspace `/substack/[slug]/[slug].md` >`/substack/[slug]/[slug]-final.md` Local backup drafts and final versions of posts. Finals are canonical text of published posts on Substack. Use these for content diffing, quote reuse, and as a reference if Substack’s editor ever mangles something.

  - **Local skeletons** - in workspace `/substack/templates-skeletons/[series-name]-skeleton.md` Conceptual pattern for each series: headings, section order, prompt comments, and only light example text. Use this to design or revise the structure of the series.

    Lock the local as “frozen reference,” and treat the pairing between local skeleton and Substack skeleton as the living thing you revise over time. Only edit structure in the local skeleton. For substantive changes, e.g., add / remove a section, update the Substack template to match and note the update in a change log in the skeleton’s header, like: *Last synced to Substack template 6.11.26*

## Wiring

Welcome posts to to repo: Welcome template includes a Connections section with link to the repo, notes that when the entire stack is published a notification will be posted on substack.

Welcome posts to YT: Connections section includes link to YT. Optionally create substack video for posting to YouTube shorts.