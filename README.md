# Intelligent Pre-Toll Processing and Dynamic Lane Management System

LaTeX source for the Bachelor of Engineering Stage-1 project report **Intelligent Pre-Toll Processing and Dynamic Lane Management System**.

The report proposes an intelligent toll-plaza prototype that combines RFID vehicle identification, camera-based number-plate recognition, ESP32 control, OLED status feedback, servo-operated barriers, and dynamic lane management.

## Contents

- `main_report.tex` - Main LaTeX source file and report entry point.
- `main.pdf` - Existing PDF output from the workspace.
- `main.docx` - Existing editable document source/output.
- `*.jpg` - Existing image assets in the workspace.

The report includes the title pages, certificate, table of contents, list of figures, abstract, acknowledgement, abbreviations, introduction, literature review, methodology, results and discussions, conclusions, future scope, and references.

## Requirements

Install a LaTeX distribution with the packages used by the document:

- macOS: [MacTeX](https://www.tug.org/mactex/)
- Windows/Linux: TeX Live

The document uses packages including `graphicx`, `geometry`, `tikz`, `float`, `array`, `booktabs`, `longtable`, `ragged2e`, `setspace`, `titlesec`, `enumitem`, `hyperref`, and `caption`.

## Build

From the project directory, compile the report with:

```bash
pdflatex -interaction=nonstopmode main_report.tex
pdflatex -interaction=nonstopmode main_report.tex
```

Running LaTeX twice updates the table of contents and list of figures. If `latexmk` is installed, the equivalent command is:

```bash
latexmk -pdf -interaction=nonstopmode main_report.tex
```

The generated PDF is written to `main_report.pdf`. Auxiliary files such as `.aux`, `.log`, `.out`, and `.toc` can be removed after compilation if they are not needed.

## Important Notes

- Compile from the repository root so relative image paths resolve correctly.
- `main_report.tex` uses the `\projectimage` helper. Missing figures are replaced by visible placeholders, so absent images do not prevent compilation.
- The figure filenames expected by the source are `block-diagram.png`, `flowchart.png`, `plate-detection-result.png`, `vehicle-detection-result.png`, `wokwi-simulation.png`, and `simulation-result.png`.
- The current workspace contains older `.jpg` assets, but not all expected `.png` figures. Add the final figures with the names above when they are available.
- The report is explicitly a prototype and distinguishes planned integrations from completed testing. Update the Results chapter with measured results before submission.

## Project Scope

The proposed toll-management system is designed to:

1. Identify vehicles using RFID tags.
2. Detect vehicles and recognize number plates using computer vision and OCR.
3. Compare RFID-linked records with recognized plate text.
4. Reject unknown tags, mismatched plates, unreliable OCR, and insufficient balances.
5. Demonstrate two-lane management with ESP32-controlled servo barriers.
6. Display local transaction status through an OLED and optionally support Blynk monitoring.

## Authors

- Prathmesh Warkhede
- Omkar Sonawane
- Omkar Walse

Guide: Prof. R. R. Katkar  
Department of Electronics & Telecommunication Engineering  
Sinhgad College of Engineering, Vadgaon (BK), Pune  
Academic year: 2026--2027