# Editorial review: project-docs content

*By P., 8.6.26, initial rollout of the project docs as a separate repo: stack-project-docs. Thinking this might become a CHANGELOG or something like that, in the project nav, so a record of changes needed / made / dates.*

## Priority findings — address these first

1. **Re-establish one current map of the project’s repositories, locations, and output names.** The documentation now describes two different physical realities: `orientation.md` says these files live in `project-docs/`, are pushed to the main repo, and are not in site navigation, while `directory-layout.md` says that, as of 8.6.26, they moved to the published sibling `stack-project-docs` repo/site. That drift propagates into instructions for where skeletons, source files, images, and backups live. This is the highest-leverage repair because it prevents otherwise disciplined instructions from sending work to the wrong place.

2. **Make the hub a release workflow, not just a production workflow.** `index.md` says each source Markdown file “will get pushed to the repo,” but it never specifies the publish/verify handoff, nor the release gate for the Substack notification. The two repo skeletons say videos are added *after* “the overview and guide are written and pushed to the repo”; read literally, that puts the overview video after the service guide, unlike the hub’s overview-video-first sequence. Define the one authoritative order: draft → review assets/links → commit/push → confirm the Pages result → upload/publish YouTube → update embeds/links → publish the Service guide notification. State whether visibility is public or unlisted at each checkpoint.

3. **Close the photograph-to-published-image handoff.** Capture guidance is unusually concrete, but the decisive editorial stage is missing: selecting frames, recording their purpose, making derivative edits, assigning final filenames, placing them in the correct repo directory, inserting them in Markdown with alt text, and checking the published result. This gap is compounded by incompatible destinations: `index.md` and the skeletons use `docs/img/[maker]/[model]/…`; `image-workflow.md` gives `/docs/img/[slug]/…`. The docs also say basic photos are taken “before the reel is serviced and also after,” while the hub schedules only the first intact-photo session and then the disassembly/reassembly session.

4. **Declare systems of record and a conflict-resolution rule for Substack drafts/skeletons.** `skeletons-templates-workflow.md` correctly anticipates “a good bit of back and forth,” but it calls local finals “canonical text” while saying most editing happens in Substack and tells the reader to sync “from time to time.” It also says to “Lock the local as ‘frozen reference’” and then “Only edit structure in the local skeleton.” Choose the master for (a) post text, (b) current skeleton structure, and (c) post-publication corrections; give a short sync checkpoint and a rule for resolving divergence.

5. **Define completion at reel and volume levels.** `volume-planning.md` records useful status, but “All docs and media completed” for the Nobby sits next to “Substack notification scheduled,” and the same page says two reels have “all docs and media published” while the Penn 720 still needs extra guides, videos, and two retro posts. The doc needs explicit statuses such as *service complete*, *core stack published*, *extended procedures pending*, and *volume complete*, plus the required artifacts for each. Otherwise the notification trigger, planned milestones, and backlog are measuring different things.

*8.6.26: item 5, just take all the status info out of the vol. doc and only maintain it in ONE place, the log of reels in the workspace. this info doesn't need to be in two places or on the project docs at all. more useful would be generic info / convo about how to strategize volumes for a doc set, and this is captured in one of the background docs i think. this principle should apply to all this stuff - don't have info in multiple places to maintain - for this repo, focus on more skeleton-like content - specifics don't belong here except as examples. redundancies are covered in the next section, so that's a starting point.*

*8.6.26: not sure where this is covered in the review, but the repo skeletons have been moved out of the project docs folder and into the workspace - this makes more sense since that's where all the other skeletons live and also because all authoring really starts there, locally, in Notepad ++.*

## 1. Redundancies

### A. The project-docs purpose and the role of the hub are stated three times, with different current-state implications

