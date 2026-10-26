# UI Sprite Separator

A personal-use, offline browser tool that automatically extracts separate transparent PNG sprites from a transparent PNG sprite sheet.

## Run locally

Open `index.html` in Chrome, Edge, or Firefox. No build process, accounts, dependencies, server, or internet connection are required.

## Usage

1. Upload a transparent PNG sprite sheet.
2. Adjust the alpha threshold, minimum component size and crop padding if needed.
3. Click **Separate Sprites**.
4. Preview the extracted sprites.
5. Click **Download ZIP** to download each sprite as a separate PNG.

## Limitations

Objects that touch or overlap in the image may be detected as a single sprite. Use transparent space between UI elements in the source sprite sheet.

## GitHub

This folder is ready to be uploaded as a repository. For private personal use, create a **private** GitHub repository called `ui-sprite-separator`, then upload `index.html`, `README.md` and `.gitignore`.
