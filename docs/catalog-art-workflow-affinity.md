# Workflow: Catalog Reel Image to Cleaned Exports in Affinity

This workflow documents a practical process for turning a scanned vintage catalog image into clean black-and-white exports with either transparent or white backgrounds using Affinity Designer 1.10.x. The key ideas are to isolate the catalog region first, work on the actual pixel layer rather than adjustment layers, use low-tolerance Flood Select for paper removal, and set document background transparency in Document Setup before exporting PNGs.

## Scope

This workflow is aimed at scanned catalog pages rather than true vector PDFs. If the source PDF is a scan, the illustration should be treated as raster artwork and cleaned as a pixel image rather than edited as vector geometry.

There is a good chance that most of the catalogs, etc. in the ORCA archives will be of this type, scanned pages.

## Recommended output set

For each reel image or catalog plate, keep three versions:

- An editable `.afdesign` master with the cleaned pixel layer and any adjustment layers intact.
- A PNG with a transparent background for reuse in layouts and web graphics.
- A PNG or JPG with a white background for quick document use where transparency is unnecessary.

## Step 1: Open the PDF and isolate the target page

Open the catalog PDF in Affinity Designer and limit import to the pages needed for the current task. In the Layers panel, locate the actual image layer for the target page, then right-click that page image and use **Rasterize & Trim** so the page becomes a manageable raster working surface without extra imported pages hanging around.

The catalogs will generally come from ORCA. Add a reference entry to the project folder `/docs/references.md` and cite in specific pages where derived images are used.

The catalogs are saved in workspace as `/maker and reel docs/[maker]/[maker]-[year]-[type]-cat.pdf`

Save the extracted page in media folder Pictures as `/[maker]/cat art/[maker]-[year]-cat-p[#].afdesign`

Usage: a reference copy to go back to for text references / info, original image without mods, etc.

## Step 2: Pull out the reel area as a new working document

In Pixel Persona, [icons in upper left] use the Rectangular Marquee Tool to draw a box around the reel image or plate to be extracted. With that selection active, copy it and use **File → New from Clipboard** to create a new document sized exactly to the selected area; this is a reliable workaround when crop behavior is inconsistent in Affinity Designer 1.10.x.

## Step 3: Save a working master immediately

Before any modifications, save the new clipped document as an `.afdesign` file. This preserves the isolated source region and makes it easy to back up if later selections or deletions become too aggressive.

Save in media folder Pictures as `/[maker]/catalog art/[desc]-[year]-cat-p[#].afdesign`

## Step 4: Resize once to a better master size

If the new clipped document is relatively small, resize it once to a larger working size such as roughly 1500 to 2000 pixels wide in **Document setup**. Use **Lanczos (non-separable)** rather than Bilinear when enlarging line art, because Lanczos preserves edge sharpness better than softer interpolation methods.

Specs in Document setup:

Type: Web
Dimensions: lock aspect ratio, 1800px x whatever
DPI: 300
Resample: Lanczos 3 non-separable

## Step 5: Improve contrast with Levels

Note: This step is useful for older or smudgy images, to help the next step (flood) work better. For better quality images it may not be needed to get a clean flood, but can still serve to optionally sharpen up the image.

Add a Levels adjustment layer and darken the black point while pushing the white point toward a cleaner paper tone. This step strengthens the printed reel lines and makes background removal easier, but it should be done gently so highlight detail on the reel is not flattened into the paper.

## Step 6: Remove paper background carefully

Select the actual pixel layer before using any selection tools; Flood Select will not behave correctly if the Levels adjustment layer is selected instead. In Pixel Persona, use the Magic wand / Flood Select Tool with a low tolerance, often around 10 percent, and click only obvious background areas so the tool targets the white paper without eating into light reel highlights.

Delete selected paper in several small passes instead of trying to remove everything at once. If the tool starts selecting part of the reel, undo immediately and reduce tolerance; on scanned catalog art, preserving highlights is more important than removing every speck of paper in one click.

Note: In Document setup Color tab check Transparent background, save, and if a white background version is wanted also uncheck and save again. If recoloring b&w images set Color format: RGB/8

## Step 6a: Cropping

In Designer persona, select the crop tool and drag frame handles to define area. Switch to Pixel persona, ctrl + C to copy, File > New from clipboard, save.

For reels and other tackle, save a version with any text, context, design elements, etc. in media folder Pictures as `/[maker]/cat art/[desc]-[year]-cat-p[#]-trans.afdesign`

