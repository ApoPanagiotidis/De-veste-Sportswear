# De Veste Sportswear

A school project: a complete WooCommerce webshop for a fictional sportswear
brand based in Leiden. Built with a custom homepage, category carousels,
legal pages, and GDPR/cookie consent — all in Dutch.

## Stack
- WordPress + WooCommerce
- Astra theme with custom CSS
- Docker (docker-compose)
- Complianz for GDPR/cookie consent

## Features
- Custom homepage modeled on a real sportswear retailer, with hero banner,
  category carousels, sport grids, brand banners, and product shortcodes
- WooCommerce product and category pages across six brands
- Clickable brand banners
- Legal pages (terms, cookie policy, privacy policy, returns, vacancies)
  built as styled custom HTML blocks
- GDPR/cookie consent via Complianz

## Run locally
1. Clone the repo
2. Copy `.env.example` to `.env` and fill in your own values
3. `docker-compose up -d`
4. Visit `localhost:8090`
5. Install WordPress + WooCommerce + the Astra theme, then re-apply the
   custom CSS from `Appearance → Customize → Additional CSS`

## Screenshots

### Homepage
![Header and hero banner](Screenshot_1.png)

![Weekend deals and product grid](Screenshot_3.png)

![Popular categories and sports](Screenshot_2.png)

![Shop by brand banners](Screenshot_5.png)

![Collection banners](Screenshot_6.png)

![Collection banners continued](Screenshot_7.png)

![Popular brands](Screenshot_4.png)

![Footer](Screenshot_8.png)

### Product page
![Product page](Screenshot_9.png)

### Cart
![Cart](Screenshot_10.png)