- **Overlap:** `index.md`, “Workflow philosophy,” calls itself “the **one place** to always return.” `orientation.md`, “Start here,” calls it “the main process document,” “the spine,” and the roadmap from selection through repository updates. `directory-layout.md`, “1a. Project docs,” again explains that its `index.md` is the project-workflow home page.
- **Why it matters:** The repetition is not merely introductory reinforcement because it carries contradictory placement/publication information (see Logic gaps A). It also creates three places to revise whenever the internal site changes.
- **Recommendation:** Make **`orientation.md` canonical for purpose, audience, repository/site status, and how to use this documentation set**. Make **`index.md` canonical for the active end-to-end production sequence**. Let `directory-layout.md` contain only the directory tree and a one-sentence pointer to each of those documents. Remove the repeated institutional description from the other two.

### B. Directory paths and filename patterns are repeated across four documents instead of being assembled from two authorities

- **Overlap:** `directory-layout.md` specifies `docs/[maker]/[slug]-overview.md`, `docs/[maker]/[slug]-service-guide.md`, and `docs/img/[maker]/[model]/…`. `naming-slugs.md` repeats paths but calls the service file `[slug]-guide.md`. `index.md` repeats the overview and service-guide locations. `skeletons-templates-workflow.md`, “Repo skeletons,” gives a third form: `docs/[maker]-[slug]-[overview / service-guide].md`.
- **Recommendation:** Let **`directory-layout.md` own directory topology** and **`naming-slugs.md` own basename grammar**. In `index.md` and `skeletons-templates-workflow.md`, use a short link to both rather than restating literal paths. Keep only an example that is generated from the two authorities. This is especially important for the folder/name boundary: the current third form makes `[maker]` part of the basename rather than the directory.

### C. Slug rules are duplicated by image naming rules, but the scopes are not cleanly separated

- **Overlap:** `naming-slugs.md`, “Slugs,” establishes `[slug]` and general repository naming rules. `image-workflow.md`, “File naming standards / slugs,” repeats `[slug]-[description].jpg`, lowercase/hyphen conventions, and elaborates numbered suffixes, views, actions, states, and image purpose.
- **Recommendation:** Keep **`naming-slugs.md` as the canonical slug definition and cross-media basename rule**. Rename the image section to **“Image descriptor vocabulary and sequence rules”** and retain only its genuinely image-specific material (for example, `hero-`, `-ref`, `-v1`, and action-sequence numbering). The suggested `photo-standards.md` should either be created at a stated location or replaced by this maintained vocabulary section; do not introduce a fourth naming authority.

### D. Video capture/export settings are maintained in both the photo and the audio/video workflows

- **Overlap:** `image-workflow.md`, “Video workflow” and “Video export settings,” specifies Guvcview, C920 settings, 1920×1080, 30 fps, H.264, MKV, Shotcut, and the 8 Mb/s export target. `audio-video-workflow.md` also names Guvcview, the C920, Shotcut, the YouTube preset, and the production sequence.
- **Recommendation:** Make **`audio-video-workflow.md` the sole owner of video capture, audio, editing, export, upload, and cleanup procedure**. In `image-workflow.md`, retain a one-line cross-reference only if the still-photo workflow needs to acknowledge that the same bench setup supports video. This reduces the chance of two conflicting presets after a change.

### E. File-type inventories occur in both the directory reference and the operating procedure

- **Overlap:** `directory-layout.md`, “Video,” inventories MLT, TXT, MP4, WAV, RPP, and MKV both under the tree and again in “File types.” `audio-video-workflow.md`, steps 2–7 and step 10, repeats the same types and their purposes.
- **Recommendation:** Keep **the directory layout’s inventory concise and structural** (which folder contains which asset class). Keep **the audio/video workflow’s names, creation order, cleanup, and retention decision**. Eliminate the duplicate explanatory list in the directory reference or replace it with a link.

### F. Substack instructions have three partially overlapping homes

- **Overlap:** `index.md` tells the reader when to write Welcome and Service guide posts; `substack-standards-series.md` defines series, tags, and the Welcome-post wiring; `skeletons-templates-workflow.md` explains copying, drafting, local copies, final names, and skeleton synchronization.
- **Recommendation:** Make **`substack-standards-series.md` canonical for editorial policy**: series definitions, tags, title pattern, publication trigger, required Connections links, and post-publication cross-linking. Make **`skeletons-templates-workflow.md` canonical for artifact lifecycle**: where the template lives, how to clone it, and how to synchronize it. In the hub, retain only timing and links to those two authorities.

