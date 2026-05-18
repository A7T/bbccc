# bbccc

[中文](README.md)

Browser-Based ChArUco Camera Calibration.

bbccc is a single-page camera calibration tool built around ChArUco boards. It runs in the browser, helps generate a printable calibration board, captures camera samples, solves calibration parameters with OpenCV.js, and exports the result as JSON.

The project name is short for "browser-based ChArUco camera calibration", but the tool itself is meant to stay straightforward: open the page, print a board, collect samples, calibrate.

## Use

Open the GitHub Pages site:

https://a7t.ink/bbccc/

Or download `docs/index.html` and open it locally in a browser.

For camera access, HTTPS is recommended. Local files may work depending on the browser, but browser camera permissions are stricter than ordinary page rendering.

## Features

- Load OpenCV.js in the browser.
- Generate a printable ChArUco calibration board.
- Check whether the board fits common paper sizes such as A4.
- Export high-resolution PNG and 1:1 PDF board files.
- Capture calibration samples from a USB camera.
- Filter samples by board area, marker count, Charuco corner count, and viewpoint diversity.
- Run camera calibration in the browser.
- Export calibration results as JSON.

## Privacy

Camera frames are processed locally in your browser. The tool does not upload camera images or calibration samples to a server.

Current builds load third-party JavaScript dependencies from CDNs, including OpenCV.js and jsPDF. A future release may provide a more self-contained single-file build.

## Development

The current version is intentionally simple:

```text
docs/
  index.html
  .nojekyll
```

GitHub Pages can publish this repository from `main / docs`.

The project may later move to a modern frontend toolchain, but preserving a convenient browser-first and preferably single-file distribution is a design goal.

## License

MIT License. See `LICENSE`.
