# Pregnancy Calculator

A lightweight, dependency-free Estimated Due Date (EDD) calculator that runs entirely in the browser. Enter a reference date and the current gestational age in weeks and days, and the app estimates the due date using a standard 40-week pregnancy timeline.

> **Note:** This calculator provides an estimate only and is not a substitute for guidance from a qualified healthcare professional.

## Features

- Calculates an estimated due date from:
  - Reference date selected with the browser's native date picker
  - Weeks pregnant
  - Days pregnant
- Updates the result automatically as values are entered or changed
- Includes a shortcut button to set weeks and days to `0`
- Provides validation for:
  - Required fields
  - Date format and valid calendar dates
  - Weeks between `0` and `42`
  - Days between `0` and `6`
- Runs as a static single-page app with no dependencies, server, or build step

## How the Calculation Works

The calculator treats a full-term pregnancy as 40 weeks, or 280 days. It converts the entered gestational age to days, subtracts that value from 280, and adds the remaining days to the reference date.

```text
estimated due date = reference date + (280 - ((weeks pregnant * 7) + days pregnant)) days
```

For example, if the reference date is `2026-05-29` and the pregnancy is `12` weeks and `3` days along:

```text
days pregnant = (12 * 7) + 3 = 87
remaining days = 280 - 87 = 193
estimated due date = 2026-05-29 + 193 days
```

## Project Structure

```text
.
├── index.html   # Single-page EDD calculator app with inline CSS and JavaScript
├── LICENSE      # MIT license
└── README.md    # Project documentation
```

## Development Notes

- Keep the app dependency-free unless a future task explicitly requires tooling.
- Preserve the static-site structure so `index.html` can be opened directly in a browser.
- The application logic, styling, and markup currently live in `index.html`.
- For behavior changes, manually test the affected calculator flow in a browser when possible.

## Usage Notes

- The reference date should be entered or selected in `yyyy-mm-dd` format.
- Weeks should be a whole number from `0` through `42`.
- Days should be a whole number from `0` through `6`.
- Due dates can vary based on clinical context; use this result as an estimate only.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
