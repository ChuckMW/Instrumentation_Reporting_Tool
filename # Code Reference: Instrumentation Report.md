# Code Reference: Instrumentation Report Generator

## Overview

This project is a web-based Industrial Instrumentation Report Generator.  
It allows users to input instrument details, calibration data, and inspector signatures, then generates a styled PDF report with calibration charts and error tables.

---

## Main Technologies & Libraries

- **Bootstrap 5** (MIT License): UI styling and layout  
  CDN: https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css

- **Chart.js** (MIT License): Charting library for calibration graphs  
  CDN: https://cdn.jsdelivr.net/npm/chart.js

- **Signature Pad** (MIT License): Canvas-based signature capture  
  CDN: https://cdn.jsdelivr.net/npm/signature_pad@4.1.7/dist/signature_pad.umd.min.js

- **html2pdf.js** (MIT License): HTML to PDF conversion  
  CDN: https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js

---

## Key Files

### Instrument_Report.html

- **HTML Structure**
  - Form for entering document and instrument details
  - Dynamic instrument sections (add/remove)
  - Signature pad for inspector
  - Hidden div for PDF content

- **CSS**
  - Dark theme for app UI
  - Light theme for PDF output
  - Responsive and print-friendly styles

- **JavaScript**
  - Dynamic instrument section creation
  - Chart.js chart setup and live updating
  - Signature Pad initialization and clearing
  - Calibration number generation (unique per report/instrument)
  - PDF generation with html2pdf.js, including charts and error tables

---

## Important Functions

### `setupChartForInstrument(instrumentDiv)`
Initializes and updates a Chart.js line chart for each instrument section based on calibration and actual data input.

### `generateCalibrationNumber(idx)`
Generates a unique, complex calibration number for each instrument every time the report is generated.  
Format: `CAL-YYYYMMDD-<instrument#>-<random5chars>`

### PDF Generation
- Collects all form data and chart images
- Calculates % error for each calibration point
- Assembles a styled HTML report
- Converts to PDF using html2pdf.js and triggers download

---

## Licensing Notes

All third-party libraries used are MIT licensed and suitable for commercial/SaaS use.  
**If you distribute or monetize, include the MIT license text for each library.**

---

## Extending or Bundling

- Can be bundled with other industrial tools for SaaS
- Can be converted to a desktop app (Electron) with minimal changes
- User authentication, database storage, and multi-tenancy can be added for SaaS

---

## Example Calibration Number

```
CAL-20250519-2-AB12X
```
(Date, instrument index, random 5-character code)

---

## Author & Support

- For questions or support, contact the project maintainer.
- For library documentation, see the official sites for [Bootstrap](https://getbootstrap.com/), [Chart.js](https://www.chartjs.org/), [Signature Pad](https://github.com/szimek/signature_pad), and [html2pdf.js](https://github.com/eKoopmans/html2pdf.js).

---