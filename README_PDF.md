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
* ✅ Choice of export location:  
  * **Yes** → PDFs are saved in the same folder as the main assembly.  
  * **No** → A folder selection dialog opens, letting you choose a custom destination.

---

## How It Works

1. The script starts from the **active assembly document** (`.iam`).  
2. At launch, you are asked where to save PDFs:  
   * **Yes** → PDFs go to the main assembly folder.  
   * **No** → Choose a custom folder via a dialog.  
3. For each component, the script checks if there is an associated drawing file (`.idw`).  
4. If found:  
   * Opens the `.idw` file,  
   * Exports it to `.pdf`,  
   * Saves the PDF in the chosen export folder.  
5. After traversing the entire assembly tree, it displays a completion message.

---

## Requirements

* Autodesk Inventor (Created in Inventor 2024)   
* Correct associations between parts/assemblies and IDW drawings
* The code was created for the Polish Inventor interface.

---

## Code Structure

* **Main()** – starts the process, asks for export location, and triggers recursion.  
* **ProcessDocumentRecursive()** – main logic for traversing assemblies and subassemblies.  
* **ExportAllSheetsToPDF()** – exports all sheets from the `.idw` file to `.pdf`.

---

## Usage Instructions

1. Open the main assembly in Autodesk Inventor.  
2. In the iLogic editor, create a new rule.  
3. Copy the entire code from the file `PDF_Generator.iLogic.vb`.  
4. Run the rule.  
5. Choose where to save your PDFs (same folder as assembly or custom folder).  
6. **PDF files** corresponding to IDW drawings will appear in the selected folder.

---

## Notes

* The script does not generate PDFs for components without IDW drawings.  
* If an IDW file is missing links or is corrupted, it will be skipped.  

---

✍️ Author: Maks  
🔗 LinkedIn: (https://www.linkedin.com/in/maks-dorchynets-80a909204)
