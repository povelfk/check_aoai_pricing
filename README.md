# Azure OpenAI Pricing Tool

A Jupyter notebook tool to fetch and display Azure OpenAI pricing data using the Azure Retail Prices API.

## Features

- Search for specific models (GPT-4o, GPT-4 Turbo, etc.)
- Filter by Azure regions
- Support for multiple currencies (USD, EUR, SEK, etc.)
- Clean, formatted output
- Automatic pagination handling

## Usage

1. Open `pricing.ipynb` in Jupyter or VS Code
2. Run the helper functions cell
3. Use `get_aoai_prices()` to fetch pricing data

```python
# Example: Get GPT-4o prices in Sweden Central
df = get_aoai_prices(region="swedencentral", model_substr="gpt-4o", currency="USD")
```

## Requirements

- `requests` - for API calls
- `pandas` - for data handling

Install with:
```bash
pip install requests pandas
```

## Parameters

- `region` - Azure region (e.g., "swedencentral", "westeurope")
- `model_substr` - Model name substring (e.g., "gpt-4o", "GPT-4 Turbo")
- `currency` - Currency code (e.g., "USD", "EUR", "SEK")
- `product_name` - Service name (default: "Azure OpenAI")