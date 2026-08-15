# Skeletons and templates

Templates typically just provide a form - headings and a few prompts. Skeletons provide form plus some example content. Templates and skeletons provide a starting point for every content file, enforce evolving standards for form, headings, style, and content, and help jog memory and ideas.

As with naming standards, skeletons / templates codify important principles for authoring stylistically consistent content.

Best‑practice pattern for document templates / skeletons development:

  - A concrete worked example (existing published guide, reel stack, etc.) with most of the content removed, just a few concrete examples.

  -  Light inline guidance / prompts layered on top (italic hints: *here’s why this name works*, *this is where the template comes from*, etc.).

The form is never blank - it always provides both real content plus minimal commentary. Over time, after a few of these combo docs stabilize, a more generic template can always be abstracted from it if that is needed for speed or sharing (a sanitized version, for example, for a generic how-to project on the repo).

## Philosophy and development guidelines

Skeletons should enable authoring to be consistent within a given media stack / series and enable the author to avoid re‑inventing structure, sections, content types, and flow for each new document. Skeletons usually start as stripped-down versions of completed documents, with specific language mostly removed to make the skeleton reusable, while preserving the pacing and voice for the overall authorial presence for the stack. In other words, a finished doc is authored first, then the skeleton is abstracted from that, not the other way around. It's the codified wisdom contained in a developed doc.

The process for a new doc / series type / skeleton, roughly:

  - Draft a general doc outline, including sections with headings (form and structure) and prompts for what content types should go in each section. With a general theme and a few idea-notes Perplexity generally does a very good job of rounding it out, so these can profitably be started as Perplexity conversations, then copied from the P. window and pasted into an md file, then lightly formatted for Markdown.

For Substack posts and other online media it is better not to include markdown in the files since it will just have to be removed anyway when reformatting.

  - For online media the md file can then be copied and pasted into a new online media article / post, depending on the media type, and saved as a draft (not published). It may need some reformatting. This can be saved online as a draft skeleton.

  - The draft can then be copied / pasted into a new article and that can be developed into a draft post, then a published post. Most of this editing can be done in SS.

  - As the post is developed on SS it can be copied and pasted into a local md file for backup and possible local authoring. There may be some back and forth between the two files, the main idea being to manually synch them from time to time as logical groups of edits are completed.

The md files are very useful for sending to Perplexity because it does a very good job of reviewing them and providing constructive editing comments to develop the draft into a finished post with consistent voice, no redundancies, etc. The local md file will require a few differences in format, for example, instead of including images, the location and filename for the image file. Alternately images can just be less formally noted.

  - When the draft skeleton > draft post > published final post process is complete, the skeleton - both the copy on SS and the local copy - should be manually synched with the finished draft,. then most of the post-specific content deleted so the skeleton is generalized enough to serve as the structural, etc. basis for all other posts in the series.

## Repo skeletons

Live in the project folder `project-docs/repo skeletons/`

Usage: Creating the source files for overviews and service guides on the repo. Open in Notepad ++, Save As to the project folder `docs/[maker]-[slug]-[overview / service-guide].md.` These files get pushed to the repo.

##YouTube skeletons / templates

Live in the workspace `youtube/skeletons-templates/` and on YouTube.

Usage:

  - Creating video scripts. Open in Notepad ++, Save As to the workspace `youtube/[slug]-[overview / service-guide / #]-script.md.` These files get printed for benchtop use when recording the videos. These may be throwaways after the videos are completed.

  - Creating YouTube descriptions. Local md files are mostly for reference and backup, to compare with descriptions on the YouTube channel and enforce standards. May be Saved As if needed for temporary use. Most drafting can be done on YouTube.

    In YouTube > Studio > Content > Videos > select a video of the same type > pencil icon / details > copy title / details > paste into new video description

    There may be some back and forth between the local description example and the online draft for convenience in drafting but there is no need to save most of these descriptions locally since they are fairly generic. One or two examples of each type are enough.

## Video templates

Live in the Video media folder `templates/`

Usage: These are Shotcut mlt project files, creating new projects in Shotcut for overview and service guide videos. They provide the basic structure for video projects, text standards, and rough timings.

Open, Save As.

## Substack skeletons / templates

Live in the workspace `substack/skeletons-templates/` and on Substack.

Usage: Creating substack posts, one per series, slug is series display / title name.

Local md files are mostly for reference and backup, to compare with posts on Substack and enforce standards. May be Saved As if needed for temporary use. Most drafting can be done on Substack. However since these can be longer documents a local copy may be useful.

Copy and paste the text from the final post in Substack into an empty md file in Notepad ++, Save As to the workspace `substack/[slug]/[slug]-[service-guide-final / etc.].md.` These files are used for local drafting and backup / archiving content.

Workflow:

In Substack > Posts > Drafts > open the skeleton for the type of post being drafted > select all / copy > Create > Article > paste > start drafting in Substack / paste into a new md doc > save in workspace `substack/[slug]/[slug]-[title].md

There will be a good bit of back and forth between the Substack draft and local draft. After the local file is finalized and the post scheduled / published, append -final to filename.

## Substack detailed workflow

Each post will be based on, authored, and saved using the following series names and locations:

  - **Substack skeletons** - in Substack `/posts / drafts [SKELETON] [series name]: [title pattern]` Starting form for new posts. Open, copy, paste into new article / post. Should be occasionally re‑synced if the skeleton changes.

  - **Substack posts** - in Substack `/posts / drafts [series name]: [title]` > `/posts / [scheduled or published] [series name]: [title]` Drafts and final versions of posts on Substack.

  - **Local copies of posts** - in workspace `/substack/[slug]/[slug].md` >`/substack/[slug]/[slug]-final.md` Local backup drafts and final versions of posts. Finals are canonical text of published posts on Substack. Use these for content diffing, quote reuse, and as a reference if Substack’s editor ever mangles something.

  - **Local skeletons** - in workspace `/substack/templates-skeletons/[series-name]-skeleton.md` Conceptual pattern for each series: headings, section order, prompt comments, and only light example text. Use this to design or revise the structure of the series.

    Lock the local as “frozen reference,” and treat the pairing between local skeleton and Substack skeleton as the living thing you revise over time. Only edit structure in the local skeleton. For substantive changes, e.g., add / remove a section, update the Substack template to match and note the update in a change log in the skeleton’s header, like: *Last synced to Substack template 6.11.26*

