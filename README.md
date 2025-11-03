# ATS compatible Resume Creator Agent

This project is an AI-powered Resume Creator agent implemented in a Jupyter Notebook. It automates the process of generating ATS (Applicant Tracking System) optimized resumes from user-uploaded PDF files and additional textual inputs.

## Features

- Extracts plain text from uploaded PDF resumes.
- Accepts additional free-text inputs to customize the resume.
- Searches for ATS-compatible resume templates using Google Custom Search API.
- Uses OpenAI's ChatGPT (via LangChain/OpenAI integration) to choose the best resume template based on the extracted data.
- Polishes and generates the resume in HTML format optimized for ATS.
- Converts the polished HTML resume into a downloadable PDF file.

## Technologies Used

- Python 3.12
- LangGraph for stateful process graph orchestration
- LangChain OpenAI integration (`ChatOpenAI`)
- OpenAI GPT models (GPT-4o-mini)
- Google Custom Search JSON API for template discovery
- PDF processing with `pypdf`
- HTML to PDF conversion with `pdfkit` (requires wkhtmltopdf)
- Web scraping with BeautifulSoup for Google search results parsing

## Setup and Installation

1. Clone the repository.

2. Install dependencies (use a virtual environment):

3. Install `wkhtmltopdf` on your system for PDF generation:

- On Ubuntu/Debian:

- On Windows, download from [wkhtmltopdf.org](https://wkhtmltopdf.org/downloads.html) and add to PATH.

4. Set environment variables for API keys:

Alternatively, adjust these values inside the notebook script environment section.

## Usage

Run the Jupyter notebook `Resume_Creator.ipynb` step-by-step or import the functions into your Python environment.

The main function is:


- `pdf_file_path`: Path to the user's resume PDF file.
- `additional_input`: Additional free text inputs to customize the resume content.

The function outputs a path to the generated ATS-optimized resume PDF.

Example:

## Workflow Overview

- Extract text from PDF resume.
- Accept additional input from user.
- Search Google for ATS-compatible resume templates.
- Evaluate and select the best template using AI scoring.
- Generate polished ATS-optimized HTML resume.
- Convert HTML to PDF and save output.

## Notes

- The notebook uses multiple API keys for OpenAI calls and randomly picks one each time.
- Rate limits of OpenAI API need to be handled for large documents.
- Google Custom Search requires a valid API key and CSE ID with proper quota.
- PDF generation depends on the external `wkhtmltopdf` utility installed and accessible in the system PATH.

## License

Specify your license here (e.g., MIT License).

## Acknowledgements

- [LangGraph](https://github.com/langgraph/langgraph) for stateful agent orchestration.
- OpenAI for GPT models used in content generation.
- Google Custom Search for template discovery.
- `pdfkit` and `wkhtmltopdf` for HTML to PDF conversion.

---

Feel free to contribute or report issues to improve this Resume Creator agent project.






