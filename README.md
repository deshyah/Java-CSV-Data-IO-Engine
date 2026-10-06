# Java CSV Data I/O Engine

A modular Java application showcasing file input/output (I/O) operations, custom defensive input validation, CSV data persistence, and interactive Swing GUI file selection.

## 📌 Overview

This project implements a complete two-way file processing suite for managing structured domain records (`Person` and `Product` data). It addresses two core software engineering challenges:

1. **Defensive Data Entry:** Utilizing a customized `SafeInput` validation library to block invalid user entries and ensure well-formed data ingestion.
2. **Persistence & Presentation:** Writing structured object records to delimited CSV flat files and parsing them back into neatly formatted desktop UI views using `JFileChooser` and Java's `printf` formatting.

---

## ✨ Key Features

* **Bullet-Proof Input Harvesting (`SafeInput`):** Validates user terminal input in real-time, preventing runtime exceptions, type mismatches, or malformed data records.
* **CSV Data Serialization:** Dynamically builds and persists delimited records (`.txt` / `.csv`) for Person and Product domain models.
* **Interactive Desktop GUI File Selection:** Integrates Java Swing's `JFileChooser` to allow users to visually browse, select, and open dataset files natively within their operating system.
* **Formatted Columnar Data Rendering:** Utilizes `String.format` and `printf` specifiers to render raw CSV strings into clean, human-readable tabular terminal reports.

---

## 🛠️ Tech Stack & Architecture

* **Language:** Java 17+
* **GUI Framework:** Java Swing (`JFileChooser`)
* **I/O Classes:** `BufferedReader`, `BufferedWriter`, `FileReader`, `FileWriter`, `Scanner`
* **Data Structures:** `ArrayList` for dynamic record collection prior to disk writes
* **IDE:** JetBrains IntelliJ IDEA

---

## 📁 Repository Structure

```text
├── PersonGenerator.java    # CLI program to collect and serialize Person records
├── PersonReader.java       # Swing GUI app to select and display formatted Person data
├── ProductWriter.java      # CLI program to collect and serialize Product records
├── ProductReader.java      # Swing GUI app to select and display formatted Product data
├── SafeInput.java          # Reusable defensive user input validation library
├── PersonTestData.txt      # Sample generated Person CSV dataset
└── ProductTestData.txt     # Sample generated Product CSV dataset
```
---

## 🚀 How to Run

### Prerequisites
* Java Development Kit (JDK 17 or higher installed)
* An IDE such as IntelliJ IDEA or VS Code

### Executing the Generators (Writing Data)
1. Run `PersonGenerator.java` or `ProductWriter.java`.
2. Follow the terminal prompts to enter record details.
3. Enter the desired output file name (e.g., `PersonTestData.txt`) when prompted.

### Executing the Readers (Parsing & Displaying Data)
1. Run `PersonReader.java` or `ProductReader.java`.
2. A native `JFileChooser` window will pop up.
3. Select any generated CSV text file to view the aligned tabular output in the console.

---

## 💡 Key Engineering Takeaways

* **Separation of Concerns:** Splitting read and write responsibilities into dedicated classes keeps data access patterns modular and scalable.
* **Defensive Programming:** Handling user input errors at the edge prevents downstream file corruption and application crashes.
* **Cross-Platform GUI Integration:** Leveraging Java Swing components bridges terminal-based business logic with native desktop user interactions.
