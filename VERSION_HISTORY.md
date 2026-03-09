# Version History

## v2.3 - Role-Based Access Control & Repository Migration (Current)
**Release Date:** March 09, 2026

### 🚀 Logic & Security Updates
- **Role-Based Access Control (RBAC)**: Implemented new role-based views for the calculator:
  - `admin` / `sales_team`: Full visibility including factory dimensions, total price, rebates, PacD fees, and supplier net revenue.
  - `garment_supplier`: Restricted view showing only the Total Price (LC Price).
  - `packaging_supplier`: Restricted view showing only the Packaging Supplier Net Revenue.
- **Dynamic Subtitle**: Subtitle updates to "Only for Bangladesh" for non-admin roles to reflect regional limits.

### 🛠️ Maintenance
- **Repository Migration**: Migrated to a new GitHub remote (`PAC-D/matalanpricecalculator_sales_team.git`) and updated the primary branch to `main`.

---

## v2.2 - UI/UX Improvements & Business Logic Refinements

### 🚀 Logic & Feature Updates
- **Renamed Carton Type**: Changed "Ratio Carton" to **"Ratio Carton (Standard Footprint)"** for clarity.
- **Pack Path 3 & 4 Exclusion**: Pack & Path Codes 3 and 4 are now explicitly excluded from pricing calculations.
  - A warning message is displayed when these codes are selected.
  - Only area calculations (dimensions, SQM) are shown; price fields are hidden.
- **BS Pack Type Restriction**: When **BS (Box Single - Single)** is selected, the **Custom Carton** option is no longer available. Only standard/predefined cartons can be selected.
- **Sequential Configuration Input**: Improved input flow to ensure fields are enabled in proper sequence:
  - Pack Type → Pack & Path Code → Flute Type → Carton Type → Carton Selection → Dimensions.
  - Each field is only enabled after the previous one is selected.

### 🎨 UI Improvements
- Added a visible **warning banner** before the Calculate button for Pack Path 3 & 4 selections.
- Improved user guidance with clear messaging about pricing exclusions.

---

## v2.1 - Enhanced Specification Logic & Refinements
**Release Date:** February 07, 2026

### 🚀 Logic & Feature Updates
- **Renamed Condition**: Changed "BH UH" to **"BS UH"** (Box Single - Up & Hanging).
- **Expanded Pack & Path Codes**: All 4 codes (1, 2, 3, 4) are now available for both **BS** and **B** types.
- **Dynamic Flute Validation**: Implemented strict flute type availability based on Pack Type & Code:
  - **BS + Code 1/2** → Only **BC Flute** allowed.
  - **B + Code 1/2** → Only **C Flute** allowed.
- **Specification Details**: Updated "Flute Type" to show quality specs: **C-Flute (C40ECT)** and **BC-Flute (BC40ECT)**.

### 🛠️ UI & PDF Improvements
- **Simplified Input**: Removed unnecessary **Supplier Code** and **Factory Code** fields.
- **Mobile PDF Optimization**: Fixed PDF generation issues on mobile devices (viewport scaling & text size inflation).

---

## v2.0 - Professional Standard & Export Features
**Release Date:** February 06, 2026

### 🚀 Major New Features
- **PDF Export**: Added ability to generate and download professional A4 PDF quotes.
  - Includes *Clone Strategy* for clean layout regardless of screen size.
  - Branding header with PACD & Matalan logos.
- **Expanded Input Fields**:
  - Added **Supplier & Factory Information** section (Names, Codes, Packaging Supplier selection).
  - Added **Pack Type Configuration** (BS, B, BH UH) and "Pack & Path Code".
- **Logic Enhancements**:
  - **BH UH**: Added logic to calculate dimensions/area but exclude price.
  - **Fee Update**: Reduced "For PacD" fee to **4%** for Standard Carton Singles (BC-Flute).

### 🎨 UI & Design Overhaul
- **Modern "Pro" Theme**: Moved from a simple gradient background to a professional dashboard style (Navy/Red/Glassmorphism).
- **Navigation**: Replaced fixed bottom footer with a top **Navigation Bar**.
- **Logos**: Integrated `pacd.png` and `matalan.png` into the header with improved alignment.

---

## v1.0 - Initial Pricing Logic
**Release Date:** December 29, 2025

### Core Capabilities
- **Basic Pricing Engine**: Calculated costs based on Flute (BC/C) and Dimensions.
- **On-Screen Results**: displayed Unit Price, Total Area, and Fees directly on the UI.
- **Inputs**: Limited to Flute Type, Carton Style, and Dimensions/Quantity.
- **Simple UI**: Purple/Blue linear gradient styling with a fixed footer for logos.
- **No Export**: *This version did not support PDF generation or saving quotes.*
