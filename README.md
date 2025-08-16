# Shopify + AI Automations (n8n templates)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Created and maintained by Mohamed Chebbi (@chebbi4m).

*Automate what repeats. Amplify what converts.*

## Repository Structure

```
.
└── shopify/
    ├── back_in_stock.json
    ├── high_aov_recovery.json
    ├── dynamic_collection_sort.json
    └── vip_tagging_and_drops.json
```

More automation folders (beyond Shopify) will be added over time.

## What's Inside

### **Back-in-Stock / Daily Inventory Alert**
Automatically notifies customers when out-of-stock items become available and sends daily inventory reports to your team.
**Trigger:** Daily at 9 AM / Product inventory changes
**Stack:** Shopify + n8n + Slack/Klaviyo
**Metrics to watch:** Back-in-stock conversion rate, inventory turnover, customer satisfaction

### **High-AOV Recovery (Concierge)**
Identifies high-value customers with abandoned carts and provides personalized recovery sequences with concierge-level service.
**Trigger:** Cart abandonment (AOV ≥ $150)
**Stack:** Shopify + n8n + Klaviyo + Slack
**Metrics to watch:** Recovery rate, AOV, customer lifetime value

### **Dynamic Collection Sorting**
Automatically reorders product collections based on performance metrics, ensuring your best products are always featured first.
**Trigger:** Weekly / Performance threshold changes
**Stack:** Shopify + n8n
**Metrics to watch:** Collection conversion rates, product performance, revenue per collection

### **VIP Tagging & Drops**
Automatically tags VIP customers (LTV ≥ $500) and sends exclusive product drops and early access notifications.
**Trigger:** Customer purchase / LTV threshold reached
**Stack:** Shopify + n8n + Klaviyo + Slack
**Metrics to watch:** VIP retention, exclusive drop conversion, customer LTV growth

## Requirements

- **n8n** (self-hosted or cloud)
- **Shopify Admin API** credentials
- **Optional integrations** used by specific flows:
  - Slack (notifications)
  - Twilio (WhatsApp messaging)
  - Gmail (email automation)
  - Klaviyo (marketing automation)

> **Note:** Always respect messaging consent and opt-in requirements for your customers.

## Quick Start

### Import & Configure

1. **Import workflow:** Go to `Workflows → Import from file` and choose a JSON from `shopify/`
2. **Set credentials:** Configure all nodes (Shopify, Slack, Twilio/Gmail, Klaviyo)
3. **Edit placeholders:** Update `YOUR_SHOP_DOMAIN`, `YOUR_KLAVIYO_API_KEY`, `YOUR_LIST_ID`, WhatsApp from, Slack channel
4. **Adjust thresholds:** Modify AOV ($150) and VIP ($500) thresholds in IF/Function/Set nodes
5. **Activate:** Turn on the workflow and test with a small batch

## Roadmap

- Post-purchase one-click upsell automation
- Second-purchase accelerator flows
- Browse-abandon nudge with Voice of Customer snippets
- Preorder/backorder auto-switch logic
- Non-Shopify flows (Klaviyo utilities, Zendesk automation, Meta ads optimization)

**Star ⭐ the repo to get updates.**

## Support / Custom Builds

Need help with these automations or want something custom built? Open an [Issue](https://github.com/chebbi4m/n8n-templates/issues) or reach out directly:

- **Email:** [YOUR_EMAIL]
- **LinkedIn:** [Mohamed Chebbi](https://www.linkedin.com/in/mohamed-chebbi-694685156/)
- **Portfolio:** [portfolio2-0-nymh.onrender.com](https://portfolio2-0-nymh.onrender.com)

## Author

Hi, I'm Mohamed Chebbi — Shopify expert building no-code AI automations for e-commerce.

*Automate what repeats. Amplify what converts.*

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
