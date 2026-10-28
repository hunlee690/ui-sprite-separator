# UI Sprite Separator

A personal-use, offline browser tool that automatically extracts separate transparent PNG sprites from a transparent PNG sprite sheet. Each detected component is exported with a precise alpha mask, so unrelated pixels inside its rectangular crop are cleared.

## Run locally

Open `index.html` in Chrome, Edge, or Firefox. No build process, accounts, dependencies, server, or internet connection are required.

## Usage

1. Upload a transparent PNG sprite sheet.
2. Adjust the alpha threshold, minimum component size, transparent padding and anti-aliased edge recovery if needed.
3. Click **Separate Sprites**.
4. Preview the extracted sprites.
5. Click **Download ZIP** to download each sprite as a separate PNG.

## Limitations

PNG canvases are always rectangular, but pixels outside each detected shape are transparent. Objects that touch or overlap may still be detected as a single sprite. Use transparent space between UI elements in the source sprite sheet.

## Edge handling

Detection starts from pixels at or above the selected alpha threshold (default: 128). This keeps faint background residue, shadows and glow from joining otherwise distinct UI elements. Increase the threshold if objects remain grouped; lower it for intentionally translucent artwork. Very high thresholds can split translucent details into extra pieces.

Edge recovery includes nearby pixels below the threshold, preserving soft anti-aliased outlines without copying every pixel inside the bounding box or taking solid pixels from another component. Recovery does not merge detected components. PNGs with a fully opaque background still require background removal first.
