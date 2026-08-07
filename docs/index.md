# Repo description

john-tech-writer.github.io/stack-project-docs

*created 8.6.26*

This repository / site / project is mainly intended to provide a general-purpose skeleton for creating a media stack for technical documentation. In this model, a Github repository anchors the core technical content, YouTube hosts video content, and Substack hosts narrative content. 

This stack models a robust workflow for known, well-researched technical authoring best practices:
  - Short overviews to provide context and explain concepts.
  - Illustrated procedures that clearly demonstrate tool use.
  - Short videos to give a general feel for a procedure and show specific moves difficult to capture in still photos or text.
  - Narrative content for a wider sense of context.
  - A notification hub for updates.

This model is suitable for procedural docs, conceptual / overview docs, and reference docs. If you are familiar with the DITA model, all this will seem very familiar. Also important, this site both explains and models how to organize the content in meaningful ways beyond the full-text search.

In this stack design, the media stack elements provide a ready-made audience platform for video and narrative content which points back to the core technical documents that live in the repository:

```mermaid

flowchart TD
  A[Github repository - technical content hosting]
  A --> Y[YouTube channel - video content hosting]
  A --> S[Substack - narrative and notification hub]

```

The media elements not only widen the audience reach of the repository, they also provide appropriate containers for content that doesn't fit the strictly technical nature of the repository.

This skeleton / model is suitable for a wide range of projects, from hardware-oriented maintenance and repair work to software-based workflows. The project documents here were developed over the course of about six months in parallel with a real demo project, which can be viewed at vintage-reel-service-guides.com.

The documents include not only general guidelines and structure, but also prompts to help kick-start the process of authoring content. They also include more specific, concrete instructions for tool use, which is often a very time consuming aspect of new projects. For example, basic instructions are provided for using Shotcut to create and edit videos.

This is a growing and evolving repository and will be updated regularly based on successive refactoring passes on real projects. The knowledge gained from real-work projects will be used to contiunously update this repository and add to it, making it a more useful toolkit as it grows and matures. All this project history is recorded in the [Changelog](changelog.md).

# Project philosophy

**Let the real work teach what the theory should look like**. As project content is developed, the workflow can also be abstracted and made concrete. Iterations on lived and living, dynamic examples result in constant improvement.

Workflow documentation informs ongoing content development and the content development in turn informs the evolution of the workflow. This includes processes, naming standards, software tools, and all the rest of the machinery that moves the project forward and makes content stylistically coherent and repeatable.

This file is the **one place** to always return to push the project a little further: cleaning dirs, tightening steps, wiring pieces together.

Every pass makes the project flow better: clearer naming, better links, more honest reflection of how project work is actually accomplished, not some abstract ideal.

Leaning on it solves decision fatigue: if the stack feels overwhelming - slugs / naming, badge / design, Substack / narrative, YouTube / video, reels / content sourcing - `project-workflow.md` can be opened, reviewed, worked on, and will move the project one notch higher. **That counts**.

# Project standards and workflow

This workflow file provides the basic roadmap for navigating, creating, and managing all project content - it serves as the index for the site. Disciplined naming standards and skeletons / templates codify important principles so authors do not have to reinvent the wheel over and over.

The basics of project development and management are to understand the workflow and file organization, to know what documents guide the project, and to have a place to record ideas for the future. These other key files:

- [README](orientation.md): Orientation to the internal project documentation.

- [Parking lot](parking-lot.md): List of project upgrades and ideas for future iterations.

- [Directory layout](directory-layout.md): Diagram of all project directories and notes on their contents.

## Naming and slugs

All reels and other project content sources are assigned a slug for easy and consistent identification across all directories and usages.

See [Naming and slugs](naming-slugs.md).

## Skeletons and templates

All content is based on skeletons / templates which enforce evolving content standards and help jog memory and ideas.

See [Skeletons and templates workflow](skeletons-templates-workflow.md).

## Workflow - overviews

