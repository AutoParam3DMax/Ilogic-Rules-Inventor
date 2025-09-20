# iLogic DXF Generator dla Autodesk Inventor

Ten projekt zawiera regułę **iLogic** dla Autodesk Inventor, która automatycznie generuje pliki **DXF** z arkuszy blach w złożeniach.
Skrypt rekurencyjnie przechodzi przez całe złożenie, uwzględnia podzespoły, pomija elementy Content Center oraz wyłączone komponenty, a następnie eksportuje rozwinięcia blach do osobnych plików DXF.

## Funkcjonalności

* ✅ Przechodzi przez całe złożenie i podzłożenia (rekurencyjnie).
* ✅ Pomija wyłączone (Suppressed) komponenty.
* ✅ Pomija części z Content Center.
* ✅ Obsługuje części blaszane (Sheet Metal) i generuje ich rozwinięcia w formacie DXF.
* ✅ W razie braku rozwinięcia automatycznie próbuje je utworzyć.
* ✅ Zapisuje DXF-y w folderze źródłowych plików.
* 🚧 Możliwość rozbudowy o generowanie STEP dla części standardowych.

## Wymagania

* Autodesk Inventor (wersja z obsługą iLogic).
* Pliki **.iam** (złożenia) zawierające części blaszane **.ipt**.

## Instrukcja użycia

1. Otwórz główne złożenie w Autodesk Inventor.
2. W edytorze **iLogic** utwórz nową regułę.
3. Skopiuj cały kod z pliku `DXF_Generator.iLogic.vb`.
4. Uruchom regułę.
5. W folderze, gdzie zapisane są części, pojawią się wygenerowane pliki `.dxf`.

## Struktura plików DXF

* Nazwa pliku DXF jest tworzona na podstawie nazwy części (po ostatnim `-`).
* Przykład:

  * część `Project-123.ipt` → `123.dxf`.
  * część `Panel.ipt` → `Panel.dxf`.

## Dalszy rozwój

Planowane lub możliwe do dodania funkcje:

* Eksport **STEP** dla części standardowych.
* Eksport **PDF** rysunków detali.
* Konfigurowalne opcje zapisu (ścieżki, nazewnictwo, warstwy).

## Licencja

Projekt dostępny na licencji **MIT** – możesz używać i modyfikować w swoich projektach.

---

👤 Autor: Maks
📌 LinkedIn: www.linkedin.com/in/maks-dorchynets-80a909204
