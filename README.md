# LaTeX Studio

https://pedrobovolindavila.github.io/latex-studio/latex-studio-standalone.html

A lightweight, browser-based LaTeX editor designed to make technical writing easier for engineering students. LaTeX Studio combines a code editor and live preview with visual tools for mathematical notation, tables, matrices, electrical circuits, and block diagrams. It also includes keyboard shortcuts, technical-writing suggestions, and `.tex` export.

> **Interface language:** Portuguese (Brazilian Portuguese). This README is written in English for the project repository.

## Why this project?

Writing technical reports, solving equations, and documenting engineering projects often means switching between a text editor, symbol references, and separate diagram tools. LaTeX Studio brings common tasks into one workspace, helping students spend less time looking up syntax and more time working on the technical content.

The project is especially useful for students who are learning LaTeX or frequently write mathematical and electrical-engineering documents. Its goal is to make LaTeX more approachable without hiding the source code: users can insert content with buttons and shortcuts, then inspect and edit the generated commands directly.

## Features

### LaTeX editor and live preview

- Edit LaTeX source in a dedicated text area.
- Preview supported text structures and mathematical expressions as you type.
- Render supported mathematical expressions using MathJax.
- Use a responsive layout with light and dark color schemes; the default follows the browser/operating-system color preference.
- Set a document title, author, and document class (`article` or `report`).

### Mathematical symbols and keyboard shortcuts

- Search the symbol library by name or command.
- Insert common structures such as fractions, roots, powers, subscripts, sums, integrals, limits, derivatives, vectors, and delimiters.
- Browse Greek letters, operators, relations, arrows, functions, font styles, and electrical-engineering notation.
- Use keyboard shortcuts for frequently used commands, including formatting, fractions, roots, superscripts, subscripts, inline/display math, comments, and Greek symbols.
- Enable or disable the symbol shortcut sequences.

### Tables, matrices, and equation systems

- Generate tables by choosing the number of rows and columns, alignment, border style, and optional caption.
- Choose full borders, horizontal rules in a `booktabs` style, or no borders.
- Generate bracketed, parenthesized, determinant-style, or brace-style matrices.
- Turn a list of equations into a `cases` or `align*` environment.

### Electrical-circuit builder

Create circuit sketches on a grid using components including:

- Resistors, capacitors, and inductors
- Voltage and current sources
- Diodes, switches, and lamps
- Wires and ground symbols

The canvas supports horizontal and vertical connections, component labels, undoing the last action, clearing the canvas, changing the grid size and zoom, and a full-screen view. The tool can insert the resulting circuit as LaTeX using the `circuitikz` package.

### Block-diagram builder

- Create a series of labeled blocks from a comma-separated list.
- Toggle a feedback path.
- Insert the diagram as a TikZ picture in the LaTeX source.

### Formatting and figures

- Insert sections, subsections, equations, lists, references, labels, footnotes, comments, and page breaks.
- Apply bold, italic, underline, superscript, subscript, highlighting, text color, and font-size commands.
- Insert a figure template with a filename and optional caption.

### Technical-writing assistance

- Show basic writing statistics, including word count, sentence count, average sentence length, and estimated reading time.
- Provide automatic suggestions for issues such as long sentences or paragraphs, informal or vague terms, repeated words, and missing explanations around equations or references.
- Offer a small vocabulary bank of academic transitions and technical verbs.

The writing suggestions are **rule-based heuristics**, not an AI-powered review service. They are intended as prompts for revision, not as a substitute for careful proofreading.

### Export and local persistence

- Copy the generated LaTeX document or download it as a `.tex` file.
- Export a document skeleton with a title, author, selected class, and commonly used packages, including `amsmath`, `graphicx`, `booktabs`, `tikz`, and `circuitikz`.
- Remember the recent source, title, and author in browser storage, so the editor can restore the last session in the same browser context.

## Getting started

LaTeX Studio is a single HTML file. No package installation, build tool, server, or backend is required for basic use.

1. Download or clone this repository.
2. Open `latex-studio-standalone.html` in a modern web browser.
3. Type LaTeX directly into the editor or use the tabs and toolbar to insert structures.
4. Enter a document title and author, and select `Article` or `Report` as appropriate.
5. Use **Export .tex** to copy or download the full LaTeX source.
6. Compile the exported `.tex` file in [Overleaf](https://www.overleaf.com/) or with a local LaTeX distribution to produce the final document.

### External resources

The HTML file loads MathJax 3.2.2 from jsDelivr for mathematical rendering and Google Fonts for typography. An internet connection is therefore needed for those external resources. The editor itself does not require a backend or send documents to a project server.

## Exported LaTeX document

The exported source includes a document class (`article` or `report`), a Brazilian Portuguese language setup, page geometry, and packages used by the insertion tools. For circuit and block diagrams, the export uses `circuitikz` and `tikz` respectively.

If your document uses external images, place those image files where your LaTeX compiler can find them and check that the filenames match the `\includegraphics{...}` commands. Additional packages may be needed for commands or environments that you add manually.

## Important notes and limitations

- **The preview is not a full LaTeX compiler.** It converts a selected subset of LaTeX structures for display and uses MathJax for supported mathematical expressions. Some commands, packages, custom macros, references, figures, or environments may not appear exactly as they will in a compiled PDF.
- **Compile before submission.** The exported `.tex` file, compiled with a real LaTeX engine, is the source of truth for the final document layout and whether the document compiles successfully.
- **Figure preview:** image commands may appear as placeholders in the browser preview; the image itself must be available to the LaTeX compiler when the document is compiled.
- **Diagram preview:** the visual preview is tailored to diagrams created with the built-in circuit and block-diagram tools. Arbitrary TikZ or `circuitikz` code may not be fully represented in the preview.
- **Browser storage:** session recovery relies on browser storage and may behave differently depending on browser settings and how the HTML file is opened. Export important work regularly.
- **External dependencies:** MathJax and Google Fonts are loaded from third-party CDNs.

## Technologies

- HTML5
- CSS3 (responsive layout and light/dark color schemes)
- Vanilla JavaScript
- [MathJax 3](https://www.mathjax.org/)
- TikZ and CircuitikZ commands generated for LaTeX export

## Project structure

```text
.
├── latex-studio-standalone.html   # Complete application (HTML, CSS, and JavaScript)
└── README.md                      # Project documentation
```

## Contributing

Bug reports, usability suggestions, and feature ideas are welcome. When proposing changes, please include the browser used, steps to reproduce the issue, and a small LaTeX example when relevant.

## License

No license is currently specified in this repository. Add a `LICENSE` file before redistributing the project under an open-source license.
