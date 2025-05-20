# 📄 Industrial Instrumentation Report Generator

A dynamic, browser-based tool to generate professional **calibration and inspection reports** for industrial instrumentation. Built with **HTML**, **Bootstrap**, **Chart.js**, and **html2pdf.js**, this application enables users to enter instrumentation data, draw calibration charts, capture signatures, and export a structured, styled PDF report — all without any server-side code.

---

## 🚀 Features

- 🔧 Add multiple instruments dynamically
- 📊 Live preview of calibration vs. actual data charts using **Chart.js**
- 🧮 Automatic generation of calibration error tables (% error)
- ✍️ Digital inspector signature pad
- 🖋 Reviewer/approver name field
- 📄 Generates a **print-ready PDF report** using **html2pdf.js**
- 🎨 Clean dark UI with well-structured, printable report styling

---

## 📂 Project Structure

- **HTML** – The full application interface is contained in a single HTML file.
- **CSS** – Inline styles handle dark-mode UI and PDF report formatting.
- **JavaScript** – Used for form handling, chart rendering, PDF export, and digital signature capture.

---

## 🛠 Technologies Used

| Tool/Library | Purpose |
|--------------|---------|
| [Bootstrap 5.3](https://getbootstrap.com) | Responsive form layout |
| [Chart.js](https://www.chartjs.org/) | Line graph visualization |
| [html2pdf.js](https://github.com/eKoopmans/html2pdf) | PDF generation from HTML |
| [Signature Pad](https://github.com/szimek/signature_pad) | Capture digital signatures |

---

## 🧾 How to Use

1. **Open `index.html`** in any modern web browser (Chrome, Edge, Firefox).
2. Fill in the document details such as header, environmental conditions, calibration procedure, and uncertainty.
3. Enter data for each instrument:
   - Instrument type, manufacturer, model, range, accuracy, calibration dates
   - Inspection result and description
   - Calibration and actual data (comma-separated)
4. Draw the **inspector's signature** in the provided signature pad.
5. Add **additional instruments** as needed with the “Add Another Instrument” button.
6. Click **"Generate PDF"** to download a fully formatted calibration report.

---

## 📸 PDF Output Includes

- Document header and info
- Environmental and procedural details
- Individual instrument sections with:
  - Calibration numbers
  - Data tables and line charts
  - Error tables (% deviation)
  - Signature and reviewer details

---

## ⚠️ Known Limitations

- This is a **static front-end app**; no data is stored or persisted.
- Reviewer signature field is prepared but not implemented in the UI (currently shows name only).
- Graph rendering and PDF generation may slightly vary across browsers.

---

## 🧪 Sample Use Case

Ideal for:

- Field engineers or QA technicians documenting calibration activities
- Internal SOP reporting for instrument checks
- Offline, client-side report generation without backend dependency

---

## 📝 Customization Tips

- Want to store reports? Integrate with `localStorage` or a backend.
- Add export to Excel with libraries like `SheetJS`.
- Implement digital timestamping or PDF encryption if required.

---

## 📄 License

This project is open-source and intended for educational and internal industrial use. Attribution appreciated if adapted.
