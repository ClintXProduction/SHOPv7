# CLTX4 SHOP — GitHub Pages Electronics Marketplace

A long-form, responsive electronics shop template for **CLTX4**.

## Included

- `index.html` — main storefront
- `style.css` — complete visual design
- `script.js` — product rendering, search, category filter, sorting, cart and language switch
- `data/products.json` — **EDIT THIS FILE TO ADD PRODUCTS, PRICES, STOCK AND IMAGES**
- `assets/images/products/` — put your product pictures here
- `python_tools/product_manager.py` — optional Python helper for editing the catalog
- `README.md` — setup guide

## GitHub Pages

This site is designed to run as a static GitHub Pages website.

1. Create a GitHub repository, for example `cltx4-shop`.
2. Upload all files while preserving the folder structure.
3. Make sure `index.html` is in the repository root.
4. Go to **Settings → Pages**.
5. Select **Deploy from a branch**.
6. Select your main branch and `/ (root)`.
7. Save and wait for GitHub Pages to publish the site.

### Important Python note

GitHub Pages serves static files. It does **not** execute a Python server/backend.

Python is included here as an optional local catalog-management tool. The actual public shop uses HTML + CSS + JavaScript + JSON, so it works on GitHub Pages.

## How to add a product

Open:

`data/products.json`

Copy an existing product object and change:

- `id` — unique ID
- `name` — English name
- `name_fil` — Filipino name
- `category` — category name
- `price` — Philippine peso price
- `stock` — quantity
- `badge` — optional label such as NEW / SALE / KIT
- `icon` — fallback emoji
- `image` — image path
- `description`
- `description_fil`

### Example with an image

```json
{
  "id": "my-product",
  "name": "My New Electronics Product",
  "name_fil": "Aking Bagong Electronics Product",
  "category": "Modules",
  "price": 150,
  "stock": 10,
  "badge": "NEW",
  "icon": "⚡",
  "image": "assets/images/products/my-product.jpg",
  "description": "English product description.",
  "description_fil": "Filipino product description."
}
```

Put `my-product.jpg` inside:

`assets/images/products/`

Then upload both the JSON change and image to GitHub.

## Image recommendations

Use JPG, PNG or WebP. Keep product images roughly square, such as 800×800 pixels.

Example:

`assets/images/products/esp32.jpg`

Then in JSON:

`"image": "assets/images/products/esp32.jpg"`

If `image` is empty, the website uses the product emoji instead.

## Changing shop contacts

Open `index.html` and edit the contact cards near the bottom.

Replace `#` with your real social links.

Replace:

`replace@example.com`

with your real shop email.

## Language system

The website currently has:

- English
- Filipino

Language selection is stored in the visitor's browser using localStorage.

To add another language, open `script.js` and add another translation object inside `translations`.

## Important security note

Do not put passwords, private API keys, payment secrets or administrator credentials inside HTML, CSS, JavaScript or JSON files published on GitHub Pages.

A real admin dashboard that securely changes products requires a backend/database or a service with authentication.

## CLTX4 customization ideas

You can later add:

- product detail pages
- checkout page
- order form
- WhatsApp/Messenger order button
- inventory status
- sale prices
- discount codes
- product reviews
- downloadable project files
- repair-service section
- custom PCB/service section
- admin dashboard with a real backend
- Firebase/Supabase database
- online payment integration
- QR payment section
- shipping calculator

## Suggested repository structure

CLTX4_SHOP/
├── index.html
├── style.css
├── script.js
├── README.md
├── data/
│   └── products.json
├── assets/
│   └── images/
│       └── products/
└── python_tools/
    └── product_manager.py

CLTX4 — BUILD • REPAIR • CREATE.