Also save a version without text (eraser tool).

For fish images, save a version with just ID text in media folder Pictures as `/fish images/[species]-[year]-[maker]-cat-p[#]-[mods].afdesign` Use these images to start an appendix page common-gamefish.md, currently (july 2026) this is linked from the references.md page.

It may also make sense to compile a master appendix of all the reel art, although this may also make more sense to just include with individual reels, like the nobby-models.md page.

Also save a version without text (eraser tool).

## Step 7: Finish edges by hand

After the major paper areas are deleted, press **Ctrl+D** to clear the marching-ants selection before using the Eraser tool. Then use a small, soft eraser on the pixel layer to remove any text, etc. and just leave the target image.

Save a version with any text, context, design elements, etc. in media folder Pictures as `/[maker]/catalog art/[desc]-[year]-cat-p[#]-trans-text-removed.afdesign`

## Step 8: Keep the document export-ready

If the goal is a transparent PNG, make sure the document itself has a transparent background. In Affinity Designer 1.10.x, this is controlled in **File → Document Setup → Colour → Transparent background**, not in the PNG export dialog itself.[3][7]

Also verify that there is no white-filled rectangle or dedicated white background layer under the artwork unless a white export is desired. PNG transparency depends on both the document background setting and the absence of opaque background layers.[8][19]

### Export presets

catalog-line-art-800px

## Step 9: Export transparent and white-background versions

For the transparent version, leave **Transparent background** enabled and export as PNG. For the white-background version, either disable the transparent document background or place a white layer below the artwork before export; both methods produce a solid white result while preserving the transparent-capable master file.

If only a specific object or cropped area should export, use the appropriate export area such as **Selection only**. If the document has already been cropped tightly, **Whole Document** is usually the simplest choice.

Export to media folder Pictures as `/[maker]/catalog art/[slug]-[year]-cat[mods].png`

### Cleaning up artifacts in artwork

Use case: A white (or other solid color) catalog page has smudges, spots, etc.

1. In Pixel persona, add a pixel layer on top of the artwork layer.

2. Click the dropper (color picker) tool and click on a white area. May need to click in the color tab the fill / stroke icons.

3. Select the brush tool and adjust the width as needed.

4. Brush white over the artifacts, zoom in and out, etc.

### Resizing canvas

Use case: this resizes the canvas, not the art.

File > Document settings > click the Anchor to Page button > click an anchor point to determine which part of the canvas will be enlarged | click the padlock to unlock dimensions | resize and export

## Troubleshooting notes

### Flood Select grabs part of the reel

Lower tolerance and target only the cleanest paper regions first. Scanned print art often has highlight tones close to the background, so aggressive selection settings can remove real image detail.

### Eraser appears to do nothing

Check that the pixel layer, not an adjustment layer or empty layer, is selected. Also clear any active selection with **Ctrl+D**, because the Eraser only affects the currently selected area while marching ants are active.

### PNG export has a white background

Turn on **Transparent background** in **Document Setup → Colour** and make sure there is no visible white layer underneath the artwork. In Affinity Designer, transparency is controlled by the document and layer stack, not by a prominent PNG checkbox in the export panel.

### Crop or canvas controls seem inconsistent

In older Designer builds, selection plus **File → New from Clipboard** is often the most reliable way to turn a chosen catalog region into a tightly cropped working file. This avoids version-specific crop tool confusion and gets straight to a clean isolated image.

## Suggested naming convention

A simple naming pattern keeps assets organized:

- `brand-model-year-cat-master.afdesign`
- `brand-model-year-cat-transparent.png`
- `brand-model-year-cat-white.png`

For example:

- `pflueger-nobby-skilkast-1955-cat-master.afdesign`
- `pflueger-nobby-skilkast-1955-cat-transparent.png`
- `pflueger-nobby-skilkast-1955-cat-white.png`

## Minimal checklist

- Open the PDF and isolate the page image.
- Rasterize and trim the page layer.
- Marquee the reel area and create a new document from clipboard.
- Save the `.afdesign` master.
- Resize once with Lanczos if a larger master is needed.
- Use Levels to improve contrast.
- Flood Select the paper at low tolerance and delete in small passes.
- Deselect and clean edges with a soft eraser.
- Enable transparent background in Document Setup if needed.
- Export transparent and white-background deliverables.