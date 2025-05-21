# AI Medical Report Analyzer 🩺

<!-- Add a banner image if available -->

An advanced Streamlit application that leverages Gemini AI to analyze medical reports (PDFs and images) and provide structured insights including diagnoses, medication recommendations, lifestyle guidance, and disease classification.

## Features ✨

- **Multi-format Support**: Upload PDFs or images (JPG, PNG) of medical reports
- **Comprehensive Analysis**:
  - Key findings extraction
  - Potential diagnoses with confidence levels
  - Medication recommendations with dosages and side effects
  - Personalized lifestyle guidance (diet, exercise, sleep)
  - Disease classification (chronic, infectious, common)
- **Interactive Visualizations**:
  - Medication effectiveness comparison charts
  - Disease classification pie charts
- **Professional Reporting**:
  - Structured tabbed interface
  - Downloadable full report
  - Printable format

## Technology Stack 🛠️

- **Backend**: 
  - Python 3.10+
  - Streamlit (Web Framework)
  - Google Gemini AI (Medical Analysis)
- **Text Processing**:
  - pdfplumber (PDF extraction)
  - pytesseract (OCR for images)
- **Visualizations**:
  - Matplotlib (Charts)
  - Lottie Animations (UI Enhancements)

## Installation ⚙️

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/medical-report-analyzer.git
   cd medical-report-analyzer
2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
3. Install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
4. Set up environment variables:
   - Create a .env file in the root directory
   -  Add your Gemini API key: 
   ```bash
   GEMINI_API_KEY=your_api_key_here
5. Install Tesseract OCR (required for image processing):
   - Windows: Download from UB Mannheim
   - Mac: brew install tesseract
   - Linux: sudo apt install tesseract-ocr

## Usage 🚀

1. Run the application
   ```bash
   streamlit run app.py
2. Open your browser to the provided local URL (usually http://localhost:8501)
3. Upload your medical report (PDF or image) and click "Analyze Report with AI"
4. View the structured results across multiple tabs

## Limitations ⚠️

1. **AI Model Constraints**:
   - Accuracy depends on the Gemini 1.5 Flash model's training data (knowledge cutoff: ~2023)
   - May struggle with highly specialized medical terminology or rare conditions

2. **Input Quality**:
   - PDFs must have selectable text (scanned PDFs require clear OCR)
   - Images require high resolution (minimum 300dpi recommended)
   - Handwritten notes are not supported

3. **Medical Scope**:
   - Focused on diagnostic reports (not designed for imaging analysis like X-rays/MRIs)
   - Medication recommendations may not account for all drug interactions
   - Lifestyle advice is generalized, not personalized nutrition plans

4. **Technical Requirements**:
   - Requires stable internet connection for AI analysis
   - Tesseract OCR must be installed locally for image processing
   - Performance may vary with large (>10 page) documents

5. **Regulatory**:
   - Not FDA-approved or clinically validated
   - Should only be used as a supplementary tool
   - Always verify results with a licensed healthcare provider

6. **Language Support**:
   - Currently optimized for English-language reports
   - Translations may lose medical nuance
