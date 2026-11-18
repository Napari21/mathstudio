# MathStudio installable website

This folder is the MathStudio static website. It is published publicly with GitHub Pages while its source is kept in the `Napari21/mathstudio` repository. Once hosted over HTTPS, visitors can install it from Edge or Chrome and use it offline after the first visit.

## Publish on GitHub Pages

The repository uses .github/workflows/pages.yml to publish the files automatically from the main branch. The GitHub Pages source is set to **GitHub Actions**. After a successful workflow, the public site is at [https://napari21.github.io/mathstudio/](https://napari21.github.io/mathstudio/).

The repository must remain public for GitHub Free Pages. The site and source are public. The site needs HTTPS for installation, offline caching, and microphone recording. You can install it in Edge or Chrome using **Install app**.

## Using MathStudio

- Tap or click the whiteboard and type; your text appears on that same board as you enter it. On phones and tablets, tapping **Type** or the board opens the device keyboard.
- Choose **Draw**, **Eraser**, **Pointer**, or **Highlight** to sketch on top of the typed working on the same board. Choose **Type** again to continue entering text.
- Use **Clear board** to remove both the text and drawings. Undo restores a clear; Undo and Redo also apply to drawing strokes.
- Click or tap a palette symbol to insert it at the text cursor on the board.
- Choose Whiteboard, Blackboard, or Grid under Background. Blackboard writing and pen strokes switch to light chalk colors. Import background accepts PNG, JPEG, or WebP images up to 20 MB; the image is resized and embedded in the lesson file.
- Use **A−** and **A+** to adjust typed writing from 24 to 96 pixels. The side math keyboard has numerator and denominator boxes for inserting a fraction, plus square-root, power, and subscript templates and a broader set of math/science symbols.
- Build a lesson as scenes: give each scene a title and duration, duplicate it, or move it up/down. The timeline shows the order and total length.
- Open **Math visuals and shapes** in the side panel to add a number line, coordinate axes, fourths bar, multiplication array, circle, rectangle, or triangle directly to the board. These are editable with the existing undo, redo, eraser, and clear controls.
- A lesson can stay on one board from beginning to end. While recording, keep writing and scroll the same board to continue; you do not need to add another step. Use **＋** only when you want a separate lesson segment.
- Choose **Write on** or **Show all**, then use the preview controls or Play lesson to review the steps.
- Preview at 0.5×, 1×, 1.5×, or 2×. Export as landscape (16:9), vertical (9:16), or square (1:1), at 720p or 1080p, and 24/30/60 fps. Turn narration on or off before exporting. Browser codec support determines whether the downloaded file is MP4 or WebM; higher frame rates and resolutions depend on the device and browser.
- Expand **Prepare YouTube upload** to edit a title, description, and tags, then download a local notes file with chapter timestamps. Use those notes when uploading manually.
- Press **Record**, allow microphone access, then speak while typing and scrolling the board. Press **Stop** when the continuous lesson is finished. Preview replays the voice with captured typing and scroll timing.
- **Save** keeps the current lesson in this browser on this device. Use **Download lesson** for a portable `.mathstudio` file; **Open** imports one. Copy that file when moving between devices. This build has no account or cloud sync.

## Tested scope and limits

MathStudio remains a no-cost static site. It now includes editable scene organization and duration controls, common math-diagram/shape stamps, selectable white/black/grid/imported-image boards, font sizing, a docked math/science keyboard with fraction and expression templates, responsive pointer drawing, narration with typing/scroll timing, playback speed control, export profiles for aspect ratio/resolution/frame rate/narration, and a local YouTube metadata/chapters helper. Projects are saved locally in the browser or exported as lesson files. The site is hosted on free GitHub Pages; no paid service or API key is used by this build.

Export rendering runs on the user’s device and generally takes about the lesson duration; keep the page open until the download starts. MP4 and 60 fps are browser-dependent; WebM is the fallback. Scene-diagram stamps are static line drawings; this release does not have an object-motion keyframe editor or scene transitions. Fractions can be entered in the keyboard and illustrated with a fraction bar, but the equation text itself is still plain text rather than a full typesetting editor. There is no live graph/slider engine, symbolic math checker, waveform editor, noise reduction, cloud sync, or direct YouTube upload. Adding cloud storage or authenticated YouTube publishing would require separate account/API setup; the current free site does not send lesson data to a server. Microphone access needs HTTPS and browser permission.

## Files

- `index.html`, `styles.css`, `app.js`: the web app
- `manifest.webmanifest`, `icon.svg`, `sw.js`: install and offline support
- `netlify.toml`, `_headers`: static hosting settings
