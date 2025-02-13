# 📂 Repository Overview

This repository manages PDF data and related CSV files used in the **Prevention DX** project.  
The files contain information on OCR status, extracted text, embedding vectors, and more.

## 📁 Included Files

### 📄 `03_テストデータ.csv`
**Description:** PDF data information  
**Column Details:**
- **file_name**: Name of the file  
- **folder_path**: Folder path where the file is located  
- **text_extracted**: Whether text extraction was successful (True/False)  
- **ocr_required**: Whether OCR is required (True/False)  
- **text**: Extracted text data  
- **screenshot_path**: Path to the screenshot of the PDF (if available)  

---

### 📄 `legal_documents.csv`
**Description:** Legal document data including embedding vectors  
**Column Details:**
- **id**: Document ID  
- **file_name**: Name of the file  
- **folder_path**: Folder path where the file is located  
- **text_extracted**: Whether text extraction was successful (True/False)  
- **ocr_required**: Whether OCR is required (True/False)  
- **text**: Extracted text data  
- **screenshot_path**: Path to the screenshot of the PDF (if available)  
- **embedding**: Vector embedding (Mcl-tohoku/bert-large-japanese)  
- **embedding_v2**: Vector embedding (nlp-waseda/roberta-base-japanese)  
- **embedding_v3**: Vector embedding (jinaai/jina-embeddings-v3)  
- **embedding_v4**: Vector embedding ( sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)  
