# Financial Analysis from PDF with Azure OpenAI

This repository contains a Python application that extracts text from PDF financial reports, converts it to Markdown format, and sends it to Azure OpenAI for analysis using the o3 reasoning model.

## Overview

This project demonstrates how to build a simple Python application that:
1. Reads content from PDF financial statements
2. Converts the extracted text to Markdown format
3. Sends the formatted content to Azure OpenAI's reasoning model
4. Retrieves and formats the financial analysis
5. Generates both text and HTML reports with key financial insights

## Features

- PDF text extraction with page-by-page processing
- Markdown formatting of financial data
- Integration with Azure OpenAI o3 reasoning model
- Structured financial report generation
- HTML report visualization with key takeaways
- Email functionality to share generated reports

## Getting Started

### Prerequisites

- Python 3.7+
- Azure OpenAI API access (endpoint, key, and deployment)

### Installation

1. Clone this repository:
```
git clone https://github.com/sureshpaulraj/financial-reasoning.git
cd financial-reasoning
```

2. Create and activate a virtual environment:
```
python -m venv .venv
```

Windows:
```
.venv\Scripts\activate
```

3. Install the required dependencies:
```
pip install -r requirements.txt
```

### Configuration

Create a `.env` file in the project root with your Azure OpenAI credentials:
```
AZURE_OPENAI_API_KEY=your_api_key
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_DEPLOYMENT_ID=your_deployment_id
AZURE_API_VERSION="2024-12-01-preview"
```

## Usage

1. Place your financial PDF files in the `pdfs` directory
2. Run the Jupyter notebook `FinancialAnalysisFromPDF.ipynb`
3. The application will:
   - Extract text from each PDF
   - Format it as Markdown
   - Send it to the Azure OpenAI API
   - Generate formatted text and HTML reports

## Report Output

The program generates two types of reports:
1. A text report (`formatted_financial_report.txt`) with financial analysis
2. An HTML report (`financial_report.html`) with structured sections:
   - Introduction
   - Key takeaways on:
     - Balance Sheet Analysis
     - Income Statement Analysis  
     - Cash Flow Statement Analysis
   - Conclusion

## Additional Features

- Token counting for PDF files
- Email functionality to distribute reports
- Markdown to HTML conversion for better visualization
- Financial data extraction using Azure OpenAI's function calling

## Dependencies

- PyPDF2 - For PDF text extraction
- requests - For API communication
- python-dotenv - For environment variable management
- PyMuPDF - For advanced PDF processing
- tiktoken - For token counting
- pydantic - For data validation and settings management
- openai - For Azure OpenAI API integration

## License

[Include your license information here]

## Acknowledgments

- Azure OpenAI for providing the reasoning model API
- PyPDF2 and PyMuPDF for PDF processing capabilities
