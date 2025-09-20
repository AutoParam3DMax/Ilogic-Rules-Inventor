# iLogic DXF Generator for Autodesk Inventor

This project contains an iLogic rule for Autodesk Inventor that automatically generates DXF files from sheet metal flats in assemblies. The script recursively goes through the entire assembly, ignores Content Center elements and suppressed components, and then exports the sheet metal flats to separate DXF files.

### Functionality

✅ Iterates through the entire assembly and subassemblies (recursively).
✅ Ignores suppressed components.
✅ Ignores parts from the Content Center.
✅ Handles sheet metal parts and generates their flats in DXF format.
✅ If a flat pattern is missing, it automatically attempts to create one.
✅ Saves DXFs in the source file folder.
🚧 Possibility of extension to generate STEP for standard parts.

### Requirements

* Autodesk Inventor (Created in Inventor 2024).
* .iam files (assemblies) containing .ipt sheet metal parts.

### Usage Instructions

1. Open the main assembly in Autodesk Inventor.
2. In the iLogic editor, create a new rule.
3. Copy the entire code from the `DXF_Generator.iLogic.vb` file.
4. Run the rule.
5. In the folder where the parts are saved, the generated `.dxf` files will appear.

### DXF File Structure

The DXF file name is created based on the part name (after the last `-`).

Example:
part `Project-123.ipt` → `123.dxf`.
part `Panel.ipt` → `Panel.dxf`.

### Further Development

Planned or possible functions to be added:
* STEP export for standard parts.
* PDF export of detail drawings.
* Customizable save options (paths, naming, layers).

### License

The project is available under the MIT license – you can use and modify it in your own projects.
👤 Author: Maks 📌 LinkedIn: www.linkedin.com/in/maks-dorchynets-80a909204
