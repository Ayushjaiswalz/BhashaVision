# BhashaVision
Multilingual OCR with Language Detectio# Multilingual OCR with Language Detection (Google Colab Compatible)

This project is an interactive **Gradio-based app** for extracting text from images in multiple **Indian languages** using **Tesseract OCR**, even from **blurry images**. It also **detects and labels** the language of each word using either `langdetect` or `langid`, and displays the results with bounding boxes on the image.

## 🧠 Features

- ✅ Multilingual OCR using Tesseract (`eng`, `hin`, `tam`, `ben`, etc.)
- ✅ Detects languages of individual words using `langdetect` or `langid`
- ✅ Works even on blurry images with auto-sharpening
- ✅ Annotated image preview with bounding boxes and language labels
- ✅ Choose between default and `tessdata_best` Tesseract models
- ✅ Easy-to-use Gradio interface

---

## 🚀 Getting Started (Google Colab)

Run this project directly from **Google Colab**:

1. Clone this repository or copy code to Colab.
2. Install required dependencies:

```python
!pip install gradio langdetect pytesseract langid opencv-python --quiet
!apt-get update --quiet
!apt-get install -y tesseract-ocr tesseract-ocr-eng tesseract-ocr-hin tesseract-ocr-ben \
  tesseract-ocr-tam tesseract-ocr-tel tesseract-ocr-guj tesseract-ocr-mar \
  tesseract-ocr-kan tesseract-ocr-mal tesseract-ocr-ori tesseract-ocr-asm \
  tesseract-ocr-pan tesseract-ocr-san tesseract-ocr-snd
!git clone https://github.com/tesseract-ocr/tessdata_best.git
!cp tessdata_best/*.traineddata /usr/share/tesseract-ocr/4.00/tessdata/
n using Tesseract &amp; Gradio
```
3. Run the Gradio app:
   iface.launch(pwa=True, debug=True)


🖼️ How It Works
1. Upload an Image: Any scanned document or photo with printed text.
2. Choose Language Detection Method:
    * langdetect: More accurate for longer words.
    * langid: Faster and lightweight.
3. Choose OCR Model:
    * default: Standard Tesseract data.
    * tessdata_best: More accurate but slower.
   
The app processes the image, extracts text, detects languages, and shows a preview image with labels and bounding boxes.

✨ Credits
  *  Tesseract OCR
  *  Gradio
  *  langdetect
  *  langid
  *  OpenCV

📜 License
  *  This project is open-source and free to use for educational and non-commercial purposes.
