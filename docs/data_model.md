# Olist Data Model

## Overview

The project uses the Brazilian E-Commerce Public Dataset by Olist.

The dataset contains multiple related tables covering customers, orders,
products, sellers, payments, reviews and geographic information.

## Core relationships

```text
customers
    |
    | customer_id
    |
    v
orders
    |
    +-------------------> payments
    |
    +-------------------> reviews
    |
    |
    v
order_items
    |
    +-------------------> products
    |                         |
    |                         |
    |                         v
    |                  category_translation
    |
    +-------------------> sellers


customers
    |
    | customer_zip_code_prefix
    v
geolocation

sellers
    |
    | seller_zip_code_prefix
    v
geolocation