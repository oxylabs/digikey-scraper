# Digikey Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/Pds3gBmKMH)

Oxylabs' [Digikey Scraper](https://oxylabs.io/products/scraper-api/ecommerce/digikey?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Digikey website effortlessly. This brief guide showcases how Digikey Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Digikey results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Digikey page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.digikey.de/en/products/filter/industrial-automation-accessories/800'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/digikey-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-de\" dir=\"ltr\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" conte ... </html>",
      "created_at": "2024-02-20 12:16:45",
      "updated_at": "2024-02-20 12:16:49",
      "page": 1,
      "url": "https://www.digikey.de/en/products/filter/industrial-automation-accessories/800",
      "job_id": "7165680679466858497",
      "status_code": 200
    }
  ]
}
```
With our Digikey Scraper tool, you are empowered to seamlessly pull out public data from any Digikey pages. Gather pertinent product specs, such as circuit type, power rating, or manufacturer, to gather market insights and outmaneuver the competition. For any inquiries, reach out to our dedicated support team through live chat or email us at hello@oxylabs.io.
