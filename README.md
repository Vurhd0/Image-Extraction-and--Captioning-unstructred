# Image-Extraction-and--Captioning-unstructred

This project provides a streamlined pipeline to **automatically extract images** and **generate descriptive captions/tags** from NCERT textbook PDFs using a single Jupyter Notebook
---

## What Has Changed?

- **Everything is done in ONE `.ipynb` file**
- **Image extraction** is handled using the `unstructured` library
- **Image captioning** is performed using either:
  - Google Gemini API (when available)
- Designed to **run entirely on Google Colab**
- Output files (`images/`, `captions.csv`) are auto-generated and downloadable

---

## Workflow Overview

1. **Image Extraction**:  
   Extract images from PDF pages using the `unstructured` library.

2. **Image Tagging**:  
   Generate descriptive captions for each extracted image using:
   - `google-generativeai` (Gemini API)
   - Fallback: HuggingFace’s Microsoft GIT captioning model

3. **Output Generation**:  
   - All images are stored in an `images/` folder
   - Captions are saved in `captions.csv`
   - Download buttons included for convenience

---

## Requirements

- Python 3.x (Handled automatically on Google Colab)
- Required Libraries:
  - `unstructured`
  - `Pillow`
  - `transformers`
  - `torch`
  - `google-generativeai`
  - `pandas`
  - `matplotlib`

All dependencies are installed automatically within the notebook.

---

## How to Use (On Google Colab)

1. **Download the `.ipynb` file from this repo**
2. Open **[Google Colab](https://colab.research.google.com/)**
3. **Upload the notebook**
4. **Mount Google Drive** if you're using PDFs stored in your drive
5. **Upload your input PDF**
6. **Change the PDF path in the cell** that specifies the file location
    ![image](https://github.com/user-attachments/assets/140cf881-7b88-49b4-878f-85e6e065b018)

8. **Run all cells**

---

## Output

- All extracted images will be saved in:
