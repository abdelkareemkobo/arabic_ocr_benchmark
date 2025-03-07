# Arabic Text Benchmarking

This project contains three Jupyter Notebook scripts to test and compare models for Arabic text processing and OCR (text extraction from images).

## Datasets 


The test data comes from Hugging Face and includes PDF scans (no Arabic-KHATT dataset):

- ahmedheakl/arocrbench_synthesizear: Synthetic Arabic text scans.
- ahmedheakl/arocrbench_patsocr: Scanned Arabic documents (PATS collection).
- ahmedheakl/arocrbench_arabicocr: General Arabic OCR scans.
- ahmedheakl/arocrbench_hindawi: Scans from Hindawi books or art

These datasets are filtered from [Kitab-bench](https://huggingface.co/collections/ahmedheakl/kitab-bench-677dd5d88d5db344d5595b78)

## What’s Inside
- **`ain_benchmark.ipynb`**: Tests the **AIN model** 
- **`qari_benchmark.ipynb`**: Tests the **Qari model** 
- **`non_llm_ocr_benchmark.ipynb`**: Compares **EasyOCR** and **Tesseract OCR** for reading Arabic text from images (e.g., books or notes).

## Why Use This?
- Check how well these models work with Arabic.
- See their speed and accuracy on real examples.

## Files
```
├── ain_benchmark.ipynb         # AIN model tests
├── qari_benchmark.ipynb        # Qari model tests
├── non_llm_ocr_benchmark.ipynb # EasyOCR & Tesseract tests
├── README.md                   # This file
```

## What You Need
- **Python 3.8+**: To run the code.
- **Jupyter Notebook**: To open and edit the scripts.
- **Libraries**: Like `pandas`, `torch`, `easyocr`, and `pytesseract` (install them later).
- **Tesseract OCR**: For the OCR script (install separately).

## How to Set Up
1. Download this folder:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Install Python stuff:
   ```bash
   pip install pandas numpy jupyter torch easyocr pytesseract
   ```
   Add more if your models need them (e.g., `transformers`).
3. Install Tesseract OCR:
   - Ubuntu: `sudo apt install tesseract-ocr tesseract-ocr-ara`
   - Windows/Mac: Check [Tesseract’s guide](https://github.com/tesseract-ocr/tesseract).
4. Start Jupyter:
   ```bash
   jupyter notebook
   ```

## How to Use
1. Open a script in Jupyter (e.g., `ain_benchmark.ipynb`).
2. Run the cells to see results.
3. Add your own Arabic text or images to test.

## What Each Script Does
1. **`ain_benchmark.ipynb`**  
   - Tests an AIN model on Arabic text.  
   - Example: Finds "محمد" as a `Person`.  
   - Shows accuracy and speed.

2. **`qari_benchmark.ipynb`**  
   - Works with Quranic data (e.g., reciters like "Yasser Al-Dosari").  
   - Turns data into text and finds things like names or verses.  
   - Shows results like `Person` or `Text`.

3. **`non_llm_ocr_benchmark.ipynb`**  
   - Reads Arabic from images using EasyOCR and Tesseract.  
   - Example: Extracts text from a photo of a page.  
   - Compares which one is better.

