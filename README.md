# DavireDivijaNandana_Girl-Hackathon_SWE_2025
# Intelligent Process Automation - AI Solution



## Overview

This project automates repetitive business processes such as document processing, data entry, and customer service interactions using AI.



## Features:

- *Document Processing*: Uses OCR + NLP to extract key data from invoices/receipts.

- *Automated Data Entry*: RPA fills forms automatically.

- *AI Chatbot*: Answers customer queries using NLP.



## Setup Instructions:

### Prerequisites

1. Install Python (>=3.8)

2. Install required dependencies:

   bash

   python -m pip install --upgrade pip setuptools wheel

   pip install flask pytesseract opencv-python spacy

   

3. Download and install the SpaCy language model:

   bash

   python -m spacy download en_core_web_sm

   

4. Ensure Tesseract OCR is installed on your system:

   - *Windows*: Download from [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki)

   - *Linux/macOS*: Install via package manager (e.g., sudo apt install tesseract-ocr)



### Running the Application

1. Start the Flask server:

   bash

   python script.py

   

2. Use Postman or Curl to send a POST request with an image to /process-document:

   bash

   curl -X POST -F "file=@invoice.jpg" http://127.0.0.1:5000/process-document

   



### API Endpoint

- *POST /process-document*

  - *Input*: Image file (e.g., invoice, receipt)

  - *Output*: Extracted text and structured data (JSON format)



### Expected JSON Response Example

json

{

  "Entities": [

    ["Amazon", "ORG"],

    ["$500", "MONEY"],

    ["February 25, 2025", "DATE"]

  ]

}





## Troubleshooting & Common Issues

- *Installation Errors*:

  - Ensure all dependencies are installed (pip install -r requirements.txt).

  - If using Windows, install *Microsoft C++ Build Tools* for SpaCy.

- *OCR Accuracy Issues*:

  - Improve preprocessing by using OpenCV filters (grayscale, thresholding).

- *Flask API Not Running*:

  - Ensure port 5000 is available and firewall allows access.



## Future Enhancements

- Integrate AI chatbot for real-time customer interactions.

- Improve NLP pipeline with domain-specific models.

- Add automated RPA workflows for seamless business automation.



---

*Contributors:* Nandana & Team | Google Girl Hackathon 2025 🚀
