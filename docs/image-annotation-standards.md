# Image annotation standards

Usage: for annotating images, adding callouts, labels, etc.

## Workflow

In Affinity Photo, open the workspace `/affinity/` reel-annotation-aftemplate file.

In the Layers panel, select the old background image layer and hit Delete (or hide it if you want to keep a reference).

With the template still open:

    Select File > Place… > choose the image to be annotated > click in the canvas

    Drag handles to position / scale the image as needed so it fills the canvas

    Keep existing Callouts layer and all styles / swatches as they are.

    Save as a new Affinity file in the media folder `[maker]/[model]` as `[slug]-[desc]-annot.afphoto`

Add new ellipses / lines / frame text:

    **Ellipses**: In Swatches tab dropdown select Document - the swatches used in the template display - hover over a swatch to display the name - use `reel-callout-orange`

    Depending on the image background color, etc. it may be necessary to increase the pt size of the stroke from 1 px (default) to 2 px.

    The ellipse tool looks like a blue filled circle. Press SHIFT when clicking and dragging to constrain the circle ratio.

    **Text**: Text style: callout-label. Depending on the image background color, it may be necessary to change the text from black (default) to white.

    **Callout line**: Click the pen tool and select Pen (not node), click at edge of text box, click ellipse, click to draw line connected to both. Stroke style: callout-stroke.

Export the to the media folder using custom preset `annotated images` - settings: JPEG (High quality), 1024 px on long side, Lanczos 3 non-separable

The exported jpg can be opened in Xnview and batch converted and saved in the appropriate reel's project folder.

## Standards

Affinity template with all 3 standards is in workspace `/affinity/`

Snapping enabled for drawing lines between ellipses and text callout frames.

Export standards: default size from Xnview file should be 1024 on long side, jpg high quality, Lanczos 3 non-separable

Color: in Affinity swatches panel: reel-callout-orange
hex = CC6600

Text style for callouts: callout-label
Ariel black 9 pt., frame text tool
cap standards: all lower-case, only cap acronyms and proper names

Stroke style: in reel-callouts category, callout-stroke
1 pt., hex - CC6600, pen tool / line mode

