# GTM Web Container Export for Addingwell Shopify Integration

This repository contains a **Google Tag Manager (GTM) Web Container export** (`template.json`) to streamline the integration of GTM and GA4 for Shopify stores using the **Addingwell Shopify Application**. It is pre-configured to manage key e-commerce tracking events and supports server-side tracking with a `server_container_url`.

---

## Features

- **Pre-configured GA4 Tags and Triggers**  
  Includes multiple GA4 tags such as:
  - Page View
  - View Item
  - Add to Cart
  - Remove from Cart
  - Begin Checkout
  - Add Payment Info
  - Purchase
  - Add Address Info
  - Add Shipping Info

- **DataLayer Variables for Shopify**  
  Captures essential e-commerce data from Shopify's dataLayer, such as:
  - Transaction ID
  - Items
  - Tax
  - Value
  - Currency
  - User-specific details (email, phone, address components)

- **Server-Side Tracking Integration**  
  Allows seamless server-side tracking through a configurable `server_container_url`.

- **Built-in Debugging and Customization**  
  Includes built-in variables like `Page URL`, `Referrer`, and `Event` for flexible debugging and monitoring.

---

## Prerequisites

Before using this container, ensure you have:  

1. **Addingwell Shopify Application** installed and configured on your store.  
2. Access to a GTM account and a **server-side GTM container** URL.  
3. Basic familiarity with GTM and Shopify dataLayer.

---

## Installation Instructions

### Step 1: Import the Container
1. Clone or download the repository and locate `template.json`.
2. Log in to your Google Tag Manager account.
3. Navigate to **Admin > Import Container** in your web container.
4. Upload `template.json`.
5. Choose either **Merge** or **Overwrite**, depending on your setup.
6. Confirm the import.

### Step 2: Configure GA4 Measurement ID and Server URL
1. Edit the **GA4 - Measurement ID** variable in GTM to include your GA4 measurement ID (e.g., `G-XXXXXXXX`).
2. Update the **GA4 - Server Container URL** variable to your server container URL.

### Step 4: Configure the Addingwell Shopify Application
1. Ensure that the Addingwell Shopify Application is properly configured with the required settings.  
2. Verify that the application is enabled in your Shopify theme and that the "Customer Event" (pixel) code has been correctly added.

### Step 4: Test Configuration
1. Enable GTM Preview mode to validate tag firing.
2. Verify events are tracked correctly in GA4.
3. Use the GTM server-side debugger for further validation.

---

## Structure Overview

### Tags
- **GA4 Configuration Tag**  
  Base configuration for GA4, includes `server_container_url`.

- **GA4 Event Tags**  
  Handles key Shopify interactions:
  - `view_item`
  - `add_to_cart`
  - `begin_checkout`
  - And more...

### Triggers
- Pre-configured to fire on custom Shopify events, such as:
  - `add_to_cart`
  - `begin_checkout`

### Variables
- **Custom Variables** for GA4:
  - `GA4 - Measurement ID`
  - `GA4 - Server Container URL`

- **DataLayer Variables** for e-commerce:
  - Transaction ID
  - Items
  - Currency
  - User details (email, phone, address components)

### Built-in Variables
- `Page URL`, `Referrer`, `Event`, and others for debugging.

---

## Troubleshooting

- Ensure `server_container_url` is correctly set in the Addingwell app.
- Test dataLayer variables and triggers using GTM’s debugging tools.
- Verify GA4 settings (Measurement ID, data streams, etc.).

---

## Contributing

Contributions to improve or extend this template are welcome. Submit a pull request or open an issue for discussion.