### G. Backup instructions are stated as both a directive to authors and an incomplete workflow

- **Overlap:** `backup-workflow.md` begins, “In each workflow doc pointing to this one add this pointer,” then supplies the exact summary. `index.md` separately inserts that summary after each photo round. The audio/video workflow does not insert it despite creating the largest, most deletion-prone assets.
- **Recommendation:** Keep **`backup-workflow.md` as the sole canonical policy** and add a small, consistent “Backup checkpoint” callout at every defined handoff (capture ingest, repo release, completed video project, and before destructive cleanup). The hub should link to the named checkpoint rather than restating the sentence ad hoc.

## 2. Logic / workflow gaps

### A. The project’s actual location and public/private status are contradictory

- **Evidence:** `orientation.md`, opening, says the documents “reside in the project folder in `project-docs/` and get pushed to the repo but are not included in site navigation.” `directory-layout.md`, “1a. Project docs,” says that on 8.6.26 they “moved out of” the main repo into their own sibling repo/site and are published through GitHub Pages. `backup-workflow.md` still lists only the main repo and a workspace under the Dropbox wrapper, not the separate project-docs repo.
- **Gap:** A reader cannot reliably tell which repo they are editing, what gets pushed where, or whether the backup set includes the now-separate docs repository.
- **Repair:** Add a compact “Current topology (as of …)” block to `orientation.md`: main public guide repo, published workflow-docs repo, workspace, Pictures, Video, and Dropbox coverage. Use stable names for all six. Update the backup layout and skeleton-location instructions from that block.

### B. Several operational paths disagree; one of them will necessarily be wrong

- **Evidence:**
  - `index.md` sends the acquisition log to `reference docs and books/reel collection.docx`; `directory-layout.md` places it in `general referece docs/reel collection.docx`.
  - `index.md` calls `/maker and reel docs/[maker]/…` a **Pictures media folder**, while `directory-layout.md` presents `maker and reel docs/` under **Workspace** and places actual photos under `Pictures/vintage reel service guides/[maker]/[model]/…`.
  - `index.md` and the skeleton image examples use `docs/img/[maker]/[model]/…`; `image-workflow.md` sends the same repo overview images to `/docs/img/[slug]/…`.
  - `skeletons-templates-workflow.md` puts repo skeletons in `project-docs/repo skeletons/`; `directory-layout.md` names the actual directory `repo-skeletons/`.
- **Gap:** This is more than nomenclature: a new reel can be correctly processed yet stranded in an unreferenced directory or built with broken image links.
- **Repair:** Establish a single path table with **asset, source of truth, working location, published location, and filename pattern**. Reference that table from every procedural document. Do not use descriptive phrases such as “project folder” where two repository roots exist.

### C. The workflow has no explicit release gate or updating loop for cross-platform links

- **Evidence:** `index.md` places the overview video directly after writing the overview and puts service videos after writing the service guide. Both repo skeletons instead say overview and service videos are made after “the overview and guide are written and pushed to the repo,” then added as an “update.” The Service guide notification is for a “new completed stack,” but no step says when to update the repo page with live YouTube links, confirm the GitHub Pages build, or test the Substack Connections links.
- **Gap:** The outward-facing objects depend on one another, but their publication states and link updates are not modeled. A service page may point to a future video; a notification may be sent before its target pages are live; or the video may be live without a durable repo/Substack connection.
- **Repair:** Add a small release checklist to `index.md`, with explicit gates and owners (even if the owner is always the author): **repo source committed/pushed → hosted page checked → YouTube uploaded/published → repo embeds/links updated → Substack notification published → all outbound links sampled**. State the permitted exception for a Welcome post, which intentionally precedes the completed stack.

### D. The basic-photo workflow omits the post-service capture and curation stage it promises

