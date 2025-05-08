# Taxpayer Management System

This repository contains the full source code for a Java-based **Taxpayer Management System**, built to manage taxpayer records, parse data from files, and provide a graphical user interface (GUI) for user interaction and visualization.

---

## 📁 Project Structure

```
source_code/
├── datamanagement/
│   ├── Address.java
│   ├── Company.java
│   ├── Date.java
│   ├── HeadOfHouseholdTaxpayer.java
│   ├── MarriedFilingJointlyTaxpayer.java
│   ├── MarriedFilingSeparatelyTaxpayer.java
│   ├── SingleTaxpayer.java
│   ├── Taxpayer.java
│   ├── TaxpayerFactory.java
│   ├── TaxpayerManager.java
│   ├── Receipt.java
│   ├── ReceiptAlreadyExistsException.java
│   ├── WrongFileEndingException.java
│   └── WrongTaxpayerStatusException.java
├── gui/
│   ├── ChartDisplay.java
│   ├── GraphicalInterface.java
│   └── TaxpayerData.java
├── parser/
│   ├── FileReader.java
│   ├── FileReaderFactory.java
│   └── TXTFileReader.java
```

---

## 📦 Components

### `datamanagement/`
This package is responsible for the core logic of the application:
- Defines taxpayer types and their associated attributes (e.g., marital status)
- Manages creation and tracking of receipts
- Factory pattern used for generating taxpayer instances
- Contains custom exceptions for error handling

### `parser/`
Provides utilities to read taxpayer data from text files:
- Abstract `FileReader` base class
- `TXTFileReader` implementation for `.txt` files
- Factory pattern (`FileReaderFactory`) enables extensibility for other formats

### `gui/`
Implements the graphical interface using Java Swing or JavaFX:
- `GraphicalInterface`: main application window
- `ChartDisplay`: visual elements such as graphs or charts
- `TaxpayerData`: handles displaying data in the GUI

---

## 🚀 Getting Started

### Prerequisites
- Java Development Kit (JDK) 8 or later
- Any IDE (e.g., IntelliJ IDEA, Eclipse) or command-line terminal

### Compilation Instructions

1. Open a terminal and navigate to the source directory:
   ```bash
   cd source_code
   ```

2. Compile all Java files:
   ```bash
   javac */*.java
   ```

3. Run the application (assuming `GraphicalInterface.java` contains the main method):
   ```bash
   java gui.GraphicalInterface
   ```

---

## 📄 Example Usage

1. The program starts with a graphical interface allowing you to load taxpayer files.
2. Once loaded, you can:
   - View taxpayer information
   - Add and remove receipts
   - Display summary charts

Files must follow a predefined format expected by the `TXTFileReader`.

---

## 🛠️ Design Patterns Used

- **Factory Pattern**: Used in `TaxpayerFactory` and `FileReaderFactory`
- **Exception Handling**: Custom exceptions enhance error detection and reporting
- **Modular Design**: Separation of GUI, parsing logic, and data management

---

## 📚 License

This project is provided **as-is** for educational purposes. No license is included. If you wish to use or redistribute this code, please add an appropriate license.

---

## 👨‍💻 Author

Developed as a sample academic project for managing tax-related records and learning core Java OOP concepts.

