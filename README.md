# Product Approval

![Version](https://img.shields.io/badge/version-19.0.0.0-blue)
![Category](https://img.shields.io/badge/category-Extra%20Tools-green)
![License](https://img.shields.io/badge/license-LGPL-3-orange)

| | |
|---|---|
| **Name** | Product Approval |
| **Version** | 19.0.0.0 |
| **Category** | Extra Tools |
| **Author** | ZestyBeanz Technologies |
| **License** | LGPL-3 |
| **Application** | No (Addon) |
| **Website** | http://www.zbeanztech.com/ |

## Description

This module helps to manage the product approval process with Draft & Approve Stages. Sales Order / Purchase Order can be confirmed & Invoice can be Posted only when the Products are in Approved Stage.

## Functionality

### Models & Fields

#### Extends `account.move`

**File:** `models/account_move.py`

**Inherits:** `account.move`

**Key Methods:**

- `action_post()` — Action/workflow method

#### Extends `product.template, product.product`

**File:** `models/product.py`

**Inherits:** `product.template`, `product.product`

**Fields:**

| Field | Type |
|-------|------|
| `state` | `Selection` |
| `mapped_product_tmpl_id` | `Many2one` |
| `mapped_product_id` | `Many2one` |

**Key Methods:**

- `action_verify()` — Action/workflow method
- `write()` — Overridden ORM method
- `action_map_product()` — Action/workflow method
- `action_draft()` — Action/workflow method
- `action_verify()` — Action/workflow method
- `action_map_product()` — Action/workflow method
- `action_draft()` — Action/workflow method

#### Extends `purchase.order`

**File:** `models/purchase_order.py`

**Inherits:** `purchase.order`

**Key Methods:**

- `button_confirm()` — Button handler

#### Extends `sale.order`

**File:** `models/sale_order.py`

**Inherits:** `sale.order`

**Key Methods:**

- `action_confirm()` — Action/workflow method

#### Extends `stock.picking`

**File:** `models/stock_picking.py`

**Inherits:** `stock.picking`

**Key Methods:**

- `button_validate()` — Button handler

### Views & UI

### Security

**Security Groups:**

- Product Manager

## Dependencies

| Module | Type |
|--------|------|
| `sale_management` | Odoo Core |
| `purchase` | Odoo Core |
| `stock` | Odoo Core |

## File Structure

```
zb_product_approve/
├── LICENSE
├── README.md
├── __init__.py
├── __manifest__.py
├── models/
│   ├── __init__.py
│   ├── account_move.py
│   ├── product.py
│   ├── purchase_order.py
│   ├── sale_order.py
│   └── stock_picking.py
├── security/
│   └── security.xml
├── static/
│   └── description/
│       ├── banners/
│       ├── icon.png
│       ├── images/
│       └── index.html
└── views/
    └── product_view.xml
```

## Installation

This module is part of the **[odoo-crm-sales-suite](https://github.com/tejas7287/odoo-crm-sales-suite)** suite.

1. Place this module in your Odoo addons directory
2. Update the apps list: **Settings** → **Apps** → **Update Apps List**
3. Search for **"Product Approval"** and click **Install**

## License

LGPL-3