- **Evidence:** `image-workflow.md`, “Basic photos,” says intact photos are taken “before the reel is serviced and also after.” `index.md` schedules an initial intact-photo session, then only a disassembly/reassembly session. Its later steps convert and use “initial” images but never schedule the second intact set, comparison, or final hero choice.
- **Gap:** There is no decision point for whether the pre-service, in-progress, or post-service photo becomes the overview hero; no process for refreshing an overview after restoration; and no handoff from a candidate image to its Markdown placement.
- **Repair:** Split this into named stages: **intake/pre-service reference**, **procedure capture**, **post-service hero/functional capture**, and **selection/publishing**. For each, say the minimum output, where it lands, and who decides whether an image is reference-only, guide-step, hero, video still, or Substack image.

### E. Image coverage rules conflict at the level of the service-guide promise

- **Evidence:** `image-workflow.md`, “Disassembly and reassembly photos,” requires “At least one image per user action/step,” with two or three for intricate moves. `image-lists.md`, “Service guides,” calls reassembly “step by step” but says the Nobby reassembly uses “5 images - just highlights.”
- **Gap:** “Step by step” and “just highlights” are different reader commitments. The writer cannot know whether missing images are an acceptable editorial compression or a coverage failure.
- **Repair:** Define a default and exception rule: for example, every irreversible, orientation-sensitive, or failure-prone action gets a frame; reversible repetitions may be summarized; a short highlight set may be used only when the guide explicitly points to the full video. Put the rule in `image-workflow.md` and let `image-lists.md` link to it.

### F. Substack’s bidirectional local/online process has no source-of-truth or sync trigger

- **Evidence:** `skeletons-templates-workflow.md` says most editing can occur in Substack, allows “back and forth” with a local copy, says local finals are “canonical text,” and describes syncing only “from time to time.” It then says to lock the local skeleton as “frozen reference” while also editing structure locally.
- **Gap:** This permits silent divergence among a local draft, a Substack draft, a local final, a local skeleton, and a Substack skeleton—especially after a scheduled post is edited.
- **Repair:** Define a two-row policy: (1) **post text:** Substack draft is working master until publication, then export to `-final` and treat that export as the canonical archival text; (2) **structure:** local skeleton is the structural master, versioned with a date, then copied to the Substack skeleton immediately after each structural change. Add one required sync at scheduling and one after post-publication edits.

### G. Backup and cleanup are not sequenced safely enough for the assets the workflow creates

- **Evidence:** `audio-video-workflow.md` tells the reader to delete autosaves, backup folders, extra project-file types, and unused Reaper media after completion. `backup-workflow.md` describes a laptop transfer sequence but no universal end-of-session verification, no restore test, and no explicit checkpoint before this cleanup. The backup document’s opening instruction says the pointer should appear at the end of *each* workflow, but it is absent from the audio/video workflow.
- **Gap:** “Primary file is verified to open” is not equivalent to “the final media and source project exist in the intended backup set.” The current ordering could turn a routine cleanup into loss of a recoverable project state.
- **Repair:** Require a named pre-cleanup checkpoint: confirm Dropbox complete on the source machine, confirm expected final/source files are present in Dropbox, confirm the primary MLT/RPP opens from its intended final location, then delete defined disposable files. State what is retained for a completed video (source MKV, primary MLT/RPP, rendered WAV, final MP4, chapter TXT, thumbnails/metadata) and what is expressly disposable.

### H. Completion language in volume planning is not tied to the stated publishing model

- **Evidence:** The plan says every reel gets a repo overview/service guide, videos, and Welcome/notification posts. The Nobby is called “All docs and media completed” while its notification is still scheduled; the Penn 720 still has extra deliverables after its overview/guide/video completion; the Zebco entry records a Reel stories post without showing the core guide/media stack.
- **Gap:** “Completed,” “published,” “service completed,” “notification,” and “volume finished” are not distinct project states. This makes it hard to prioritize, report a milestone accurately, or decide when a volume is done.
- **Repair:** Add a legend and per-reel checklist to `volume-planning.md`. Suggested states: *acquired*, *research ready*, *bench/service complete*, *core repo published*, *core video published*, *Welcome published*, *completion notification published*, *extended modules pending*, *volume closed*.

