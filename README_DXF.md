# iLogic DXF Generator for Autodesk Inventor

This project contains an **iLogic rule** for Autodesk Inventor that automatically generates **DXF files** from sheet metal parts in assemblies. The script recursively traverses the entire assembly, including subassemblies, skips **Content Center** parts and suppressed components, and then exports the sheet metal flat patterns into separate DXF files.

---

## Features

✅ Recursively traverses the entire assembly and subassemblies.  
✅ Skips suppressed components.  
✅ Skips Content Center parts.  
✅ Supports sheet metal parts and generates their flat patterns in DXF format.  
✅ Automatically creates a flat pattern if one does not exist.  
✅ Saves DXF files in the same folder as the source parts.  

🚧 Future expansion: possibility to generate **STEP files** for standard parts.

---

## Requirements

- Autodesk Inventor (version with iLogic support)  
- `.iam` assembly files containing sheet metal `.ipt` parts  

---

## Usage Instructions

1. Open the main assembly in Autodesk Inventor.  
2. In the iLogic editor, create a new rule.  
3. Copy the entire code from the file `DXF_Generator.iLogic.vb`.  
4. Run the rule.  
5. The generated `.dxf` files will appear in the folders where the parts are saved.  

---

## DXF File Naming

The DXF file name is generated based on the part name (after the last `-`).

**Example:**  
- Part `Project-123.ipt` → `123.dxf`  
- Part `Panel.ipt` → `Panel.dxf`  

---

## Future Development

Planned or possible features to add:  
- Export **STEP** for standard parts  
- Export **PDF** drawings of parts  
- Configurable save options (paths, naming conventions, layers)  

---

## License

This project is available under the **MIT License** – you can use and modify it in your projects.  

👤 **Author:** Maks  
📌 **LinkedIn:** [www.linkedin.com/in/maks-dorchynets-80a909204](https://www.linkedin.com/in/maks-dorchynets-80a909204)
