# 🧾 Image & Document to PDF Converter (with HEIC and Auto-Naming Support)

A simple, cross-platform Python tool that converts **images** and **documents** into high-quality, automatically named PDF files.  
It supports both:
- 📸 Image formats (`.jpg`, `.png`, `.heic`, etc.)
- 📝 Document formats (`.docx`, `.txt`, `.md`, `.rtf`, `.odt`)

Each PDF is:
- Named with a **custom title** you choose  
- Automatically numbered (`[1]`, `[2]`, `[3]`, …)  
- Timestamped with the current date and time  
- Saved into the `PDF/` folder  
- Automatically opened after creation  

---

### 📦 Example Output
```
PDF/
├── holiday[1]_2025-10-16_14-35-21.pdf
├── holiday[2]_2025-10-16_14-40-07.pdf
├── report[3]_2025-10-16_14-45-12.pdf
├── meeting_notes[4]_2025-10-16_15-12-45.pdf
└── agenda[5]_2025-10-16_15-14-10.pdf
```

---

## ⚙️ 1. Install Python 3

### 🪟 **Windows**
1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. Download and run the **Windows installer**.
3. During installation, **check** “Add Python to PATH”.
4. Verify installation:
   ```bash
   python --version
   ```
   or
   ```bash
   py --version
   ```
   You should see something like `Python 3.12.x`.

---

### 🍎 **macOS**
1. Check if Python 3 is already installed:
   ```bash
   python3 --version
   ```
   If you see `Python 3.12.x`, you’re all set.

2. If not, install it using **Homebrew**:
   ```bash
   brew install python
   ```

---

### 🐧 **Linux (Ubuntu/Debian)**
Most Linux distributions include Python 3 by default:
```bash
python3 --version
```
If not installed:
```bash
sudo apt update
sudo apt install python3 python3-pip -y
```

---

## 🧰 2. Install Required Python Libraries

Once Python 3 is installed, install the required dependencies (same for all systems):

```bash
python3 -m pip install --upgrade pip
python3 -m pip install Pillow pillow-heif reportlab python-docx pypandoc
```

Then install **Pandoc** (used for `.md`, `.rtf`, and `.odt` document support):

- **macOS:**
  ```bash
  brew install pandoc
  ```
- **Linux:**
  ```bash
  sudo apt install pandoc -y
  ```
- **Windows:**  
  Download and install from [https://pandoc.org/installing.html](https://pandoc.org/installing.html)

---

## 📂 3. Folder Structure

Create your project folder like this:

```
image-to-pdf/
├── convert_to_pdf.py
├── img/
│   ├── photo1.jpg
│   ├── photo2.png
│   └── photo3.heic
├── DOC/
│   ├── report.docx
│   ├── notes.txt
│   ├── summary.md
│   └── agenda.rtf
└── PDF/
```

✅ **Usage**
- Place image files inside `img/`
- Place document files inside `DOC/`
- Generated PDFs appear automatically in `PDF/`
- The script auto-creates the `PDF/` folder if it doesn’t exist

---

## ▶️ 4. How to Use

1. Open your terminal or command prompt and navigate to your project folder:

   **Windows:**
   ```bash
   cd "C:\path\to\image-to-pdf"
   ```

   **macOS / Linux:**
   ```bash
   cd "/path/to/image-to-pdf"
   ```

2. Run the script:
   ```bash
   python3 convert_to_pdf.py
   ```

3. Choose a conversion type:
   ```
   1️⃣  Images to PDF
   2️⃣  Documents to PDF
   ```

4. When prompted, enter a **custom name** for your PDF (e.g. `report`, `vacation`, `notes`).  
   The script will automatically:
   - Detect existing PDFs in the `PDF/` folder  
   - Assign the next available `[number]`  
   - Add the current date and time  
   - Save your new PDF with a unique name  

   Example:
   ```
   PDF/
   ├── report[1]_2025-10-16_15-10-00.pdf
   ├── report[2]_2025-10-16_15-12-34.pdf
   └── report[3]_2025-10-16_15-14-55.pdf
   ```

5. The PDF will open automatically in your default viewer.

---

## 🖼️ 5. Supported File Types

|   Category 	 |					   Extensions 					 		              |                 Description              |
|---------------|------------------------------------------------------------|------------------------------------------|
| **Images** 	 | `.jpg`, `.jpeg`, `.png`, `.bmp`, `.tiff`, `.heic`, `.heif` | Combined into one multi-page PDF         |
| **Documents** | `.docx`, `.txt`, `.md`, `.rtf`, `.odt`                     | Each converted into its own formatted PDF|

---

## ⚡ 6. Output Examples

**Image PDF Example**
```
PDF/
└── vacation[1]_2025-10-16_14-42-33.pdf
```

**Document PDF Example**
```
PDF/
├── report[1]_2025-10-16_15-10-00.pdf
├── notes[2]_2025-10-16_15-11-42.pdf
└── summary[3]_2025-10-16_15-13-07.pdf
```

---

## 🧩 7. Troubleshooting

### ❌ `python` or `python3` not found
- Reinstall Python and check “Add to PATH” (Windows).
- On macOS/Linux, always use `python3`.

### ❌ `PIL not found`
```bash
python3 -m pip install Pillow
```

### ❌ `pillow_heif not found`
```bash
python3 -m pip install pillow-heif
```

### ❌ `pypandoc` or conversion errors
Make sure **Pandoc** is installed:
```bash
brew install pandoc        # macOS
sudo apt install pandoc -y # Linux
```

### ❌ Permission error on macOS
```bash
sudo python3 convert_to_pdf.py
```

---

## 🧠 8. Pro Tips

- Rename your PDF base name every time for better organization.  
- Both images and documents share the same numbering system.  
- PDFs include A4 margins, proper word wrapping, and auto-page breaks.  
- All output files are stored and timestamped for easy archiving.

---

## 🧑‍💻 Author

**Sorin Rotaru**  
Created for fast, simple, and cross-platform image & document PDF generation.  
Works seamlessly on **Windows**, **macOS**, and **Linux** 🖥️  

---

## 🪪 License

This project is open for **personal and educational use**.
# convert-to-PDF
