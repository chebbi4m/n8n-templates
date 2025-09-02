# n8n Automation Templates

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Created and maintained by Mohamed Chebbi (@chebbi4m).

*Automate what repeats. Amplify what converts.*

## Repository Structure

```
.
├── booking/
│   └── booking_template.json
└── shopify/
    ├── back_in_stock.json
    ├── high_aov_recovery.json
    ├── dynamic_collection_sort.json
    └── vip_tagging_and_drops.json
```

This repository contains ready-to-use n8n workflow templates for various business automation needs. Each folder contains specialized workflows for different platforms and use cases.

## What's Inside

### **Booking Automation**
Multi-channel booking system that captures reservations from website, phone, WhatsApp, Messenger, Instagram, and email, then processes them with AI and stores them in Google Sheets.

### **Shopify E-commerce Automations**
- **Back-in-Stock / Daily Inventory Alert** - Automated inventory monitoring and alerts
- **High-AOV Recovery (Concierge)** - Personalized cart abandonment recovery for high-value customers
- **Dynamic Collection Sorting** - Auto-optimize product collections based on performance
- **VIP Tagging & Drops** - Automatic VIP customer identification and exclusive notifications

## How to Use

### Step 1: Import Workflow
1. Open your n8n instance (self-hosted or cloud)
2. Navigate to **Workflows** → **Import from file**
3. Select the JSON file from the appropriate folder
4. The workflow will be imported with all nodes and connections

### Step 2: Configure Credentials
Each workflow requires specific API credentials. Configure them in n8n:

1. **Go to Settings** → **Credentials**
2. **Add new credentials** for each service used:
   - **Shopify API** - For e-commerce workflows
   - **OpenAI API** - For AI-powered features
   - **Google Sheets API** - For data storage
   - **Twilio API** - For WhatsApp/SMS messaging
   - **Slack API** - For notifications
   - **Gmail API** - For email automation
   - **Klaviyo API** - For marketing automation
   - **WhatsApp Business API** - For WhatsApp messaging

### Step 3: Update Configuration
After importing, update these placeholders in the workflow:

- `YOUR_SHOP_DOMAIN` → Your Shopify store domain
- `YOUR_SHEET_ID` → Your Google Sheets ID
- `YOUR_KLAVIYO_API_KEY` → Your Klaviyo API key
- `YOUR_LIST_ID` → Your Klaviyo list ID
- `YOUR_WHATSAPP_PHONE_NUMBER_ID` → Your WhatsApp Business phone number ID
- Channel names (Slack channels, etc.)
- Threshold values (AOV amounts, VIP limits, etc.)

### Step 4: Test and Activate
1. **Test the workflow** with a small batch first
2. **Check all connections** and data flow
3. **Activate the workflow** when ready
4. **Monitor execution** and adjust as needed

## Requirements

- **n8n** (self-hosted or cloud)
- **API credentials** for the services used in each workflow
- **Proper permissions** for all integrated services

> **Note:** Always respect messaging consent and opt-in requirements for your customers.

## Roadmap

- Post-purchase one-click upsell automation
- Second-purchase accelerator flows
- Browse-abandon nudge with Voice of Customer snippets
- Preorder/backorder auto-switch logic
- Non-Shopify flows (Klaviyo utilities, Zendesk automation, Meta ads optimization)

**Star ⭐ the repo to get updates.**

## Support / Custom Builds

Need help with these automations or want something custom built? Open an [Issue](https://github.com/chebbi4m/n8n-templates/issues) or reach out directly:

- **Email:** [chebbim4@gmail.com]
- **LinkedIn:** [Mohamed Chebbi](https://www.linkedin.com/in/mohamed-chebbi-694685156/)
- **Portfolio:** [portfolio2-0-nymh.onrender.com](https://portfolio2-0-nymh.onrender.com)

## Author

Hi, I'm Mohamed Chebbi — Shopify expert building no-code AI automations for e-commerce.

*Automate what repeats. Amplify what converts.*

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
