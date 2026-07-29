# De Veste Sportswear 🏃‍♂️👟

A Dutch-language sportswear webshop built with **WordPress and WooCommerce** for a fictional sports retailer called **De Veste Sportswear**.

The website includes a custom storefront, product and category pages, promotional sections, brand collections, a shopping cart, legal pages, and GDPR cookie consent.

This project was created as a **school learning project** by **Apo Panagiotidis**.

## What the website does

* **Custom homepage** — presents featured products, promotional campaigns, sports categories, collections, and popular brands.
* **Product catalogue** — allows visitors to browse sportswear, footwear, and accessories.
* **Product pages** — display product images, descriptions, prices, sizes, stock information, and purchase options.
* **Shopping cart** — allows customers to add products, change quantities, remove items, and view the order total.
* **Product search** — includes a search bar for finding products and brands.
* **Category navigation** — visitors can browse products by clothing type, sport, or brand.
* **Brand pages** — contains products and promotional sections for several well-known sportswear brands.
* **Sale section** — highlights discounted products and temporary promotions.
* **Responsive layout** — adapts the storefront to different screen sizes.
* **Customer account area** — WooCommerce account functionality for orders and account information.
* **Legal pages** — includes terms and conditions, privacy information, returns, cookie policy, and other customer-service pages.
* **Cookie consent** — uses Complianz for GDPR and cookie-consent management.

## Homepage sections

The custom homepage includes:

* Store benefits and service highlights
* Header with logo, product search, account, and shopping cart
* Main navigation menu
* World Cup 2026 hero banner
* Weekend-deal promotion
* Featured product grid
* Popular product categories
* Sport-based shopping sections
* Brand-focused image banners
* Footwear promotion
* Clothing collection banners
* Popular brand logos
* Customer-service footer
* Payment-method icons

## Product categories

The website contains categories such as:

* Sneakers
* Running shoes
* T-shirts
* Shorts
* Hoodies
* Tracksuits
* Sports footwear
* Sports clothing

Visitors can also browse products based on sports such as:

* Football
* Running
* Tennis
* Athletics

## Brands

The storefront includes products or promotional sections for brands such as:

* Nike
* Adidas
* Puma
* Lacoste
* Banlieue
* ASICS
* New Balance

## Tech stack

* **Content management system:** WordPress
* **E-commerce:** WooCommerce
* **Theme:** Astra
* **Page customization:** WordPress editor and custom HTML blocks
* **Styling:** Custom CSS
* **Cookie consent:** Complianz
* **Database:** MySQL 8.0
* **Containerization:** Docker and Docker Compose
* **Web server:** Apache through the official WordPress image

## Project structure

```text
├── README.md                  # Project documentation
├── docker-compose.yml         # WordPress and MySQL development environment
├── Screenshot_1.png           # Header and homepage hero banner
├── Screenshot_2.png           # Product categories and sports sections
├── Screenshot_3.png           # Weekend deals and featured products
├── Screenshot_4.png           # Popular brands and footer
├── Screenshot_5.png           # Brand banners and footwear promotion
├── Screenshot_6.png           # Clothing collection banners
├── Screenshot_7.png           # Popular brands section
├── Screenshot_8.png           # Complete website footer
├── Screenshot_9.png           # WooCommerce product page
└── Screenshot_10.png          # WooCommerce shopping cart
```

## Docker environment

The included `docker-compose.yml` starts two containers:

### WordPress

* Uses the latest official WordPress image
* Runs through Apache
* Connects to the MySQL container
* Is available on port `8090`
* Stores WordPress files in a persistent Docker volume

### MySQL

* Uses MySQL 8.0
* Creates a database named `wordpress`
* Stores database data in a persistent Docker volume

The Docker services are configured as follows:

```yaml
services:
  db:
    image: mysql:8.0
    container_name: wordpress-mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wpuser
      MYSQL_PASSWORD: wppassword
    volumes:
      - db_data:/var/lib/mysql

  wordpress:
    image: wordpress:latest
    container_name: wordpress-site
    restart: always
    ports:
      - "8090:80"
    environment:
      WORDPRESS_DB_HOST: db
      WORDPRESS_DB_USER: wpuser
      WORDPRESS_DB_PASSWORD: wppassword
      WORDPRESS_DB_NAME: wordpress
    volumes:
      - wp_data:/var/www/html
    depends_on:
      - db
```

## Running the project locally

### Requirements

Install the following software before starting:

* Docker
* Docker Compose

### Setup

1. Clone or download the repository.
2. Open a terminal in the project directory.
3. Start the containers:

```bash
docker-compose up -d
```

4. Open the website in a browser:

```text
http://localhost:8090
```

5. Complete the WordPress installation.
6. Install and activate the required theme and plugins.

## Required WordPress setup

Install the following components:

* WooCommerce
* Astra theme
* Complianz

After installation:

