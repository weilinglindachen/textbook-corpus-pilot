# Textbook Corpus Builder (HGCT Format)

## Overview
This Python script is tailored for building a corpus from textbook data, specifically formatted to be compatible with the HGCT (Historical Grade Chinese Textbooks) Query Tool. It processes textbook data from a CSV file, organizes it into a structured format, and saves it in a directory, ensuring compatibility with the HGCT tool.

## Features
- Semester Identification: Converts grade information into semester format, aligning with HGCT requirements.
- Lesson Filtering: Filters and maps lesson information to fit the HGCT format.
- Metadata Construction: Builds metadata for each textbook entry, adhering to HGCT standards.
- Subcorpus Creation: Generates text files for each entry in the corpus, formatted for HGCT.
- Corpus Building: Reads from a CSV file and organizes the data into a structured corpus suitable for HGCT.
- Metadata File Generation: Creates YAML files for text and time metadata, compatible with HGCT.

## Requirements
- Python 3.x
- Standard Python modules: csv, re, pathlib
- Custom modules: textbook.configs, textbook.pipes
- A CSV file with textbook data in the specified format

## Usage
- CSV File Preparation: Format your CSV file with columns for ID, subject, grade, year, publisher, type, lesson, title, and content, as per HGCT standards.
- Set File Paths: Define the path to your CSV file and the output directory for the corpus.
- Script Execution: Run the script to process the CSV file and output the corpus in the specified directory, formatted for HGCT.
- Output Verification: The script generates text files for each entry and two YAML files (text_meta.yaml and time.yaml) containing metadata, all compatible with HGCT.

## Functions
- get_semester(grade: str): Converts grade to semester format for HGCT.
- filter_lesson(lesson: str): Filters and maps lesson information for HGCT compatibility.
- build_time_meta(semester: str, year: str, grade: str, time_meta: dict): Constructs time-related metadata for HGCT.
- build_subcorpus(filename: str, content: str): Creates a subcorpus text file formatted for HGCT.
- build_corpus(csv_file: str, corpus_folder: str, encoding: str = "utf-8"): Main function to build the corpus from the CSV file for HGCT.

## Error Handling
- The script includes checks for the existence of the CSV file and raises an exception if it is not found.

## Customization
- Adjust NUMERAL_MAPPING and ORD_MAPPING in textbook.configs for specific lesson and grade mappings.
- Modify the regular expressions in filter_lesson and build_subcorpus for different formatting requirements.

## Note
- This script is part of a larger project and is designed to work with specific modules (textbook.configs, textbook.pipes). Ensure these modules are correctly set up in your Python environment for successful execution. The output is specifically formatted to be compatible with the HGCT Query Tool.



