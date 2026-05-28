# Individual Assignment I: No-Code E-Commerce Application Design Project

## Student Information
* **Course:** E-Commerce and Web Application Course (EWA408510)
* **Academic Year:** 2025-2026 | Semester: II
* **Institution:** UNILAK — University of Lay Adventists of Kigali
* **Completion Date:** May 27, 2026

---

## Project Title
**IAM TECH — Premium Electronics No-Code E-Commerce Storefront**

---

## Platform Used
* **Platform:** Shopify 
* **Justification:** Chosen for its native inventory tracking, automated variant relationship rendering, rigorous SEO mapping controls, and structured CSV data import/export schemas.

---

## Features Implemented

### 1. Multi-Variant Product Catalog Architecture
* Integrated a 5-product matrix with embedded specifications, inventory tracking thresholds, custom weight metrics (in grams), cost-per-item profitability tracking, and global pricing tables.
* Structured complex variants (e.g., color and finish profiles) under synchronized product handles to mirror production-grade retail supply channels.

### 2. High-Performance Front-End Branding
* Engineered a custom rectangular e-commerce storefront banner ($1200 \times 400$ px aspect ratio).
* Implemented an intentional visual grid layout featuring a high-contrast call-to-action panel alongside premium visual asset anchors emphasizing **Smartphones, JBL Audio, and Sony Cameras**.

### 3. Comprehensive Page Routing & Copywriting
* **Homepage:** Clean hero module layout featuring the newly rebranded *IAM TECH* digital banner, a welcoming statement, and an immediate catalog funnel.
* **Product Catalog:** Automated multi-row rendering parsed from inventory manifests, detailing rich descriptions using clean HTML layout paradigms (`<p>`, `<ul>`, `<li>`).
* **About Page:** A professional brand identity description outlining the enterprise's curation process, customer-first fulfillment timelines, and strategic industry position.
* **Contact & Cart Interaction System:** Fully configured standard intake channel matched with functional add-to-cart workflows, simulated stock reservation logic (`shopify` tracking), and checkout routing rules.

---

## Product Data Reference Matrix
The following structured matrix outlines the specific e-commerce inventory layout systematically prepared for database injection:

| Handle | Title | Variant / Options | Price | Stock Qty | SKU | Barcode (GTIN) | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `lumoscharge-smart-desk-lamp` | LumosCharge Smart Desk Lamp with Wireless Charger | Color: Matte Black | $69.99 | 50 | `VE-LC-BLK` | `810012345678` | Active |
| `lumoscharge-smart-desk-lamp` | LumosCharge Smart Desk Lamp with Wireless Charger | Color: Sleek White | $69.99 | 45 | `VE-LC-WHT` | `810012345695` | Active |
| `aeropure-mini-hepa-air-purifier` | AeroPure Mini HEPA Air Purifier | Default Title | $49.99 | 120 | `AP-MINI-HEPA` | `810012345718` | Active |
| `hydropulse-sonic-electric-toothbrush` | HydroPulse Sonic Electric Toothbrush | Color: Charcoal Grey | $79.99 | 85 | `HP-ST-GRY` | `810012345749` | Active |
| `hydropulse-sonic-electric-toothbrush` | HydroPulse Sonic Electric Toothbrush | Color: Pearl Pink | $79.99 | 60 | `HP-ST-PNK` | `810012345756` | Active |
| `soundwave-pro-anc-wireless-earbuds` | SoundWave Pro ANC Wireless Earbuds | Default Title | $119.99 | 200 | `SW-ANC-PRO` | `810012345800` | Active |
| `nexacharge-20000-pd-power-bank` | NexaCharge 20000mAh PD Fast Charging Power Bank | Default Title | $39.99 | 150 | `NC-PB-20K` | `810012345886` | Active |

---

## Screenshots
*Note: Visual media assets are locally preserved inside the `/images` directory of this repository.*

#### 1. Homepage & Branding Banner
![Homepage Banner](images/homepage_banner.png)
*Figure 1: High-end hero element displaying the custom IAM TECH rectangular branding layout.*

#### 2. Dynamic Product Page
![Product Catalog Layout](images/product_page.png)
*Figure 2: Active inventory collection loop highlighting HTML bulleted descriptions and variant selectors.*

#### 3. Contact & Cart Interface
![Cart Page Interaction](images/cart_page.png)
*Figure 3: Interactive cart interface displaying itemized pricing totals and checkout gateways.*

---

## Challenges & Solutions

### Challenge 1: Column Schema and Relational Breaks During Multi-Variant Imports
* **Context:** When attempting to import items with distinct attributes (e.g., the *Matte Black* vs. *Sleek White* lamp setups) using standard spreadsheets, flat CSV structures frequently result in separate, duplicate product listings rather than nested variant selectors on a single page.
* **Solution:** Analyzed Shopify's core import schema to isolate the structural logic of the `Handle` key. Grouped rows sequentially under a single identical handle string while leaving the primary title and descriptions blank on trailing lines. This systematically instructed the database interpreter to group separate rows as a cohesive multi-variant matrix under one unique product listing.

### Challenge 2: Rich HTML Formatting Preservation within Text Fields
* **Context:** Plain text formatting inside long descriptions leads to flat, unappealing product pages that damage user engagement metrics and lower customer retention rates.
* **Solution:** Embedded clean, responsive inline markup directly into the `Body (HTML)` string payload within the import manifest. Wrapping elements carefully inside paragraph tags (`<p>`) and un-ordered listing fragments (`<ul><li>`) ensured that structural presentation layers were safely rendered upon database injection.

---

## Lessons Learned
1. **Database Schema Integrity:** Gained structural experience managing complex data formatting rules required for bulk inventory initialization. Realized how precision mapping directly affects live site performance, pricing accuracy, and tracking configurations.
2. **Visual Content Synergy:** Understood that professional e-commerce success is heavily dependent on cohesive graphic hierarchies. Designing standard-compliant banner assets ($1200 \times 400$ px) prevents unpredictable device scaling and enforces uniform consumer confidence.
3. **No-Code Architecture Potential:** Discovered that modern low-code frameworks like Shopify do not remove the technical layer; rather, they abstract it. Succeeding on these platforms requires an intentional understanding of content structures, data schemas, and clean information architectures.

---

## Live Website Link
[View Live Storefront Application](https://iamtech-electronics.myshopify.com)

---

## GitHub Repository Link
[Access Project Source Code Repository](https://github.com/username/iam-tech-ecommerce)
