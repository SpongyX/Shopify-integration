# Clerk Shopify Native Product Card Slider

This integration allows you to use Shopify's native product cards to render a product slider using Clerk.io. The slider is implemented using the Swiper library and can be customized through the Shopify admin interface.

## Installation

Follow these steps to install and configure the Clerk Shopify Native Product Card Slider:

### 1. Create the Template

Create a new file named [`templates/product.view.liquid`](templates/product.view.liquid).

### 2. Create the Section

Create a new file named [`sections/clerk-slider.liquid`](sections/clerk-slider.liquid).

### 3. Create the JavaScript File

Create a new file named [`assets/get-clerk-data.js`](assets/get-clerk-data.js).

### 4. Update the Theme Layout

Add the following code to [`layout/theme.liquid`](layout/theme.liquid) to ensure the slider runs:

```liquid
{% comment %}
  Inject this snippet alongside the original Clerk.io implementation.  
{% endcomment %}
{% if settings.enable_clerk %}
  {% render 'clerk-tracking' %}
  <script src="{{ 'get-clerk-data.js' | asset_url }}" type="module" defer="defer"></script>
  {% comment %} <script src="{{ 'clerk-sidecart.js' | asset_url }}" type="module" defer="defer"></script> {% endcomment %}
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
{% endif %}
```
## Example client:
  - [Tiffany Lighting Direct](https://www.tiffanylightingdirect.co.uk/) 
