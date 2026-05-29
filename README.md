# Pregnancy Calculator

A lightweight, browser-based Estimated Due Date (EDD) calculator. Enter a reference date and the current gestational age in weeks and days, and the app estimates the due date based on a standard 40-week pregnancy timeline.

## Features

- Calculates an estimated due date from:
  - Reference date in `yyyy-mm-dd` format
  - Weeks pregnant
  - Days pregnant
- Runs entirely in the browser with no server or build step required
- Uses plain HTML, CSS, and JavaScript
- Provides basic validation for required fields, date format, and date validity

## How the Calculation Works

The calculator treats 40 weeks as 280 days. It subtracts the entered gestational age from 280 days, then adds the remaining days to the reference date:

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
├── index.html   # Single-page EDD calculator app
├── LICENSE      # MIT license
└── README.md    # Project documentation
```

## Usage Notes

- The reference date should be entered as `yyyy-mm-dd`.
- Weeks should be between `0` and `42`.
- Days should be between `0` and `6`.
- The result is an estimate and should not replace medical advice from a qualified healthcare professional.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
