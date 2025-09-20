# iLogic – BOM Export with Excel Post-Processing

This iLogic script is designed to **export a structured BOM** from sheet metal assemblies in Autodesk Inventor and automatically **correct the Excel file** after export.  
It collects all sheet metal parts recursively from the assembly and generates a clean, well-formatted Excel file for further use.  

> ⚠️ Note: The script was created using **my own custom assembly template**, and the Excel corrections are tailored to match **my personal BOM layout**. Users need to adjust the template path inside the code to use their own format.

---

## Features

* ✅ Recursively traverses the entire assembly and subassemblies to collect sheet metal parts.  
* ✅ Creates a temporary assembly containing only the collected sheet metal parts using a custom template.  
* ✅ Exports a BOM to Excel (`.xlsx`) from the structured "Parts Only" view.  
* ✅ Automatically fixes and formats the Excel file according to my BOM layout:  
  * Renames columns  
  * Extracts part numbers into a separate column  
  * Deletes unnecessary columns  
  * Auto-fits column widths  
  * Centers text horizontally and vertically  
  * Applies borders for better readability  
* ✅ Opens the final Excel file automatically after processing.  

---

## How It Works

1. The script starts from the **active assembly document** (`.iam`).  
2. It recursively searches for all sheet metal parts (`.ipt`) in the assembly and subassemblies.  
3. A new temporary assembly is created containing only the found sheet metal parts, based on a **custom template**.  
   > ⚠️ Users must edit the `"Own path\Template.iam"` function and set their own **template path**.  
4. The BOM is exported to Excel (`LaserParts.xlsx`) in the same folder as the source assembly.  
5. Excel corrections are applied automatically via the `FixExcel` function to match the custom BOM layout.  
6. The final Excel file is opened, and a message box confirms successful export.

---

## Requirements

* Autodesk Inventor (Created in Inventor2024)  
* Excel installed on the system for post-processing

---

## Code Structure

* **Main()** – orchestrates the process: creates the laser assembly, exports the BOM, and applies Excel fixes.  
* **FixExcel(filePath)** – modifies the exported Excel file according to my custom BOM layout: renames columns, extracts DXF names, removes unnecessary columns, formats, and applies borders.  
* **CreateLaserAsm(oDoc)** – generates a temporary assembly containing only sheet metal parts using the custom template.  
* **TraverseOccurrences(oOccs, smList)** – recursively collects all sheet metal components from an assembly and subassemblies.

---

## Usage Example

1. Open your main assembly (`.iam`) in Autodesk Inventor.  
2. Edit the `"Own path\Template.iam"` function in the code and set your own template path if needed.  
3. Run the iLogic rule.  
4. The script generates a **LaserParts.xlsx** file in the assembly folder with a clean, formatted BOM tailored to the custom template.

---

## Notes

* Only sheet metal parts (`.ipt`) are included in the BOM.  
* Columns L, N, and beyond are automatically removed during Excel post-processing.  
* The Excel corrections are designed specifically for my custom BOM layout.  
* Users must replace the template path inside the code to use their own assembly template.  
* Further customization is possible, e.g., exporting additional columns or changing formatting.

---

✍️ Author: Maks  
🔗 LinkedIn: www.linkedin.com/in/maks-dorchynets-80a909204
