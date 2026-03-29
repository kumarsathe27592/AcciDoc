# 🚨 iRAD Excel Generator

Convert iRAD (Integrated Road Accident Database) PDFs into structured **Excel reports** instantly — no AI, no API keys required.

---

## 📋 Features

- Upload any iRAD PDF and extract all accident fields automatically
- Generates a formatted Excel workbook with **2 sheets**:
  - **Accident Register** — summary table with key fields
  - **Full Details** — every parsed field organized by section
- Pure regex-based parsing (PyMuPDF) — works offline, no API needed
- Clean Streamlit UI with pipeline progress and live logs

---

## 🖥️ Screenshots

> Upload PDF → Parse fields → Download Excel in seconds

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/irad-excel-generator.git
cd irad-excel-generator
```

### 2. Create a virtual environment (recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the app

```bash
streamlit run app.py
```

The app will open at **http://localhost:8501**

---

## 📦 Dependencies

| Package | Purpose |
|---|---|
| `streamlit` | Web UI framework |
| `PyMuPDF` | PDF text extraction |
| `openpyxl` | Excel file generation |

---

## 📁 Project Structure

```
irad-excel-generator/
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── .gitignore           # Files to exclude from Git
└── README.md            # This file
```

---

## 📊 Excel Output Structure

### Sheet 1 — Accident Register
A formatted summary table with columns:
Sr. No. · FIR Number · Date · Time · Vehicle Involved · Lat/Lon · Severity · Deaths · Injured · Description

### Sheet 2 — Full Details
All extracted fields grouped into sections:
- Case Identifiers
- Accident Details
- Casualty Summary
- Vehicle Details
- Driver / Victim Details
- Legal Details

---

## ⚙️ How It Works

1. **Extract** — PyMuPDF reads all text from every page of the iRAD PDF
2. **Parse** — Regex patterns match field labels to their values (FIR number, date, GPS, casualties, vehicle info, driver info, etc.)
3. **Build** — openpyxl generates a formatted two-sheet Excel workbook
4. **Download** — One-click download of the `.xlsx` file

---

## 🔧 Troubleshooting

**PyMuPDF install error on Windows:**
```bash
pip install --upgrade pip
pip install PyMuPDF
```

**Port already in use:**
```bash
streamlit run app.py --server.port 8502
```

**Fields showing "—" (empty):**  
The PDF may have a non-standard layout. iRAD PDFs from different states may use slightly different label names — check the regex patterns in `app.py` and adjust if needed.

---

## 📄 License

MIT License — free to use, modify, and distribute.
