Shopify Inventory
A tool for managing and tracking inventory across your Shopify store — sync stock levels, get low-stock alerts, and keep your product catalog up to date.

Features

View and manage inventory levels for all products and variants
Sync inventory quantities with your Shopify store via the Admin API
Low-stock and out-of-stock alerts
Bulk update inventory across multiple locations
Export inventory data to CSV for reporting


Prerequisites

Node.js v18 or higher
A Shopify store with Admin API access
A Shopify API key and secret (see Setup)


Setup
1. Clone the repository
bashgit clone https://github.com/rt5899-art/Shopify-Inventory.git
cd Shopify-Inventory
2. Install dependencies
bashnpm install
3. Configure environment variables
Create a .env file in the root directory:
envSHOPIFY_STORE_URL=your-store.myshopify.com
SHOPIFY_API_KEY=your_api_key
SHOPIFY_API_SECRET=your_api_secret
SHOPIFY_ACCESS_TOKEN=your_access_token
To generate API credentials, go to your Shopify Admin → Apps → Develop apps → create a new app and enable the read_inventory and write_inventory scopes.
4. Run the application
bashnpm start

Usage
Once running, you can:

View inventory: Browse all products and their current stock levels across locations.
Update stock: Manually adjust quantities or trigger a sync with Shopify.
Set alerts: Configure thresholds to be notified when items run low.
Export: Download a CSV snapshot of your current inventory.


Project Structure
Shopify-Inventory/
├── src/
│   ├── api/          # Shopify API client and helpers
│   ├── inventory/    # Core inventory logic
│   └── utils/        # Shared utilities
├── .env.example      # Example environment config
├── package.json
└── README.md

Contributing
Contributions are welcome! To get started:

Fork the repository
Create a new branch: git checkout -b feature/your-feature
Make your changes and commit: git commit -m "Add your feature"
Push to your branch: git push origin feature/your-feature
Open a Pull Request

Please open an issue first for major changes to discuss what you'd like to do.# Shopify-Inventory
