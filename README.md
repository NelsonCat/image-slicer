# Image Grid Slicer

A browser-based image slicing tool for **GitHub Pages**. Upload an image, choose a grid from **2×2 to 6×6**, preview the slices, and download all output images as a **ZIP** file.

## Features

- Upload **JPG**, **PNG**, or **GIF** images
- Choose **columns** from 2 to 6
- Choose **rows** from 2 to 6
- Slice the image into evenly divided parts
- Preview the source image with grid lines
- Preview every output tile before downloading
- Download all slices as a single **ZIP** file
- Runs entirely in the browser — no backend required
- Ready to deploy on **GitHub Pages**

## Demo URL Format

After deployment, your site will be available at:

https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY-NAME/

Example:

https://nelsoncat.github.io/image-slicer/

## How It Works

1. Upload an image file.
2. Enter the number of columns.
3. Enter the number of rows.
4. Click **Slice image**.
5. Preview all sliced parts.
6. Click **Download ZIP** to save the output.

## Supported File Types

- `.jpg`
- `.jpeg`
- `.png`
- `.gif`

## Notes About GIF Files

GIF files can be uploaded, but this tool slices the image as rendered by the browser. It does **not** export animated GIF slices frame-by-frame.

## Project Files

index.html   Main application file
README.md    Project documentation

## Run Locally

Because this is a static browser app, you can usually open `index.html` directly in a browser.

If you prefer a local web server, you can use one of these options:

### Python

python -m http.server 8000

Then open:

http://localhost:8000

### VS Code Live Server

If you use VS Code, you can also open the project folder and launch it with the **Live Server** extension.

## Deploy to GitHub Pages

### Option 1: Deploy from a branch

This is the easiest option for this project.

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Commit the files to the `main` branch.
4. Open the repository on GitHub.
5. Go to **Settings → Pages**.
6. Under **Build and deployment**, set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/root`
7. Save the settings.
8. Wait 1 to 3 minutes for the site to go live.

## Usage Guide

### Upload an image

Click the file picker and choose a supported image.

### Set the grid size

- Columns: `2` to `6`
- Rows: `2` to `6`

### Slice the image

Click **Slice image** to generate the tiles.

### Preview output

The app shows:

- The source image with overlaid grid lines
- A preview card for every generated slice

### Download the result

Click **Download ZIP** to save all slices in a single archive.

## Output File Naming

Generated files are named using row and column order, for example:

myphoto_r1_c1_01.png
myphoto_r1_c2_02.png
myphoto_r2_c1_03.png

This makes it easy to reconstruct the original order later.

## Technical Details

- Built with plain **HTML**, **CSS**, and **JavaScript**
- Uses the browser **Canvas API** to slice images
- Uses **JSZip** to generate ZIP downloads in the browser
- No server, database, or build pipeline required

## Limitations

- Animated GIFs are not exported as animated slices
- Very large images may use more memory in the browser
- Output format is currently exported as **PNG** for consistency

## Customization Ideas

Possible future improvements:

- Drag-and-drop upload
- Dark mode
- Custom output filename prefix
- Fixed output dimensions for each tile
- Optional transparent padding around slices
- Individual tile download buttons
- Multiple export formats

## License

You can use and modify this project for personal or internal use. If you plan to publish or distribute it broadly, add the license that matches your intended use.

## Credits

Built as a lightweight static tool intended for deployment on **GitHub Pages**.
