# Textbook Corpus Builder

This repository contains a Python package specifically designed for building a corpus of textbook content, formatted to be compatible with the [HGCT (Hanzi Glyph Corpus Toolkit) Query Tool](https://yongfu.name/hgct/index.html). The primary focus is on processing and organizing textbook data, including metadata related to the text content.

## Installation
To use this package, clone the repository and install the required dependencies.

1. Python version
```bash
Python >= 3.0
```

2. Clone repository

```bash
git clone git@github.com:weilinglindachen/textbook-corpus-pilot.git
```

3. Install Requirement

```bash
cd textbook-corpus-pilot && pip install -r requirements.txt
```

## Usage
### Building the Corpus

To build the corpus, use the `build_corpus` function from the corpus module. This function reads a CSV file containing textbook data and organizes the content into a structured corpus. Define the path to your CSV file and the desired output folder before calling the function:

```python
from corpus import build_corpus

# Path to the CSV file
csv_file = './data/教科書課文.csv'

# Name of the output folder
folder = "textbook_corpus"

# Building the corpus
build_corpus(csv_file, folder)
```
After running the `build_corpus` function, the newly generated `textbook_corpus` folder will be created in the project root, containing the structured corpus data.

```
|--- data/
|    |--- 教科書課文.csv
|--- textbook/
|--- textbook_corpus/ (newly generated)
|--- ...
```
