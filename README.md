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
- A lesson can stay on one board from beginning to end. While recording, keep writing and scroll the same board to continue; you do not need to add another step. Use **＋** only when you want a separate lesson segment.
- Choose **Write on** or **Show all**, then use the preview controls or Play lesson to review the steps.
- Press **Record**, allow microphone access, then speak while typing and scrolling the board. Press **Stop** when the continuous lesson is finished. Preview replays the voice with captured typing and scroll timing.
- **Save** keeps the current lesson in this browser on this device. Use **Download lesson** for a portable `.mathstudio` file; **Open** imports one. Copy that file when moving between devices. This build has no account or cloud sync.

## Tested scope and limits

The website MVP implements typing directly on the shared board, editable multi-step working, responsive mouse/touch/stylus drawing tools, step narration capture and playback, preview/timeline, automatic browser saving, lesson-file download/import, install manifest, offline service worker, and 1920×1080 WebM video preview export.

Video export is currently silent WebM; MP4 encoding and narration mixed into exported video still need a server-side renderer. The board is larger on desktop and square on phones, with larger writing text. The progressive reveal animates typed text by character, not actual pen strokes. Voice, typed changes, and board scroll position are captured together on the active step for lesson preview. Recording continues until you press Stop; extra steps are optional segments, not required for long lessons. There is no automatic speech transcription or word-level alignment. Lessons stay in the browser unless manually downloaded, so there is no cloud backup or synchronization. Microphone access requires a secure HTTPS site and browser permission.

## Files

- `index.html`, `styles.css`, `app.js`: the web app
- `manifest.webmanifest`, `icon.svg`, `sw.js`: install and offline support
- `netlify.toml`, `_headers`: static hosting settings
