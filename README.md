# 📦 Comprehensive Inventory Management System

A robust, full-stack, web-based software application engineered to optimize stock control, automate multi-channel supply logistics, track financial losses, and safely manage climate-controlled storage environments. Built primarily utilizing **PHP** for relational backend logic and a custom **SCSS/CSS** design system for an optimized user interface.

---

## 🏗️ Architecture & Data Flow

```
                 [ Supply Chain / Warehouse Input ]
                                │
                                ▼
                       [ Web Dashboard UI ]
                                │
                  (POST / GET Action Requests)
                                │
                                ▼
                       [ PHP Backend Engine ]
                                │
       ┌────────────────────────┼────────────────────────┐
       ▼                        ▼                        ▼
 [ Cold Storage ]       [ Loss Auditor ]       [ Product Seller ]
 (Climate Telemetry)   (Discrepancy Ledger)    (Sales Distribution)
       │                        │                        │
       └────────────────────────┼────────────────────────┘
                                │
                                ▼
                  [ Relational Database Layer ]
                    (MySQL)

```

---

## ⚡ Key Features

* **Cold Storage Management (`/coldstorage`)** — Designed specifically for inventory with strict environmental requirements. Logs real-time climate telemetry (temperature, humidity, zones) and handles capacity tracking alongside automated expiration safeguards.
* **Loss Auditing & Compliance (`/lossaduitor`)** — A secure auditing ledger dedicated to tracking stock shrinkage, damaged cargo, and inventory discrepancies. Features automated calculations that instantly cross-reference lost units against purchase costs for exact financial reconciliation.
* **Product Distribution Gateway (`/productseller`)** — Houses the outbound transactional marketplace layer. Programmed with transactional handlers that decrement shelf counts in real-time upon a successful sale to completely eliminate double-selling errors.
* **Vendor & Supply Chain Matrix (`/vendor`)** — A complete Supplier Relationship Management (SRM) directory managing supplier profiles, lead times, and fulfillment workflows while standardizing intake protocols for arriving shipments.
* **Modern SCSS Pipeline (`/scss`, `/css`)** — Powered by structured SCSS utilities (mixins, variables, nesting) to build a high-density dashboard UI. Maintained using a customized `.browserslistrc` layout rulebook to ensure browser consistency across modern mobile and older enterprise web environments.

---

## 📂 Repository Structure

```text
├── Database file/          # Schema blueprint and SQL configuration mappings
├── assets/                 # Images, icons, and static design resources
├── coldstorage/            # Environmental logging, zone metrics, and expiration tracking
├── css/                    # Compiled production stylesheets for UI rendering
├── lossaduitor/            # Auditing logs, discrepancy reports, and financial reconciliation
├── productseller/          # Transnational marketplace, order invoicing, and dispatch status
├── scss/                   # Raw preprocessor assets, color variables, and layout mixins
├── vendor/                 # SRM directory, procurement intake, and supplier profiles
├── .browserslistrc         # Target operational presets for backward CSS compatibility
└── README.md               # System overview documentation

```

---

## 🚀 Setup

### 1. Clone the repository

```bash
git clone https://github.com/jugumaya/inventory_management.git
cd inventory_management

```

### 2. Set Up Environment & Web Server

This package requires a local web server container running PHP 8.x along with a MySQL/MariaDB management instance (e.g., XAMPP, WampServer, or native Apache/Nginx).

**Using XAMPP/WampServer:**

1. Move or clone this repository folder directly into your server's public root directory (e.g., `C:/xampp/htdocs/` for XAMPP users).
2. Launch the **Apache** and **MySQL** modules from your environment control panel.

### 3. Database Initializing

1. Open your browser and navigate to your database control suite (typically `http://localhost/phpmyadmin`).
2. Create a fresh database instance named `inventory_management`.
3. Import the underlying schema script located inside the `/Database file` folder to set up relational foreign key mappings.

---

## ▶️ Running the System

1. Activate your local web server infrastructure.
2. Open your preferred web browser and direct your path to the system entry index:
```text
http://localhost/inventory_management/

```


3. Navigate between modules dynamically from the core sidebar to access cold chain metrics, file loss adjustments, or product order fullfilment suites.

---

## 📦 Technical Stack

* **Backend Engine:** Core PHP (Relational routing, ledger auditing calculation, telemetry logs)
* **Database Engine:** MySQL / MariaDB (Structured table indexing, integrity constraint mapping)
* **Frontend Design:** SCSS / CSS3 (Thematic styling, flexible dashboard layouts)
* **Client Logic:** HTML5 & Vanilla JavaScript (Asynchronous form handlers, live DOM mutations)

