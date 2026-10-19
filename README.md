# Verity

AI-text and source-overlap checker that runs entirely in the browser. No server, no APIs, no uploads.

## Run
Open `index.html` in a browser, or serve the folder (`python3 -m http.server`) and visit http://localhost:8000.

## Deploy on GitHub Pages
Push this folder to a repo, then Settings → Pages → Deploy from branch → `main` / root.

## How detection works
- Style signals: sentence-length burstiness, vocabulary diversity, formal wording, stock AI phrases, transition-led sentences, repetition, contractions, informal markers.
- Optional on-device model (Transformers.js, downloaded once; weight capped at 35%). If it can't download, style signals are used alone.
- Source overlap: TF-IDF cosine + n-gram containment against a local reference library (Admin page).

Scores are probabilistic estimates, not proof of authorship.
