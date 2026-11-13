# MathStudio installable website

This folder is the MathStudio static website. It is published publicly with GitHub Pages from the `Napari21/mathstudio` repository. Visitors can install it in Edge or Chrome and use it offline after the first visit.

## Publish on GitHub Pages

The `.github/workflows/pages.yml` workflow publishes the files from the `main` branch. GitHub Pages is set to deploy through **GitHub Actions**. The site address is [https://napari21.github.io/mathstudio/](https://napari21.github.io/mathstudio/).

The repository and source files are public. HTTPS is used for installation, offline caching, and microphone access. Choose **Install app** in Edge or Chrome to install MathStudio.

## Using MathStudio

- Tap or click the whiteboard and type; your text appears on that same board as you enter it. On phones and tablets, tapping **Type** or the board opens the device keyboard.
- Choose **Draw**, **Eraser**, **Pointer**, or **Highlight** to sketch on top of the typed working on the same board. Choose **Type** again to continue entering text.
- Use **Clear board** to remove both the text and drawings. Undo restores a clear; Undo and Redo also apply to drawing strokes.
- Click or tap a palette symbol to insert it at the text cursor on the board.
- Use **＋** to add steps. Select a step in the lesson list; **Delete step** removes the selected one.
- Choose **Write on** or **Show all**, then use the preview controls or Play lesson to review the steps.
- Select a step and press **Record**. Allow microphone access, then speak while typing or drawing; press **Stop** when finished. Recording runs until you stop it, and lesson preview replays voice with the captured typing timing.
- **Save** keeps the current lesson in this browser on this device. Use **Download lesson** for a portable `.mathstudio` file; **Open** imports one. Copy that file when moving between devices. This build has no account or cloud sync.

## Tested scope and limits

The website MVP implements typing directly on the shared board, editable multi-step working, responsive mouse/touch/stylus drawing tools, step narration capture and playback, preview/timeline, automatic browser saving, lesson-file download/import, install manifest, offline service worker, and 1920×1080 WebM video preview export.

Video export is currently silent WebM; MP4 encoding and narration mixed into exported video still need a server-side renderer. The board is larger on desktop and square on phones, with larger writing text. The progressive reveal animates typed text by character, not actual pen strokes. Voice and typed changes are captured together for lesson preview; typing events follow the voice recording timeline, but there is no automatic speech transcription or word-level alignment. Lessons stay in the browser unless manually downloaded, so there is no cloud backup or synchronization. Microphone access requires a secure HTTPS site and browser permission.

## Files

- `index.html`, `styles.css`, `app.js`: the web app
- `manifest.webmanifest`, `icon.svg`, `sw.js`: install and offline support
- `.github/workflows/pages.yml`: GitHub Pages deployment workflow
