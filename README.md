# SahayakAI Documentation

## Overview

SahayakAI is a Streamlit web application designed to translate English PDF documents into Hindi. It leverages the power of the Cohere API to provide accurate and context-aware translations. The application has a user-friendly interface that allows users to upload a PDF, view the original and the translated document side-by-side, and download the translated version.

## Modules

### main.py

This module contains the core functionality of SahayakAI.

#### Classes

- `PDF(FPDF)`
  - A subclass of `FPDF`, it is used to create a PDF document with custom header and footer. It includes the Hindi font 'AnnapurnaSIL-Regular.ttf'.

#### Functions

- `extract_text(pdf_path)`
  - Extracts text from a given PDF file.
- `aya_translation(input_text, cohere_api_key)`
  - Translates the provided text into Hindi using the Cohere API.
- `save_text_to_pdf(text, filename)`
  - Saves the given text into a PDF file with the specified filename.
- `process_pdf(file_path, cohere_api_key)`
  - Extracts text from a PDF file, translates it, and saves the translation into a new PDF file.

### app.py

This module is responsible for the Streamlit web interface of SahayakAI.

#### Streamlit Interface

- Page configuration and title are set.
- A file uploader is provided for users to upload their PDFs.
- Original and translated PDFs are displayed side-by-side.
- Provides a download button for the translated PDF.

#### Key Components

- File uploader to accept PDF files.
- Display of the original PDF using base64 encoding.
- Spinner to indicate translation in progress.
- Temporary saving of the uploaded file for processing.
- Cleanup of the temporary file after use.

## Usage

To use SahayakAI:

1. Open the Streamlit application.
2. Upload a PDF file in English using the file uploader.
3. View the original document on the left side.
4. Wait for the translation to complete (indicated by a spinner).
5. View the translated document in Hindi on the right side.
6. Download the translated PDF using the provided download button.

## Installation and Setup

To set up SahayakAI:

1. Clone the repository containing `main.py` and `app.py`.
2. Install the required libraries: `streamlit`, `fitz`, `fpdf`, `cohere`.
3. Obtain a Cohere API key and set it in `app.py`.
4. Run the Streamlit application using `streamlit run app.py`.

## Dependencies

- Streamlit: For creating the web application.
- Fitz (PyMuPDF): For extracting text from PDFs.
- FPDF: For creating PDF documents.
- Cohere API: For translation services.

## Note

Ensure that the 'AnnapurnaSIL-Regular.ttf' font file is available in the same directory for proper rendering of Hindi text in the PDFs.

---

This documentation provides a comprehensive overview of SahayakAI, detailing its functionality, usage, and setup requirements.
