# Document Metadata Extractor

A powerful tool that extracts comprehensive metadata from documents using advanced AI and NLP techniques. This notebook runs entirely in Google Colab, making it accessible to anyone with a web browser.

##  Live Demo

**Web Application**: [Document Metadata Extractor](https://metadataai-bymars.onrender.com/)
The website is hosted on render, it might take sometime to coldstart linl:https://metadataai-bymars.onrender.com/
##  Project Overview

This project extracts rich metadata from uploaded documents including:
- **Keywords**: AI-powered keyword extraction
- **Entities**: Author, organization, and publication date detection
- **Summary**: Intelligent document summarization
- **Document Statistics**: Word count, character count, file size
- **Processing Metadata**: Timestamps and processing information

### Supported File Formats
- **PDF**: Text-based and image-based (OCR processing)
- **DOCX**: Microsoft Word documents
- **TXT**: Plain text files

##  Tech Stack

### Core Technologies
- **Python**: Primary programming language
- 
### Document Processing
- **pdfminer.six**: PDF text extraction
- **python-docx**: DOCX file processing
- **pdf2image**: PDF to image conversion for OCR
- **pytesseract**: Optical Character Recognition (OCR)

### AI & NLP
- **spaCy**: Named Entity Recognition (NER)
- **KeyBERT**: Keyword extraction using BERT embeddings
- **Transformers**: Text summarization with BART model
- **NLTK**: Natural language processing utilities

### System Dependencies
- **Tesseract OCR**: Image-to-text conversion
- **Poppler**: PDF processing utilities

##  How to Run on Google Colab

### Step 1: Open the Notebook
1. Go to [Google Colab](https://colab.research.google.com)
2. Upload the `Copy_of_Untitled1.ipynb` file
3. Or create a new notebook and copy the code cells

### Step 2: Install Dependencies
The first cell automatically installs all required packages:

### Step 3: Run All Cells
1. Execute all cells in sequence (Runtime → Run all)
2. Wait for all packages to install (may take 5-6 minutes)
3. The interactive upload widget will appear

### Step 4: Upload and Process Documents
1. Click the "Upload Document" button
2. Select a PDF, DOCX, or TXT file
3. Watch the real-time progress bar
4. View extracted metadata and download results
5.if it takes too long, upload smaller file or rerun the last cell
## 📊 Features

### Interactive Interface in live website
- **Drag-and-drop file upload**
- **Real-time progress tracking**
- **Visual feedback with progress bars**
- **One-click JSON download**

### Advanced Processing
- **Multi-format support**: PDF, DOCX, TXT
- **OCR capabilities**: Extract text from image-based PDFs
- **Smart text extraction**: Automatic fallback to OCR when needed
- **Entity recognition**: Identify authors, organizations, dates
- **Keyword extraction**: AI-powered keyword identification
- **Text summarization**: Generate concise document summaries


### Processing Pipeline
1. **File Upload**: Secure temporary file handling
2. **Text Extraction**: Format-specific extraction methods
3. **OCR Fallback**: Automatic OCR for image-based PDFs
4. **NLP Processing**: Parallel entity and keyword extraction
5. **Summarization**: AI-powered text summarization
6. **Metadata Assembly**: Structured output generation
7. **Download**: JSON export functionality

##  Use Cases

### Academic Research
- Extract metadata from research papers
- Identify authors and institutions
- Generate paper summaries
- Extract key concepts and keywords

### Business Intelligence
- Process business documents
- Extract company information
- Identify key stakeholders
- Generate executive summaries

### Content Management
- Organize document libraries
- Extract metadata for indexing
- Generate content summaries
- Identify document themes

### Legal and Compliance
- Process legal documents
- Extract key entities and dates
- Generate document summaries
- Identify relevant parties

### Common Issues

**Package Installation Errors**
- Restart runtime and run cells again
- Check Colab's GPU/TPU settings
- Ensure stable internet connection

**OCR Processing Issues**
- Verify Tesseract installation completed
- Check PDF file quality and size
- Try with smaller files first

**Download Issues**
- Check browser download settings
- Verify file permissions
- Try different browser
.

