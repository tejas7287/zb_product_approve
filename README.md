# Product Approval

**Version:** 19.0.0.0  
**Category:** Extra Tools  
**License:** LGPL-3  
**Author:** ZestyBeanz Technologies
**Website:** http://www.zbeanztech.com/

## Description

This module helps to manage the product approval process with Draft & Approve Stages. Sales Order / Purchase Order can be confirmed & Invoice can be Posted only when the Products are in Approved Stage.

## Features

- Odoo 19.0 compatible
- Addon module


## Dependencies

This module depends on the following Odoo modules:

- `sale_management`
- `purchase`
- `stock`

## Installation

1. Clone this repository into your Odoo addons directory:
   ```bash
   git clone https://github.com/tejas7287/zb_product_approve.git
   ```

2. Add the module path to your Odoo configuration file (`odoo.conf`):
   ```
   addons_path = /path/to/odoo/addons,/path/to/zb_product_approve
   ```

3. Restart the Odoo server:
   ```bash
   sudo systemctl restart odoo
   ```

4. Go to **Apps** → **Update Apps List** → Search for **"Product Approval"** → Click **Install**

## Module Structure

```
zb_product_approve/
├── __init__.py
├── __manifest__.py
├── models/
├── security/
├── static/
├── views/
```

## Configuration

After installation, configure the module through Odoo's Settings menu or the module's specific configuration options.

## License

This project is licensed under the LGPL-3 License.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