### I. Reference acquisition has no documented editorial/rights decision record

- **Evidence:** `index.md` tells the reader to acquire all available documentation, save it in the workspace, add an entry to `docs/references.md`, and include a photo/document in the project if it is “not copyrighted and … available outside pay walls.” Other sources are linked rather than included.
- **Gap:** Availability outside a paywall is not a usable decision rule for republication, and the docs do not state the minimum metadata to record (source URL, creator/publisher, publication date, rights/permission basis, captured-by date, or use in which guide). This will make later citation, attribution, and reuse decisions inconsistent.
- **Repair:** Add a compact reference-intake record and an explicit publication decision: **link only / reproduce a self-created scan or photo / reproduce under stated permission or public-domain basis / do not use**. Keep the detailed rights rationale with the source record; keep the public References-page entry concise.

## 3. Terminology inconsistencies

| Concept | Conflicting terms / locations | Editorial fix |
|---|---|---|
| **The docs repository and its status** | `orientation.md` calls these internal, pushed-but-not-navigated `project-docs/`; `directory-layout.md` says they are the published sibling `stack-project-docs` site. | Use **“workflow-docs repository”** (or another chosen stable name) for this site and **“guide repository”** for `vintage-reel-service-guides`. Define both once in Orientation. |
| **“Project folder”** | It can mean the main guide repo (`directory-layout.md`, section 1), the docs repo (`orientation.md` / `skeletons-templates-workflow.md`), or the general Dropbox wrapper (`backup-workflow.md`). | Retire the unqualified term in procedures. Use **guide-repo root**, **workflow-docs-repo root**, **workspace**, **Pictures root**, **Video root**, or **Dropbox project root**. |
| **The workflow hub’s name** | The actual file is `index.md`; `index.md` itself says to open `project-workflow.md`; `directory-layout.md` says `index.md` “is `project-workflow.md`”; `orientation.md` alternates “project workflow” and “project-workflow.” | Choose a display name (**Project workflow**) and a reference convention (**the Project workflow page, `index.md`**). Do not write a phantom filename in prose. |
| **Service-guide output filename** | `directory-layout.md` and `index.md`: `[slug]-service-guide.md`; `naming-slugs.md`: `[slug]-guide.md`; `skeletons-templates-workflow.md`: `[maker]-[slug]-[overview / service-guide].md`. | Standardize the full output example in the path table and make all three documents point to it. |
| **Image source/destination locations** | `index.md` calls `maker and reel docs` a Pictures folder; `directory-layout.md` places it in Workspace; image output is `[maker]/[model]` in the hub/skeletons and `[slug]` in `image-workflow.md`. | Use **source/reference documents**, **raw capture**, **working derivatives**, and **repo-published images** as distinct terms, each with one location. |
| **Substack Service guide series** | `substack-standards-series.md` defines **“Service guide”** (singular); `index.md` says **“Service guides”** (plural); `volume-planning.md` calls it a **“notification”** post. | Choose one visible series title, e.g. **Service guide**, and define **completion notification** as its function, not a competing name. |
| **Welcome series / tag form** | The canonical title is **Welcome to the bench** and the tag is **New Arrival** in `substack-standards-series.md`; elsewhere appear “welcome to the bench,” `welcome-bench`, `new-arrival`, and “new arrival.” | Keep case-sensitive display names separate from machine names: **series title**, **tag label**, and **draft filename stem**. State all three in the standards doc. |
| **Production-notes series** | `substack-standards-series.md`: **Production notes**. `parking-lot.md`: “from the bench / production notes,” “At the bench / Production notes,” and “At the Bench / Production Notes.” | Decide whether **At the bench** is a renamed display series, a recurring rubric inside Production notes, or an abandoned concept. The parking lot may retain alternatives, but mark the canonical choice. |
| **Reel stories capitalization** | The standards document uses **Reel stories**, consistent with its sentence-style cap standard; `volume-planning.md` and the Parking Lot use **Reel Stories**. | Use the stated sentence-style series capitalization outside freeform note quotations. |
| **Substack skeleton directory name** | `skeletons-templates-workflow.md` says `substack/skeletons-templates/` and later `substack/templates-skeletons/`. | Select one directory name; use it in every location example and in the directory layout. |
| **Skeleton governance** | The document distinguishes skeletons from templates well, but calls a local skeleton both “frozen reference” and the place to “Only edit structure.” | Define **reference copy**, **editable master**, and **online deployed copy** as three separate roles—or use two copies with clear names. |
| **Completion terms** | “service completed,” “completed stack,” “all docs and media completed,” “published,” and “volume finished” are used without a common status definition. | Add the status vocabulary to Volume planning and use it in the hub’s notification trigger. |

