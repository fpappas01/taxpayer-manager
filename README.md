# Taxpayer Management System

This repository contains the full source code for a Java-based **Taxpayer Management System**, built to manage taxpayer records, parse data from files, and provide a graphical user interface (GUI) for user interaction and visualization.

---

## Project Structure

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

## Components

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
Implements the graphical interface using Java Swing:
- `GraphicalInterface`: main application window
- `ChartDisplay`: visual elements such as graphs or charts
- `TaxpayerData`: handles displaying data in the GUI

---

## Design Patterns Used

- **Factory Pattern**: Used in `TaxpayerFactory` and `FileReaderFactory`
- **Exception Handling**: Custom exceptions enhance error detection and reporting
- **Modular Design**: Separation of GUI, parsing logic, and data management
