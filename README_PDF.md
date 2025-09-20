# iLogic – Automatic PDF Generation from IDW Files in an Assembly

This iLogic script is designed to automatically generate **PDF files** from IDW drawings linked to parts (`.ipt`) and assemblies (`.iam`) in Autodesk Inventor projects.  
It supports **recursive traversal of the entire assembly**, ensuring that all components with IDW drawings are exported to PDF.

---

## Features

* ✅ Recursively searches the entire assembly and subassemblies.  
* ✅ Supports both parts (`.ipt`) and assemblies (`.iam`).  
* ✅ Generates PDFs for all sheets in IDW files.  
* ✅ Automatically skips already processed files to avoid duplicates.  
* ✅ Error messages for skipped components.

---

## How It Works

1. The script starts from the **active assembly document** (`.iam`).  
2. It checks if a component has an associated drawing file (`.idw`).  
3. If found:  
   * Opens the `.idw` file,  
   * Exports it to `.pdf`,  
   * Saves the PDF in the same folder as the IDW file.  
4. After traversing the entire assembly tree, it displays a completion message.

---

## Requirements

* Autodesk Inventor (Created in Inventor 2024)   
* Correct associations between parts/assemblies and IDW drawings

---

## Code Structure

* **Main()** – starts the process, checks the document type, and triggers recursion.  
* **ProcessDocumentRecursive()** – main logic for traversing assemblies and subassemblies.  
* **ExportAllSheetsToPDF()** – exports all sheets from the `.idw` file to `.pdf`.

---

## Usage Instructions

1. Open the main assembly in Autodesk Inventor.  
2. In the iLogic editor, create a new rule.  
3. Copy the entire code from the file `PDF_Generator.iLogic.vb`.  
4. Run the rule.  
5. **PDF files** corresponding to IDW drawings will appear in the project folders.

---

## Notes

* The script does not generate PDFs for components without IDW drawings.  
* If an IDW file is missing links or is corrupted, it will be skipped.  
* You can extend the functionality, e.g., export to **DWG** or change the target folder.

---

✍️ Author: Maks  
🔗 LinkedIn: www.linkedin.com/in/maks-dorchynets-80a909204 


