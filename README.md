# Python PDF Generator

A Python project that generates multi-page, notebook-style PDF documents from data stored in a CSV file.

The project uses **FPDF** to create and format the PDF and **Pandas** to read and process the CSV data. Each topic can have multiple pages, with automatically generated headers, footers, and ruled writing lines.

## Features

* 📄 Generates PDF documents automatically
* 📑 Creates multiple pages for each topic
* 📝 Adds notebook-style horizontal writing lines
* 🏷️ Automatically adds the topic name as a header
* 🔖 Adds the topic name as a footer
* 📊 Reads topic and page information from a CSV file
* 🔄 Uses Python loops to generate pages dynamically

## Technologies Used

* **Python**
* **FPDF** — PDF generation
* **Pandas** — CSV data processing

## Project Structure

```text
python-pdf-generator/
│
├── main.py
├── topics.csv
├── output.pdf
└── README.md
```

## CSV Format

The project expects a CSV file containing the topic and number of pages to generate.

Example:

```csv
Topic,Pages
Python Basics,3
Web Scraping,5
Python Automation,4
```

The `Topic` column determines the title displayed on the PDF, while the `Pages` column determines how many pages are generated for that topic.

## How It Works

The program reads the CSV file using Pandas:

```python
df = pd.read_csv("topics.csv")
```

It then loops through each topic:

```python
for index, row in df.iterrows():
```

For every topic, the program creates the required number of pages.

Notebook-style writing lines are generated using a loop:

```python
for y in range(20, 298, 10):
    pdf.line(10, y, 200, y)
```

This changes the vertical position of each line and creates a ruled-paper effect across the page.

## Installation

Clone the repository:

```bash
git clone https://github.com/Fonexspec/python-pdf-generator.git
```

Navigate into the project:

```bash
cd python-pdf-generator
```

Install the required dependencies:

```bash
pip install fpdf pandas
```

## Running the Project

Make sure `topics.csv` is in the same directory as the Python script.

Then run:

```bash
python main.py
```

The generated PDF will be saved as:

```text
output.pdf
```

## What I Learned

This project helped me practice:

* Python functions
* `for` loops
* Working with CSV files
* Pandas DataFrames
* Iterating through DataFrame rows
* Generating PDFs with Python
* Creating multiple PDF pages
* Positioning elements on a PDF
* Automating repetitive tasks

## Future Improvements

Possible improvements include:

* Adding customizable page sizes
* Adding different line spacing options
* Allowing custom fonts
* Adding page numbers
* Adding user-defined margins
* Adding PDF form fields for typed input
* Creating a simple interface for generating PDFs

## Author

**Funsho David Akinyele (Fonexspec)**

This project was created as part of my journey learning Python and developing skills in automation and data processing.
