# Matalan Price Calculator

A specialized web application designed for calculating carton prices, managing supplier specifications, and generating PDF quotes for Matalan's packaging operations in Bangladesh.

## 🚀 Key Features (v2.0)

*   **PDF Export Functionality**: Generate professional, branded A4 PDF quotes for suppliers (New in v2).
*   **Comprehensive Data Capture**:
    *   **Supplier Details**: Capture Origin, Supplier Name/Code, and Factory Name/Code.
    *   **Pack Configuration**: Select Pack Types (BS, B, BH UH) and Path Codes.
*   **Automated Pricing Engine**:
    *   Calculates unit costs, total area, and final pricing based on flute type (BC/C).
    *   **Dynamic Fees**: 4% PacD Fee for Standard Singles, 7.5% for others.
*   **Marking Rules**: Automatically applies low-quantity surcharges (< 100 units) for printing or labeling.
*   **Role-Based Views**: Configurable visibility for Admins, Garment Suppliers, and Packaging Suppliers.

## 📦 Version History

See [VERSION_HISTORY.md](./VERSION_HISTORY.md) for a detailed log.

- **v2.0**: Added PDF Export, Supplier/Factory inputs, Pack Type logic, and comprehensive UI redesign.
- **v1.0**: Initial calculator with basic logic and on-screen results only (No Export).

## 🛠️ Usage

1.  **Enter Supplier Info**: Select the Packaging Supplier and enter Factory details.
2.  **Configure Carton**: Choose Pack Type (BS/B/BH UH), Flute, and Carton Style.
3.  **Input Dimensions**: For custom cartons, enter L/W/H. For Standard, select the code (e.g., A1, B2).
4.  **Calculate**: View instant breakdown of Area, Unit Price, and Fees.
5.  **Export**: Click "Export PDF" to generate a printable quote.

---
*Developed for PacD / Matalan Bangladesh Operations*