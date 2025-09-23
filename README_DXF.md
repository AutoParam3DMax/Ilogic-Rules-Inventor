# iLogic DXF Generator for Autodesk Inventor

This project contains an **iLogic rule** for Autodesk Inventor that automatically generates **DXF files** from sheet metal parts in assemblies. The script recursively traverses the entire assembly, including subassemblies, skips **Content Center** parts and suppressed components, and then exports the sheet metal flat patterns into separate DXF files.

---

## Features

✅ Recursively traverses the entire assembly and subassemblies.  
✅ Skips suppressed components.  
✅ Skips Content Center parts.  
✅ Supports sheet metal parts and generates their flat patterns in DXF format.  
✅ Automatically creates a flat pattern if one does not exist.  
✅ Saves DXF files either:
   - in the same folder as the **main assembly**, or  
   - in a folder **manually selected** via Windows folder browser.  

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
5. At runtime, choose how you want to export DXFs:
   - **YES** → save DXFs in the main assembly’s folder.  
   - **NO** → select a folder in Windows.  
6. The generated `.dxf` files will appear in the chosen folder.  

---

## DXF File Naming

The DXF file name is generated based on the part name (after the last `-`).  
This behavior reflects the **author’s personal preference** that part names should include a `-` to separate project/part information.  

- If the name contains `-`, only the portion after the last `-` is used.  
- If the name does **not** contain `-`, the **entire name** is used.  

**Examples:**  
- Part `Project-123.ipt` → `123.dxf`  
- Part `Panel.ipt` → `Panel.dxf`  

---

## DXF Export Options

The DXF export string used is:  "FLAT PATTERN DXF?AcadVersion=2000&InvisibleLayers=IV_Tangent;IV_ARC_CENTERS;IV_FEATURE_PROFILES;IV_FEATURE_PROFILES_DOWN;IV_BEND_DOWN;IV_BEND"


If you want to customize these options (e.g., layer names), you can verify and adjust them in Inventor:

1. Open a sheet metal part.  
2. Generate its flat pattern.  
3. Go to **Save Copy As → DXF**.  
4. In the configuration window, open the **Layers** tab.  
5. Review the available layer names and adjust the iLogic rule accordingly.  

---

## Troubleshooting

⚠️ This rule was originally written for the **Polish Inventor interface**.  
If you encounter issues, you may need to adjust some command names or layer names to match your language version of Inventor.  

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
📌 **LinkedIn:** https://www.linkedin.com/in/maks-dorchynets-80a909204



