# Document Metadata Extractor

## 📋 Overview

The Document Metadata Extractor is an intelligent, AI-powered tool designed to automatically analyze and extract comprehensive metadata from various document formats. Built for Google Colab/Jupyter environments, this tool combines advanced Natural Language Processing (NLP) techniques with Optical Character Recognition (OCR) to provide deep insights into document content.

## 🎯 Key Features

- **Multi-Format Support**: Process PDF, DOCX, and TXT files seamlessly
- **AI-Powered Analysis**: Extract keywords, entities, and generate summaries using state-of-the-art NLP models
- **OCR Capabilities**: Handle image-based PDFs and scanned documents
- **Export Functionality**: Download results in structured JSON format
- **Visual Feedback**: Real-time progress indicators and processing status updates

## 🚀 Use Cases

- **Academic Research**: Quickly analyze research papers and extract key information
- **Document Management**: Automate metadata extraction for large document collections
- **Content Analysis**: Understand document themes, key topics, and authorship
- **Information Retrieval**: Create searchable metadata for document databases
- **Report Processing**: Extract executive summaries and key insights from business reports
- **Legal Document Analysis**: Identify key entities and dates in legal documents

## 🛠️ Technology Stack

### Document Processing
- **pdfminer.six**: PDF text extraction and parsing
- **python-docx**: Microsoft Word document processing
- **pytesseract**: OCR (Optical Character Recognition) for image-based text
- **pdf2image**: PDF to image as fallback for OCR processing

### Natural Language Processing
- **spaCy**: Named Entity Recognition (NER) and linguistic analysis
- **KeyBERT**: Keyword extraction using BERT embeddings
- **Transformers (Hugging Face)**: BART model for text summarization
- **NLTK**: Natural language toolkit for text processing

### System Dependencies
- **Tesseract OCR**: Open-source OCR engine
- **Poppler Utils**: PDF processing utilities
- **Leptonica**: Image processing library

## 📊 Project Pipeline Overview

### 1. Document Upload & Validation
- User uploads document through interactive widget
- File format validation and size checking
- Temporary file storage for processing

### 2. Text Extraction Phase
- **PDF Processing**: 
  - Primary: Direct text extraction using pdfminer
  - Fallback: OCR processing for image-based PDFs
- **DOCX Processing**: text extraction from Word documents
- **TXT Processing**: Direct text file reading with encoding handling

### 3. AI Analysis Pipeline
- **Keyword Extraction**: 
  - Uses KeyBERT with BERT embeddings
  - Identifies top 5 most relevant keywords
  - Removes common stop words,etc
- **Named Entity Recognition**:
  - Extracts authors, organizations, and dates
  - Uses spaCy's pre-trained English model
  - Handles multiple entity types
- **Text Summarization**:
  - Generates concise summaries using BART model
  - Optimized for document comprehension
  - Handles varying document lengths

### 4. Metadata Compilation
- **Document Statistics**: File size, word count, character count, line count, paragraph count
- **Content Analysis**: Keywords, summary, text preview
- **Entity Information**: Author, organization, publication date
- **Processing Metadata**: Timestamp, processing duration

### 5. Results Presentation
- **Interactive Display**: Formatted output with emojis and styling
- **JSON Export**: Structured data download
- **Text Preview**: Full document text display
- **Progress Tracking**: Real-time status updates

## 📖 Usage Guide

### Prerequisites
1. **Google Colab Account**: Free cloud-based Jupyter environment
2. **Internet Connection**: Required for model downloads and processing
3. **Document Files**: PDF, DOCX, or TXT files to analyze

### Setup Instructions
1. import jupyter notebook on google collab
2. 
3. **Install Dependencies**: Run the system and Python package installation cells, these are first 4 cells of the notebook, first time setup might take 3-4 minutes to download and install
4. run the final cell, upload doc when prompted

### Step-by-Step Usage
1. **Upload Document**: Click the upload button and select your file
2. **Monitor Progress**: Watch the real-time progress bar and status updates
3. **Review Results**: Examine the extracted metadata and analysis
4. **Download Results**: Click the download button to save JSON metadata
5. **run the last cell again and Repeat**

### Supported File Formats
- **PDF**: Text-based and image-based PDFs (with OCR capability)
- **DOCX**: Microsoft Word documents
- **TXT**: Plain text files with UTF-8 encoding

### Output Format
The tool generates a comprehensive JSON structure containing:
- Document information (title, size, statistics)
- Content analysis (keywords, summary)
- Entity extraction (author, organization, dates)
- Processing metadata (timestamp, duration)

## 🔧 Configuration Options

### Model Parameters
- **Keyword Count**: Adjustable number of keywords (default: 5)
- **Summary Length**: Configurable summary length (default: 130 words)
- **Entity Types**: Customizable entity recognition focus

### Processing Options
- **OCR Quality**: Adjustable OCR processing parameters
- **Text Truncation**: Configurable text length limits for processing
- **Error Handling**: Graceful fallback mechanisms

## 📈 Performance Considerations

### Processing Speed
- **Small Documents** (< 1MB): 10-30 seconds
- **Medium Documents** (1-5MB): 30-60 seconds
- **Large Documents** (> 5MB): 1-3 minutes

### Resource Requirements
- **Memory**: 2-4GB RAM recommended
- **Storage**: Temporary storage for uploaded files
- **Network**: Internet connection for model downloads

### Optimization Tips
- Use text-based PDFs when possible (faster processing)
- Limit document size for quicker analysis
- Process documents during off-peak hours for better performance

## 🚨 Limitations & Considerations

### Technical Limitations
- **File Size**: Maximum 100MB per file recommended
- **Language**: Currently optimized for English text
- **Format Support**: Limited to PDF, DOCX, and TXT formats
- **OCR Accuracy**: Image quality affects OCR results

### Model Limitations
- **Summary Quality**: Depends on document length and content
- **Entity Recognition**: May miss entities in complex documents
- **Keyword Relevance**: Context-dependent keyword extraction

### Privacy & Security
- **Data Processing**: Files are processed in Google Colab environment
- **Temporary Storage**: Files are temporarily stored during processing
- **No Data Retention**: Files are deleted after processing

