# OCR Text Detection Examples (OpenCV + Tesseract)

This project contains two Python examples for extracting text from images using **OpenCV** and **Tesseract OCR**.

## Files

- `TextSimple.py`: Minimal character detection example.
- `TextMoreExamples.py`: Extended examples (character boxes, word detection template, digits-only OCR template, webcam/screen-capture template).
- `1.png`: Sample input image used by both scripts.

## Requirements

- Python 3.9+
- Tesseract OCR installed on Windows
- Python packages:
  - `opencv-python`
  - `pytesseract`
  - `numpy`
  - `pillow`

## Install

1. Install Tesseract OCR:
   - https://tesseract-ocr.github.io/tessdoc/Home.html
   - [Tesseract User Manual](https://tesseract-ocr.github.io/tessdoc/Home.html)
   - Default path used in scripts:
     - `C:\Program Files\Tesseract-OCR\tesseract.exe`

2. Install Python dependencies:

```powershell
pip install opencv-python pytesseract numpy pillow
```

## Configure Tesseract Path

Both scripts currently set:

```python
pytesseract.pytesseract.tesseract_cmd = 'C:\\Program Files\\Tesseract-OCR\\tesseract.exe'
```

If your installation path is different, update this line in each script.

## Run

From the project folder:

```powershell
python TextSimple.py
```

or

```powershell
python TextMoreExamples.py
```

A window opens showing the image with detected character bounding boxes and labels.

## Notes

- `TextMoreExamples.py` includes additional OCR modes in commented blocks:
  - image-to-string
  - word-level detection (`image_to_data`)
  - digits-only OCR config (`--oem 3 --psm 6 outputbase digits`)
  - webcam / screen-capture OCR loop
- Uncomment the block you want to test.
- Press any key in the OpenCV window to close (`cv2.waitKey(0)`).

## References

The code in this project is based on the following tutorial:

- [OpenCV-Python-Tutorials-and-Projects/TextDetection](https://github.com/murtazahassan/OpenCV-Python-Tutorials-and-Projects/tree/master/Intermediate/TextDetection)

**NOTE:** This is for educational purposes. Please do not plagiarize.
