# Ghost Signal

Ghost Signal is a browser-based time-series investigation tool created for the Kiroween 2026 Frankenstein category. It combines robust statistical heuristics with a detective-style evidence board: import a CSV, inspect flagged points on a timeline, and export findings for follow-up.

## Try it locally

Open `index.html` in a modern browser, or serve this directory with `python3 -m http.server 8000` and visit `http://localhost:8000`. Choose **Explore sample case** for a self-contained demonstration, or upload a CSV with a header row, a timestamp column parseable by JavaScript, and a numeric value column. Select the columns and sensitivity in the investigation panel. Files are processed locally in the browser and are not uploaded to a server.

## Detection and limitations

The app compares values and consecutive changes against their medians using median absolute deviation (MAD). A zero-MAD fallback flags sufficiently large deviations. Time gaps are estimated from the median positive interval; market closures and other scheduled gaps can be flagged. Detection is heuristic and findings are not evidence of cause, financial advice, or a substitute for checking source data. Missing or invalid values are omitted. This is intended for exploratory analysis, not automated decision-making.

## Kiroween

Category: **Frankenstein**. The project stitches statistical signal analysis, interactive visualization, and a case-file narrative into a single investigation experience. The `.kiro` directory contains project steering; document actual Kiro usage in the submission after using it. Do not claim tools, hooks, or workflows that were not actually used.

## License

MIT, see [LICENSE](LICENSE).
