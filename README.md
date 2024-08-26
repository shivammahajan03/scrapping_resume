# Resume Scrapper

## Project Overview

The Resume Scrapper project is a Python-based tool designed to extract essential information from resumes in PDF and DOCX formats. It utilizes the OpenAI API to accurately parse and extract details such as the candidate's name, email, current company, role, and skills. The extracted data is then compiled into a structured CSV file, making it easier to analyze and manage large volumes of resumes.

## Features

- **PDF and DOCX Parsing**: Supports extraction of text from both PDF and DOCX resume formats.
- **AI-Powered Extraction**: Leverages OpenAI's models to extract key resume details such as name, email, current company, role, and skills.
- **Batch Processing**: Processes all resumes in a specified directory and compiles the extracted information into a CSV file.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.x installed on your machine.
- Required Python packages:
  - `pandas`
  - `openai`
  - `fitz` (PyMuPDF)
  - `docx`
  - `os`

You can install the necessary packages using the following command:

```bash
pip install pandas openai pymupdf python-docx
```

## Project Setup

1. **Clone the Repository**: Clone the project repository from GitHub to your local machine.

    ```bash
    git clone https://github.com/your_username/resume_scrapper.git
    cd resume_scrapper
    ```

2. **Set Up OpenAI API Key**: 
   - Replace the placeholder `key = ""` in the code with your actual OpenAI API key.
   - Ensure you have appropriate access and limits set for your OpenAI account.

3. **Organize Resumes**: Place all the resumes you want to process in a directory. Update the `folder_path` variable in the code to point to this directory.

## Usage

To run the resume scrapper:

1. **Run the Script**: Execute the Python script to begin extracting resume details.

    ```bash
    python resume_scrapper.py
    ```

2. **Output**: The script will process all the resumes in the specified folder and save the extracted data in a CSV file (`final_extract_v1.csv`).

## Code Breakdown

- **extract_text_from_pdf(pdf_path)**: Extracts text content from a PDF file using the `fitz` library.
- **extract_text_from_docx(docx_path)**: Extracts text content from a DOCX file using the `python-docx` library.
- **OpenAI Integration**: Uses OpenAI’s API to process the extracted text and identify key information such as name, email, company, role, and skills.
- **Data Storage**: Converts the extracted information into a DataFrame and saves it as a CSV file.

## Future Enhancements

- **Enhanced Data Validation**: Implementing checks to ensure the accuracy and completeness of the extracted data.
- **Support for Additional File Formats**: Adding support for other resume formats like TXT, RTF, etc.
- **GUI Integration**: Developing a user-friendly graphical interface to make the tool more accessible.
