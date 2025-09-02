# Shopify E-commerce Automation Templates

This folder contains n8n workflow templates specifically designed for Shopify e-commerce automation and optimization.

## Available Templates

### `back_in_stock.json` - Back-in-Stock / Daily Inventory Alert

Automatically monitors inventory levels and sends alerts when products are running low.

#### **What it does:**
- Runs daily at 8 AM to check all product inventory
- Identifies products with low stock (≤ 5 units by default)
- Sends formatted alerts to Slack with product details and links
- Includes both customer-facing product URLs and admin management URLs

#### **Key Features:**
- **Daily Monitoring** - Automated daily inventory checks
- **Smart Filtering** - Only alerts on products with stock > 0 but ≤ threshold
- **Rich Alerts** - Includes product title, variant, SKU, quantity, and links
- **Admin Integration** - Direct links to Shopify admin for quick restocking

#### **Configuration:**
- `LOW_STOCK_THRESHOLD` - Adjust the low stock threshold (default: 5)
- `SHOP_DOMAIN` - Your Shopify store domain for URL generation
- Slack channel for alerts

#### **Required Credentials:**
- **Shopify API** - For accessing product inventory data
- **Slack API** - For sending inventory alerts

---

### `dynamic_collection_sort.json` - Dynamic Collection Sorting

Automatically reorders product collections based on sales performance to optimize conversion rates.

#### **What it does:**
- Runs daily at 6 AM to analyze recent sales data
- Fetches orders from the last 14 days
- Calculates revenue and quantity sold for each product
- Ranks products by revenue performance
- Updates collection order to feature best-performing products first
- Posts top 5 performers to Slack for visibility

#### **Key Features:**
- **Performance-Based Sorting** - Products ranked by actual sales revenue
- **14-Day Window** - Uses recent sales data for relevance
- **Automatic Updates** - Daily collection reordering
- **Performance Tracking** - Slack notifications with top performers

#### **Configuration:**
- Collection ID to update
- Shopify store domain
- Slack channel for performance updates

#### **Required Credentials:**
- **Shopify API** - For accessing orders and updating collections
- **Slack API** - For performance notifications

---

### `high_aov_recovery.json` - High-AOV Recovery (Concierge)

Identifies high-value abandoned carts and provides personalized recovery sequences.

#### **What it does:**
- Runs every 2 hours to check for abandoned checkouts
- Filters for high-value carts (≥ $150 by default)
- Identifies carts older than 2 hours
- Sends personalized recovery messages via WhatsApp (if phone available) or email
- Provides concierge-level service with specific help options

#### **Key Features:**
- **High-Value Focus** - Only targets carts ≥ $150 AOV
- **Multi-Channel** - WhatsApp preferred, email fallback
- **Personalized Messages** - Includes cart value and checkout link
- **Concierge Service** - Offers specific help options (sizing, shipping, alternatives)
- **Smart Timing** - Only contacts after 2-hour abandonment window

#### **Configuration:**
- AOV threshold (default: $150)
- WhatsApp phone number for sending
- Gmail credentials for email fallback

#### **Required Credentials:**
- **Shopify API** - For accessing abandoned checkouts
- **Twilio API** - For WhatsApp messaging
- **Gmail API** - For email recovery messages

---

### `vip_tagging_and_drops.json` - VIP Tagging & Drops

Automatically identifies VIP customers and manages exclusive marketing campaigns.

#### **What it does:**
- Monitors Shopify orders every 15 minutes
- Calculates customer lifetime value (LTV) from all paid orders
- Identifies VIP customers (≥ $500 LTV by default)
- Adds VIP customers to Klaviyo VIP list
- Sends WhatsApp congratulations message to new VIPs
- Tracks customer order history and LTV growth

#### **Key Features:**
- **Real-Time Monitoring** - Checks for new orders every 15 minutes
- **LTV Calculation** - Tracks total customer lifetime value
- **VIP Identification** - Automatic VIP status based on spending
- **Klaviyo Integration** - Adds VIPs to marketing lists
- **WhatsApp Notifications** - Congratulates new VIP customers
- **Comprehensive Tracking** - Monitors email, phone, LTV, and order count

#### **Configuration:**
- VIP threshold (default: $500 LTV)
- Klaviyo VIP list ID
- WhatsApp Business phone number ID

#### **Required Credentials:**
- **Shopify API** - For accessing order history
- **Klaviyo API** - For VIP list management
- **WhatsApp Business API** - For VIP notifications

## Common Setup Requirements

### **Shopify API Setup:**
1. Create a Private App in your Shopify admin
2. Enable required permissions:
   - `read_products` - For inventory monitoring
   - `read_orders` - For order analysis
   - `write_products` - For collection updates
   - `read_checkouts` - For abandoned cart recovery

### **General Configuration:**
- Update all placeholder values with your actual credentials
- Adjust thresholds based on your business needs
- Configure Slack channels for notifications
- Set up proper webhook endpoints for external integrations

### **Best Practices:**
- Test workflows with small batches first
- Monitor execution logs for any errors
- Adjust timing and thresholds based on your business patterns
- Ensure compliance with messaging consent requirements
- Regularly review and optimize based on performance metrics
