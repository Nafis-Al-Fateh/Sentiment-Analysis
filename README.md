# 🌏 Belt and Road Initiative (Bangladesh Case): Online News Text Mining and Sentiment Analysis

## 🧠 Project Overview

This project performs large-scale **sentiment analysis** on online news articles related to the **Belt and Road Initiative (BRI)** in **Bangladesh**.

Using a dataset of English-language **PDF news articles (≈300 files)**, this pipeline extracts textual content — even from **scanned or image-based PDFs** — and analyzes their **sentiment polarity and subjectivity** over time.

The final goal is to visualize how **media sentiment** about the Belt and Road Initiative has evolved, offering valuable insights for **policy, economics, and international development research**.

---

## 🚀 Features

✅ **Supports both text-based and scanned PDFs** (via OCR)\
✅ **Batch processing of 300+ files** in Google Colab\
✅ **Automated sentiment scoring** using TextBlob\
✅ **Time-series visualization** of sentiment trends\
✅ **Bar plot of sentiment distribution**\
✅ **Exports results to CSV for further analysis**

---

## 🧩 Workflow Overview

1. **Upload Articles**
   - Upload `.pdf` files or a `.zip` archive of multiple news articles.

2. **Text Extraction**
   - Uses `PyPDF2` for digital PDFs.
   - Uses `pytesseract` OCR for scanned or image-based PDFs.

3. **Sentiment Analysis**
   - Computes **polarity** (–1 to +1) and **subjectivity** (0 to 1) with **TextBlob**.
   - Classifies each document as **Positive**, **Negative**, or **Neutral**.

4. **Visualization & Export**
   - Time-series line chart shows sentiment trend.
   - Bar chart shows sentiment distribution.
   - All results saved in `bri_pdf_sentiment_results_ocr.csv`.

---

## 🧠 Research Context

This project supports the study:  
> **“Online News Text Mining and Sentiment Analysis: The Belt and Road Initiative in Bangladesh.”**

It explores how **media narratives** around the Belt and Road Initiative (BRI) in Bangladesh have evolved, reflecting changing public discourse, policy perceptions, and geopolitical influence.

---

## ⚙️ Technologies Used

| Category | Tools/Libraries |
|-----------|----------------|
| **Language** | Python |
| **NLP** | TextBlob, NLTK |
| **OCR** | pytesseract, pdf2image |
| **PDF Processing** | PyPDF2, Poppler |
| **Visualization** | Matplotlib |
| **Data Handling** | Pandas |
| **Environment** | Google Colab |

---

## ⚔️ Challenges and Solutions

| Challenge | Description | Solution |
|------------|--------------|-----------|
| **1. Mixed PDF formats** | Some articles were scanned and unreadable as text. | Integrated **OCR (pytesseract)** for image-based PDFs. |
| **2. Missing timestamps** | Many files lacked clear publication dates. | Implemented **regex-based date extraction** from filenames. |
| **3. Uploading 300+ files** | Handling large uploads caused issues in Colab. | Added **ZIP upload support** and **TQDM progress tracking**. |
| **4. Neutral formal tone** | News articles often lacked clear emotion. | Applied **polarity thresholds** and subjectivity filters. |
| **5. OCR noise** | Extracted text from images was sometimes noisy. | Implemented **text cleaning** and manual review for low-confidence outputs. |

---

## 📊 Visual Outputs

### 📊 Sentiment Distribution
Shows the share of Positive, Negative, and Neutral news.

<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/3bf5f322-5802-4e8c-aa21-e89648305aec" />


---

## 📂 Output Example

**CSV Export:**
```csv
BRI 295.csv attached to this repository
