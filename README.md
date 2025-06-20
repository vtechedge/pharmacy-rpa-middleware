# Pharmacy RPA Middleware

This project is a modular backend system that automates repetitive pharmacy tasks using OCR, bots, and structured data extraction. It is built using Python and designed to work with scanned prescription images.

---

## Project Folder Structure

```
pharmacy-rpa-middleware/
├── bot_engine/          # Bot automation logic (keyboard/mouse control)
├── data_extractor/      # OCR + field extraction
├── input_handler/       # File watcher to monitor scanned files
├── controller/          # (Future) API interface
├── config/              # Configuration & .env file
├── data/prescriptions/  # Output JSON data
├── input_docs/          # Raw scanned input files
├── logs/screenshots/    # Screenshots from bot runs
├── tests/               # Unit tests
├── scripts/             # CLI bot trigger scripts
├── README.md
├── requirements.txt
└── run.py

```
---

## How It Works (Backend Only)

1. Drop a prescription image into `input_docs/`
2. The watcher (`watcher.py`) detects it
3. OCR engine extracts text using Tesseract
4. Structured JSON is created in `data/prescriptions/`
5. (In next phase) The bot engine reads JSON and fills GUI

---

## How to Run

### 1. Clone the repo

git clone https://gitlab.com/your-org/pharmacy-rpa-middleware.git
cd pharmacy-rpa-middleware


### 2. Install dependencies

pip install -r requirements.txt


### 3. Make sure Tesseract OCR is installed

# Windows
Install from: https://github.com/tesseract-ocr/tesseract
# Mac
brew install tesseract


### 4. Start the watcher

python input_handler/watcher.py


### 5. Drop image file into `input_docs/`

---

## Tech Stack

- **Python 3.10+**
- **Tesseract OCR** (`pytesseract`)
- **Pillow** (image processing)
- **PyAutoGUI** (used in bot module)
- **Flask API** (future)

---

## License

This project is proprietary. For collaboration, please contact the owner.

---
