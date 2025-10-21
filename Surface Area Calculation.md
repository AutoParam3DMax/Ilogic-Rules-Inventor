# iLogic – Surface Area Calculation for Selected Parts or Faces

This iLogic rule calculates the **total surface area** of selected parts, faces, or components in Autodesk Inventor.  
It is especially useful for estimating painting, coating, or surface treatment requirements.

---

## 🚀 Features

* ✅ Calculates area for selected **faces** and **components**  
* ✅ Supports both **parts (`.ipt`)** and **assemblies (`.iam`)**  
* ✅ Converts the total area to **square meters (m²)**  
* ✅ Saves the result in the **Inventor User Defined Properties** (`Painting area`)  
* ✅ Handles **FaceProxy** objects and multiple surface bodies  

---

## ⚙️ How It Works

1. Select the surfaces or components you want to measure in your Inventor document.  
2. Run the iLogic rule.  
3. The script evaluates the area of each selected face or all surface bodies of the selected components.  
4. The total area is displayed in a message box and saved to a **User Defined Property** named `Painting area`.  

---

## 🧩 Example Workflow

1. Open a **part** (`.ipt`) or **assembly** (`.iam`) in Autodesk Inventor.  
2. Select the faces, bodies, or components you want to calculate.  
3. Run the rule (`Calculate Surface Area`).  
4. A message box will show the total area in **m²**.  
5. Check the **Inventor User Defined Properties** to find the `Painting area` value saved automatically.

---

## 💡 Notes

* The rule **does not support nested component structures** beyond the first level in assemblies — only selected occurrences are considered.  
* If no usable surfaces are selected, the rule will display a warning.  
* The area calculation is based on **Inventor's internal surface evaluation**, and FaceProxy objects are included.  
* The total area is rounded to **4 decimal places** for display and **2 decimal places** in the property.  

---

## 🧰 Requirements

* Autodesk Inventor 2024 (Polish) or newer  
* iLogic enabled  
* Selected faces or components in the active document  

---

## 🧑‍💻 Author

Maks
🔗 [LinkedIn] www.linkedin.com/in/maks-dorchynets-80a909204