## 4. Genuine weaknesses

### A. `image-lists.md` stops before it becomes a usable cross-platform planning tool

- **Evidence:** The repo section has a useful checklist. The later headings, “Videos - stills for timeline,” “Overviews,” “Service guides,” and “Substack posts,” contain no entries.
- **Why this is weak:** The hub says intact images will later serve video and Substack, but the only list that should turn that reuse into a deliberate plan is blank. This leaves the writer to decide afresh which stills, aspect ratios, crops, captions, and moments are needed for each destination.
- **Concrete repair:** Either complete those two sections with a small per-output checklist (for example: overview-video opener, mechanism close-up, before/after, end-card still; Welcome-post hero/detail; Service-guide notification stack image) or remove the empty headings until a genuine list exists. Add a column/marker for **capture once / use in repo / use in video / use in Substack**.

### B. Several central photography instructions are explicitly unfinished rather than safely provisional

- **Evidence:** `image-workflow.md` says “Need to doc working distance,” “Need to doc better what size image field will be,” and ends its “Geometry” and “Lighting” sections with imperatives to describe/draw the setup, followed only by “NEO.”
- **Why this is weak:** These are the variables most likely to affect repeatability of close service photography. The document has strong lens exposure notes, but not a reproducible bench layout or lighting recipe.
- **Concrete repair:** Convert the open reminders into a minimum viable bench recipe: camera/lens, subject distance, camera height/angle, tray/hero-box location, light names/positions/diffusion, white-balance target, and one reference photograph/diagram. Keep experimental alternatives in the Parking Lot or a separate test log.

### C. The photo-processing instruction uses global automatic changes without a content-quality checkpoint

- **Evidence:** `image-workflow.md` instructs a batch convert with “Resize to 1800px / longest side, Auto contrast, Auto levels,” then sends output to the repo. It explains candidate versions and `hero-` use elsewhere but gives no review criteria or preservation rule.
- **Why this is weak:** Automatic contrast/levels can change the appearance of finishes, labels, and corrosion—the very evidence a restoration guide may need to show. The procedure does not say whether originals are preserved, whether processing is applied only to derivatives, or how a reader decides that a processed image still represents the reel faithfully.
- **Concrete repair:** Add a short post-conversion check: retain the original capture unchanged; process copies only; inspect white balance, clipping, label legibility, detail shadows, and color/material fidelity; use manual adjustment or a `-v#` derivative when the automatic version changes meaningful evidence. State which derivative is eligible for the repo.

### D. The YouTube publication instruction is too dependent on an unspecified previous upload

- **Evidence:** `audio-video-workflow.md`, step 8, says to write the title/description “based on last YouTube upload,” compare it to a workspace skeleton, and add playlists.
- **Why this is weak:** “Last upload” is not necessarily the same content type and can perpetuate an accidental deviation. The file gives no minimum metadata/quality checklist for title form, description links, chapters, thumbnail, visibility, end screens/cards, captions, or the repo/Substack links that make the stack coherent.
- **Concrete repair:** Replace “last YouTube upload” with “the latest approved example of the same video type,” and add a concise publication checklist with the required fields and the exact output to update afterward (video-links log, repo embeds, Substack connection/notification).

### E. The parking lot mixes backlog items with long, unqualified advisory prose

