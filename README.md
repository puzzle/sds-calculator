Digital Sovereignty Score (SDS) Calculator
=========================================

A small, static HTML/CSS/JS application that calculates the Digital Sovereignty Score (SDS) based on a weighted checklist across six dimensions.
See `HINTERGRUND.md` for background on the methodology and how the dimensions map to the ZenDiS criteria catalogue.

- Three-state answer per question (Ja / Teilweise / Nein), each contributing its individual weight to the score
- Live SDS calculation as a percentage (0–100%) and a score (0 - 6) with a qualitative label (e.g. "hoch ausgeprägt")
- Questions, weights, and help texts are defined in `questions.js`
- Accessible by default: native radio inputs per question (screen-reader and keyboard friendly out of the box)
- No dependencies or build steps (purely static)

## Project Structure
- `index.html` – Markup shell for the checklist and result area (rows are rendered from `questions.js`)
- `index.css` – Layout and styling in a monochrome blue infographic style
- `index.js` – Renders the checklist, handles selection and weighted score calculation
- `questions.js` – The six dimensions: question text, help text, and weight (must sum to 100)

  
## Run Locally

Two straightforward ways to run the project locally:

1. Open in the browser directly
   - Double-click `index.html` or open it via your browser's "File > Open" dialog.

2. Serve via a small local web server (recommended for consistent behavior)
   - Using Python 3:
     - Navigate to the project directory
     - Run: `python -m http.server 8000` (on Windows you can use `py -m http.server 8000`)
     - Open `http://localhost:8000/` in your browser and navigate to `index.html`
   - Using Node.js:
     - Run: `npx http-server -p 8000`
     - Open `http://localhost:8000/` in your browser
   - Alternatively: use the VS Code "Live Server" extension and open `index.html`

## Development

- No toolchain required. Edit `questions.js`, `index.html`, `index.css`, or `index.js` directly.
- The code runs without a bundler.

## License

See `LICENSE` in this repository.
