# Pic Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Pic Scraper](https://oxylabs.io/products/scraper-api/ecommerce/pic?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Pic website effortlessly. This brief guide showcases how Pic Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Pic results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Pic page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.pic.bg/landing_pages/novi-predlojenia'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/pic-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"en\">\n<head>\n<link as=\"image\" href=\"/uploads/landing_page/background/194/ ... </html>",
      "created_at": "2024-02-20 12:51:40",
      "updated_at": "2024-02-20 12:51:41",
      "page": 1,
      "url": "https://www.pic.bg/landing_pages/novi-predlojenia",
      "job_id": "7165689466311440385",
      "status_code": 200
    }
  ]
}
```
With our Pic Scraper, you can easily extract public data from any Pic web page. Gather indispensable photography details such as resolution, date taken, or location metadata, to evaluate photography trends and stay ahead of your peers. If you need any assistance, reach out to our support team via live chat or shoot us an email at hello@oxylabs.io.