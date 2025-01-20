# PDF Splitter Script

This Python script splits a multi-page PDF into single-page PDFs. The resulting files can be named either sequentially or based on the MD5 hash of the content. You can specify the input PDF and the output folder through command-line arguments.

## Features

- Split a PDF into individual pages.
- Name the output PDFs either sequentially (e.g., `file_1.pdf`, `file_2.pdf`) or based on the MD5 hash of the page's content (e.g., `abc123.pdf`).
- Flexible output folder creation.

## Requirements

- Python 3.x
- Required libraries:
  - `PyMuPDF` (install using `pip install pymupdf`).
  - `argparse` (typically included with Python standard library).
  - `hashlib` (included with Python standard library).

## Usage

### Command-Line Arguments

- `-i`, `--input_pdf` (required): Path to the input PDF file that will be split.
- `-o`, `--output_folder`: Folder where the single-page PDFs will be saved. If not provided, the output folder will be created in the same directory as the input PDF with the base name of the input PDF.
- `-s`, `--sequential`: Optional flag to use sequential numbering for output files. If not set, the output files will be named based on the MD5 hash of the content.

### Example

#### 1. Split PDF with Sequential Naming

```bash
python split_pdf.py -i input.pdf -o /path/to/output/folder -s
