# ABCD ODDS Plugin (Document Delivery System)

A modular, database-driven **Document Delivery and Bibliographic Commutation** plugin for the ABCD library automation platform, fully engineered for PHP 8.1+ environments. It provides a streamlined, responsive web interface for patrons to request physical or digital document copies, such as journal articles, book chapters, and theses.

## Key Features

* **Dynamic Schema-Driven Forms:** Automatically renders contextual form fields depending on the selected bibliographic level (e.g., serial articles vs. monographs). It enforces database integrity by parsing field criteria directly from the database schema (`odds.fdt`) and structural configuration layouts (`odds_show_controls.tab`).
* **Core vs. Content Architecture:** Native compatibility with ABCD's cascading override structure. All local configurations, regional domain tables, customized message files, and help texts reside securely in the user-owned `content/` directory, remaining entirely untouched during core engine upgrades.
* **Automated Workflow & Notifications:** Equipped with an isolated mailing engine (`OddsMailer`) that triggers automatic email notifications using dynamic, customizable text/HTML templates. Supports automated alerts for request confirmations, fulfillment delivery, or library cancellations to both patrons and system administrators.
* **Flexible Access Control:** Features native toggles for granular security workflows, allowing either public/anonymous requests or strict authentication-only channels linked seamlessly to active OPAC user sessions.
* **Modern Validation Engine:** Leverages a lightweight, vanilla JavaScript and server-side validation matrix to sanitize data and guarantee strict compliance with data constraints before committing transactional flattens into the underlying ISIS database layers.

## Requirements

* **ABCD Platform:** Version 4.0+ (with `PluginBridge` and `LanguageManager` support).
* **PHP Version:** PHP 8.1 or higher.
* **Extensions:** `mbstring`, `curl`, and `zip`.
