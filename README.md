# Comprehensive Inventory Management System

A robust, full-stack, web-based software application engineered to optimize stock control, automate multi-channel supply logistics, track financial losses, and safely manage climate-controlled storage environments. Built primarily utilizing PHP for relational backend logic and a custom SCSS/CSS design system for an optimized user interface.

---

##  System Architecture & What I Built

I architected and developed this system into decoupled, domain-driven modules to ensure high scalability and easy maintenance. Below is the granular breakdown of every component I implemented:

### 1. Cold Storage Management (`/coldstorage`)
Designed specifically for inventory items with strict environmental and temperature requirements (e.g., perishables, pharmaceuticals, chemicals).
* **Environmental Logging:** Coded modules to track and log real-time telemetry metrics such as temperature thresholds, humidity levels, and zone assignments.
* **Expiration Safeguards:** Created automated aging tracking to trigger alerts when products approach critical dates within the cold chain.
* **Capacity Tracking:** Built logic to mathematically monitor space allocation within designated refrigeration/freezer units to prevent over-packing.

### 2. Loss Auditing & Compliance (`/lossaduitor`)
Developed a secure auditing ledger dedicated to tracking stock shrinking, damaged cargo, and inventory discrepancies.
* **Discrepancy Reporting:** Formulated submission protocols for field workers to log damaged, lost, or expired stock with cause classification codes.
* **Financial Reconciliation:** Created calculations that automatically cross-reference lost units against purchase costs, giving management an exact dollar figure of inventory write-offs.
* **System Log Integration:** Built structural database bridges ensuring every written-off item updates the active stock numbers instantly.

###  3. Product Seller & Distribution Gateway (`/productseller`)
Engineered the outbound transactional marketplace layer responsible for managing sales channels and standard product delivery.
* **Real-Time Stock Deductions:** Programmed transactional handlers that decrement shelf counts immediately upon a successful sale to eliminate double-selling errors.
* **Invoicing & Dispatch Status:** Built templates to generate digital manifests tracking order fulfillment from "Pending Packing" to "Dispatched".

###  4. Vendor & Supply Chain Matrix (`/vendor`)
Constructed a complete Supplier Relationship Management (SRM) directory.
* **Profiles & Tracking:** Created an organized index containing supplier profiles, lead times, contact data, and active fulfillment tracking.
* **Procurement Intake:** Standardized the intake workflow for handling arriving supplier shipments, matching physical manifests against database purchase records.

### 5. Relational Database Layer (`/Database file`)
* **Schema Blueprinting:** Designed the normalization layout for relational data (tables for Products, Logs, Warehouses, Users, and Line-Items).
* **Data Integrity:** Set up fundamental primary/foreign key mappings to prevent orphan records if a product or vendor profile is updated.

###  6. Modern SCSS/CSS Frontend Design (`/scss`, `/css`, `/.browserslistrc`)
* **Custom Styling Utilities:** Leveraged SCSS syntax (mixins, variables, nested nesting) to build an uniform, high-density dashboard UI.
* **Browser Consistency:** Maintained a legacy-safe styling pipeline utilizing a custom `.browserslistrc` configuration file to guarantee layout integrity across older enterprise and modern mobile browsers alike.

---

## 📊 Core Technical Stack

* **Backend Engine:** PHP (Core execution, structural routing, data processing)
* **Frontend Design:** SCSS / CSS (Custom responsive grid layout, thematic color variables)
* **Markup & Client Logic:** HTML5 & JavaScript (Form processing, active DOM manipulations)
* **Target Configurations:** `.browserslistrc` operational presets

---

## Step-by-Step Installation & Deployment

### Prerequisites
* A local web server environment container (e.g., **XAMPP**, **WampServer**, or native Apache/Nginx + PHP 8.x)
* **MySQL** / **MariaDB** database management instance

### Setup Blueprint

1. **Clone the Core Repository:**
   ```bash
   git clone [https://github.com/jugumaya/inventory_management.git](https://github.com/jugumaya/inventory_management.git)