1. Configure the WooCommerce store.
2. Create the product categories.
3. Add the products and product images.
4. Create the navigation menus.
5. Rebuild the homepage sections.
6. Add the legal and customer-service pages.
7. Add the custom CSS through:

```text
Appearance → Customize → Additional CSS
```

## WooCommerce functionality

WooCommerce provides the main webshop functionality, including:

* Products
* Product categories
* Prices
* Discounts
* Stock information
* Product variations
* Shopping cart
* Checkout
* Customer accounts
* Order management

The screenshots show a working product page where customers can select product options and add the item to their cart.

The shopping-cart page displays:

* Product information
* Product quantity
* Individual product price
* Cart subtotal
* Shipping options
* Total order value
* Checkout button

## Custom homepage

The homepage was designed to resemble a modern professional sportswear retailer.

It combines WooCommerce product shortcodes, custom HTML sections, images, banners, links, and CSS styling.

Example sections include:

* Promotional product cards
* Category carousels
* Brand banners
* Sport grids
* Collection banners
* Featured products
* Popular brands
* Customer-service navigation

## Custom styling

Custom CSS was used to modify the Astra and WooCommerce appearance.

The styling includes:

* Dark-blue and orange brand colors
* Custom header layout
* Promotional announcement bar
* Navigation menu styling
* Product cards
* Category circles
* Image banners
* Buttons and hover effects
* Footer columns
* Responsive layouts
* WooCommerce product and cart styling

## Legal and information pages

The website contains or was designed to contain pages such as:

* About Us
* Contact
* Vacancies
* Terms and conditions
* Privacy policy
* Cookie policy
* Returns
* Shipping information
* Payment information
* Frequently asked questions

Several pages were created using styled custom HTML blocks inside WordPress.

## GDPR and cookies

The Complianz plugin is used to provide:

* Cookie-consent notification
* Cookie-policy generation
* GDPR-related settings
* Consent management
* Privacy configuration

A production website would still require the legal content and cookie configuration to be reviewed for the business and country in which the store operates.

## Screenshots

### Homepage header and hero banner

![Header and hero banner](Screenshot_1.png)

### Categories and sports

![Popular categories and sports](Screenshot_2.png)

### Weekend deals and products

![Weekend deals and product grid](Screenshot_3.png)

### Popular brands and footer

![Popular brands](Screenshot_4.png)

### Brand campaigns and footwear

![Brand banners and footwear promotion](Screenshot_5.png)

### Clothing collections

![Collection banners](Screenshot_6.png)

### Brand overview

![Popular brands section](Screenshot_7.png)

### Footer

![Website footer](Screenshot_8.png)

### Product page

![WooCommerce product page](Screenshot_9.png)

### Shopping cart

![WooCommerce shopping cart](Screenshot_10.png)

## Repository limitations

The repository contains the Docker configuration and screenshots, but it does not include a complete export of the finished WordPress website.

The following files are not included:

* WordPress database export
* WordPress XML content export
* Astra child theme
* Custom CSS file
* Uploaded media library
* WooCommerce product export
* Plugin configuration
* Homepage block or page-builder export

Starting the Docker environment therefore creates a new WordPress installation rather than automatically restoring the completed website shown in the screenshots.

The pages, products, menus, images, plugins, and custom styling must be recreated manually unless a database and WordPress-content backup is added.

## Security notes

The database usernames and passwords in `docker-compose.yml` are intended for local development only.

For production use:

* Replace all default passwords.
* Store credentials in an environment file.
* Do not expose the MySQL service publicly.
* Use HTTPS.
* Keep WordPress, themes, and plugins updated.
* Use secure administrator credentials.
* Configure regular backups.
* Add security and spam protection.
* Review WooCommerce payment and privacy settings.

## Possible future improvements

* Add a complete WordPress database export.
* Include the `wp-content` directory or a theme export.
* Create a custom Astra child theme.
* Move custom CSS into a version-controlled stylesheet.
* Export WooCommerce products as CSV.
* Include a WordPress XML content export.
* Use a `.env` file for database credentials.
* Add Docker health checks.
* Add automated WordPress setup instructions.
* Configure a real payment provider.
* Add shipping-zone configuration.
* Add customer reviews and product ratings.
* Improve product filters.
* Add product wish lists.
* Add newsletter integration.
* Improve accessibility and keyboard navigation.
* Optimize images and page-loading performance.
* Add automated backups.
* Add deployment documentation.

## Learning goals

This project provided practical experience with:

* Installing and configuring WordPress
* Building an online store with WooCommerce
* Customizing the Astra theme
* Creating a professional webshop homepage
* Working with WordPress menus and widgets
* Creating WooCommerce products and categories
* Styling WordPress with custom CSS
* Creating custom HTML content blocks
* Configuring a shopping cart and checkout
* Working with WordPress plugins
* Implementing GDPR cookie consent
* Creating legal and information pages
* Running WordPress and MySQL with Docker
* Designing a consistent visual brand
* Building a responsive e-commerce layout

## Author

**Apo Panagiotidis**
