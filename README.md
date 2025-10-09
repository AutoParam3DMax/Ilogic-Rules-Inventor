# iLogic – Sheet Metal Size Control for Assemblies

This iLogic rule automatically checks whether **sheet metal parts** in an Autodesk Inventor assembly fit within a **specified sheet size**.  
It traverses the entire assembly structure recursively and highlights parts that exceed the defined dimensions.

---

## 🚀 Features

* ✅ Recursively checks all subassemblies and sheet metal components  
* ✅ Detects sheet metal parts exceeding the defined limits (length & width)  
* ✅ Highlights exceeding parts in **red** directly in the assembly  
* ✅ Optionally unfolds parts that don’t have a flat pattern yet  
* ✅ Generates a **TXT report** with all oversize parts and their dimensions  
* ✅ Handles suppressed components safely  

---

## ⚙️ How It Works

1. The user runs the rule from the main assembly (`.iam`) file.  
2. The script asks for **maximum allowed length and width** (in millimeters).  
3. It recursively goes through all components:
   * For every sheet metal part (`.ipt`), it unfolds the flat pattern (if needed),
   * Reads its flat pattern dimensions,
   * Compares them to the user-defined limits.  
4. If the dimensions exceed the allowed range:
   * The part is **highlighted in red**,
   * Its name and size are added to a summary list.  
5. When finished:
   * A dialog displays all oversized components,
   * A text report (`_Exceedances.txt`) is saved in the same folder as the assembly.  

---

## 🧩 Example Workflow

1. Open your top-level assembly in Autodesk Inventor.  
2. Run the rule (for example: `Check Dimensions`).  
3. Enter:
   * **Length** – e.g. `1000 mm`
   * **Width** – e.g. `2000 mm`  
4. After checking:
   * Oversized sheet metals will appear **red**,  
   * A message will list all components that exceed limits,  
   * The same list will be saved to a text file.

---

## 🧠 Code Structure

* **Main()** – handles user input and triggers recursive traversal  
* **SzukajPodzespol()** – searches through all subassemblies  
* **SprawdzWymiar()** – evaluates sheet size and sets appearance accordingly  

---

## 📄 Output Example

**TXT report format:**

---

## 💡 Notes

* If a part has no flat pattern, it will be automatically unfolded.  
* Suppressed or non-sheet-metal parts are ignored.  
* Highlighting colors can be adjusted (`RenderStyle` or `Color`).  
* Units are converted to **millimeters** by default.

---

## 🧰 Requirements

* Autodesk Inventor 2023 or newer  
* iLogic enabled  
* Sheet metal components with defined flat patterns  

---

## 🧑‍💻 Author

**Maks**  
🔗 [LinkedIn](https://www.linkedin.com/in/maks-dorchynets-80a909204)