1. Select reel based on [Volume planning](volume-planning.md), acquire.

    Add an entry for the reel in workspace `reference docs and books/reel collection.docx`. This file is a record of when each reel was acquired, cost, origin, and notes on what's been done / needs to be done for each reel.

2. Acquire all available documentation for the reel, save in workspace `maker and reel docs/[maker]/[slug]-[desc].[ext]` and add entries to project folder `docs/references.md`.

    Typical docs include schematics, parts lists, box inserts, user manuals, patents, and articles from the ORCA archives.

    If documents and / or box is included with reel, take photos and save in project folder `/docs/[maker]/[slug].[pdf / jpg / etc.]`. Also if docs are not copyrighted and are available outside pay walls (e.g., ORCA archives), then they can be included in the project. These images are treated as documents, linked from the References page, and included in the project so users can view them using the link provided in the References page.

    If documents are obtained from other sources, the files are not included in the project. The source link will be provided in the References page but users may need to pay to view the documents (e.g., ORCA online archives).

3. Take initial photos of reel in one piece using the standards in [Image workflow](image-workflow.md). Save to the Pictures media folder `/maker and reel docs/[maker]/[slug]-[desc].jpg`.

    These images will be used initially / primarily for the repo overview. Secondarily some will be used later in the workflow for the repo service guide, videos, and substack posts - anywhere an image of the reel intact is useful.

    For info on how to use grids on the Olympus PL1 camera and in Shotcut, as well as principles of framing and grid use, see in the workspace `photo-video-grids-framing.md`

    After taking the initial pictures, sync updated project folders to Dropbox as described in [Backup workflow](backup-workflow.md).

4. Open Pictures folder using [XnView](https://www.xnview.com/en/xnview/) and batch rename / batch convert. See [Image workflow](image-workflow.md)

    Save to Project folder `docs/img/[maker]/[model]/[slug]-[desc].jpg` using Tools > Batch convert > Output tab

5. Write substack post for "Welcome to the bench" series.

    See [Substack standards and series](substack-standards-series.md) and See [Skeletons and templates workflow](skeletons-templates-workflow.md).

6. Write overview using skeleton in project folder `repo skeletons/` and save in project folder as `docs/[maker]/[slug]-overview.md.` This will get pushed to the repo.

7. Create overview video. Follow the procedure in [Audio - video workflow](audio-video-workflow.md).

## Workflow - service guides

1. Take a second round of images while disassembling and reassembling reel. Save to the Pictures media folder `/maker and reel docs/[maker]/sg/[slug]-[desc].jpg`

    These images will be used initially / primarily for the repo service guide. Some of the service guide images will also be taken from the overview images (reel intact). Secondarily some will be used later in the workflow for videos and substack posts - anywhere an image of the reel intact is useful.

    After taking the second round of photos, sync updated project folders to Dropbox as described in [Backup workflow](backup-workflow.md)

2. Write service guide using skeleton in project folder `repo skeletons/` and save in project folder as `docs/[maker]/[slug]-service-guide.md.` This will get pushed to the repo.

3. Create service guide videos, usually two but sometimes more. Follow the procedure in [Audio - video workflow](audio-video-workflow.md).

4. Write substack post for "Service guides" series.

    This post is intended as the main notification (Substack serves as the "hub") for new completed stacks - overview and service guides on the repo and videos on YouTube.

    See [Substack standards and series](substack-standards-series.md) and See [Skeletons and templates workflow](skeletons-templates-workflow.md).

## Workflow - Substack

The other couple of Substack series can be published on a looser schedule. See [Substack standards and series](substack-standards-series.md).

When service is completed on a reel, write one or more "Reel stories," about test casting, taking it into the field, how it performs, how it is integrated with other tackle to make a balanced outfit, what fish are sought and caught.

"Production notes" can be published anytime as occasional features. Progress milestones during a stack production run make good subjects, like how the lighting is done / changed / etc.