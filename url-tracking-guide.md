# URL Tracking Guide

This guide explains how to use the redirect.html page to create trackable URLs for your DisputeDojo website.

## Basic Usage

The redirect page allows you to create links that track when users click them, and then redirect users to your main website (or any specific page you choose).

### Basic URL Structure

```
https://invite.disputedojo.com/redirect.html?source=linkedin&campaign=launch
```

This URL will:
1. Load the tracking pixel with the specified parameters
2. Redirect the user to your main website (disputedojo.com)

## Available Parameters

The redirect page accepts the following parameters:

| Parameter | Description | Example Values |
|-----------|-------------|----------------|
| source | Traffic source | linkedin, facebook, twitter |
| campaign | Campaign name | launch, summer_promo, webinar |
| medium | Marketing medium | social, email, banner |
| content | Content variant | blue_button, hero_image |
| to | Destination URL | https://disputedojo.com/pricing |

## Example URLs

### Basic tracking with redirect to homepage:
```
https://invite.disputedojo.com/redirect.html?source=newsletter&campaign=welcome
```

### Tracking with specific destination:
```
https://invite.disputedojo.com/redirect.html?source=facebook&campaign=ad_campaign&to=https://disputedojo.com/pricing
```

### Complete example with all parameters:
```
https://invite.disputedojo.com/redirect.html?source=twitter&campaign=product_launch&medium=social&content=tweet1&to=https://disputedojo.com/features
```

## Use Cases

### Email Marketing
Add trackable links in your email campaigns:
```html
<a href="https://invite.disputedojo.com/redirect.html?source=email&campaign=newsletter&medium=email&content=cta_button">Try DisputeDojo Now</a>
```

### Social Media
Create different links for different platforms to compare effectiveness:
```
Twitter: https://invite.disputedojo.com/redirect.html?source=twitter&campaign=summer&medium=social
LinkedIn: https://invite.disputedojo.com/redirect.html?source=linkedin&campaign=summer&medium=social
```

### QR Codes
Generate QR codes that link to your tracking URLs for offline marketing materials.

## Viewing Analytics

In Google Analytics (GA4):
1. Go to **Acquisition → Traffic acquisition**
2. Filter for the sources, campaigns, and mediums you used in your URLs
3. Create custom reports to analyze specific parameters

## Advanced: URL Shortening

For cleaner, shorter URLs, you can use a URL shortening service like Bitly or TinyURL:
1. Create your tracking URL with all parameters
2. Paste it into a URL shortener
3. Share the shortened URL 