# PDF Merger (Python)

A lightweight command-line tool for merging multiple PDF files into one. It prompts the user for the number of PDFs, takes their filenames, and merges them using `PyPDF2` into a single output file called `merged-pdf.pdf`. 

---

## Features

* Prompts user for number of PDFs to merge.
* Accepts filenames dynamically.
* Merges all selected PDFs in the order provided.
* Outputs a single merged PDF.
* Uses `PyPDF2`’s `PdfWriter` for robust merging.

---

## How It Works

1. `PdfWriter()` is initialized to accumulate pages.
2. User specifies **how many PDFs** they want to merge.
3. Loop collects PDF filenames into a list:

   ```python
   for i in range(0, n):
       name = input(f"Enter the name of pdf {i + 1}: ")
   ```


4. Each PDF is appended to the writer:

   ```python
   merger.append(pdf)
   ```


5. Final merged file is saved as `merged-pdf.pdf`.

---

## Installation

### Install PyPDF2

```bash
pip install PyPDF2
```

---

## Usage

### Run the script:

```bash
python main.py
```

### Example Interaction

```
How many pdfs do you want to merge?
3
Enter the name of pdf 1: a.pdf
Enter the name of pdf 2: b.pdf
Enter the name of pdf 3: c.pdf
```

Output generated:

```
merged-pdf.pdf
```

---

## Requirements

* Python 3.x
* PyPDF2

---

## Notes

* Input filenames must include `.pdf` extension.
* Order of merging follows the order of user input.
* Ensure all files exist in the same directory as the script (or give full paths).

---