- **Evidence:** `parking-lot.md` begins as a backlog, but the section “Substack - leveraging behind-the-scenes content” includes a long block introduced as “Perplexity’s commentary,” including prescriptions such as “Using ‘At the bench / production notes’ as the primary home for process is perfect” and quantified “80–90%” / “10–20%” splits.
- **Why this is weak:** The file is intended to preserve deferred ideas, but this prose reads like a prospective standard while remaining unratified and sometimes uses noncanonical series names. It makes a future reader work to distinguish an idea, a decision, and an adopted rule.
- **Concrete repair:** For each backlog entry, lead with **status** (*idea / experiment / adopted / superseded*), **next decision**, and **destination if adopted**. Move the full discussion to a dated incubator note or condense it into an action card. When adopted, promote the policy to Substack standards rather than letting the Parking Lot become a shadow style guide.

### F. The backup document is a machine-switching checklist, not yet a complete backup workflow

- **Evidence:** `backup-workflow.md` provides an excellent desktop-to-laptop sequence but only for that scenario; it does not say what “finished syncing” means for large video files, whether the sibling workflow-docs repo is included, what is intentionally excluded, or how recovery is verified.
- **Why this is weak:** The document’s title promises the broader operational policy that other workflows reference. The current material is useful but too narrow to govern capture ingest, completed video archival, or recovery after an accidental deletion.
- **Concrete repair:** Keep the laptop checklist intact, but precede it with a universal policy: covered roots, desired local/cloud status, verification method, retention tiers, and a minimal restore test. Then make the video-cleanup checkpoint cite that policy.

### G. The volume plan offers a compelling slate but lacks selection and closure criteria

- **Evidence:** The opening rule says each volume has four basic reel types plus an oddball/novel reel; later volumes include alternatives (“OR”), “TBD,” and partial lists. The Parking Lot proposes actions “after each volume,” but the plan never defines the closing condition.
- **Why this is weak:** Alternatives and TBDs are appropriate in an early slate, but the document also contains progress reporting. Without selection criteria (availability, condition, documentation, type balance, narrative value, bench complexity) and a closure rule, the reader cannot tell when an option must be resolved or whether a sparse later volume is provisional.
- **Concrete repair:** Add a one-paragraph selection rubric and a volume-close checklist. Mark each volume as **provisional** or **locked**; for provisional entries, give the decision needed and its trigger rather than only “TBD.”

## 5. What’s working well

- **The corpus has a real operating spine.** `index.md` separates the overview, service-guide, and looser Substack tracks cleanly, and it starts with acquisition/research rather than treating publication as an isolated writing task. The intent to make the hub the place that reduces decision fatigue is sound.

- **The documentation treats media as evidence, not decoration.** `image-workflow.md` is strongest where it connects service actions to images: “At least one image per user action/step,” hands/tools visible, parts organized, correct schematic names, and the distinction between sequence numbers and alternative versions. Those are the marks of a technical-documentation workflow rather than a generic content plan.

- **The template/skeleton philosophy is mature.** `skeletons-templates-workflow.md` correctly favors a developed, worked example over an empty form and explicitly frames a skeleton as “codified wisdom” extracted from finished work. That is an excellent basis for preserving voice and technical completeness while allowing the workflow to evolve.

- **The Substack standards make a valuable editorial distinction.** Separating a reader-facing series title from a behind-the-scenes tag is precise and useful; distinguishing Welcome, Production notes, Reel stories, and the completion-notification series gives the narrative work an intentional role alongside the technical work.

- **The documentation preserves experimentation without putting it in the main path.** The Parking Lot’s color, Pandoc, dramatism, remaster, and expanded-video ideas show a healthy system for retaining possibilities. Its “refactoring and harvesting” idea is especially good: promote durable insight to a canonical document and park the rest rather than forcing premature systematization.

- **The level of tool and asset specificity is often excellent.** Camera settings, lens starting points, Reaper/Shotcut artifacts, chapter-marker handling, and two-machine synchronization are concrete enough to support repeatable practice. The needed revisions are largely about connecting these strong local procedures into one unambiguous release and preservation system.
