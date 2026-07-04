# The Knockout — WC26 Bracket Predictor

Single-file, no-build static page for picking a World Cup 2026 knockout bracket
and sharing predictions as a URL. No backend, no build step — the whole app is
`index.html`.

- Live results: fetched client-side from [openfootball/worldcup.json](https://github.com/openfootball/worldcup.json).
- Sharing: your bracket is encoded entirely in the URL fragment (`#v2....`) —
  nothing is stored server-side.
- Publish: GitHub Pages, serving `index.html` from the repo root.

## Local development

Just open `index.html` in a browser, or serve it locally:

```
python3 -m http.server
```

(A plain `file://` open works too, since the live-fetch has CORS enabled;
only sandboxed iframe previews without network access fall back to the
embedded snapshot.)
