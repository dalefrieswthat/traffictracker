# Transparent Tracking Pixel

A simple transparent 1x1 pixel image for tracking user visits from emails and web pages.

## How It Works

This repository contains a transparent 1x1 pixel image that can be embedded in emails and web pages. When someone opens an email or views a page with this pixel, their browser loads the image, which allows Google Analytics to track the view along with any parameters added to the URL.

## Setup Instructions

### 1. Host the Pixel on GitHub Pages

1. Push this repository to GitHub
2. Enable GitHub Pages in the repository settings:
   - Go to Settings > Pages
   - Select "main" as the source branch
   - Save the settings
3. GitHub Pages will generate a URL for your pixel:
   ```
   https://yourusername.github.io/reponame/pixel.png
   ```

### 2. Track Email Opens

Add the pixel to your email templates with tracking parameters:

```html
<img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=newsletter" 
     alt="" style="width:1px;height:1px;">
```

Customize the parameters for different email campaigns:
```html
<img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=welcome" alt="" style="width:1px;height:1px;">
<img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=promotion" alt="" style="width:1px;height:1px;">
```

### 3. Track Website Page Views in Softr

Add a Custom HTML block to each Softr page you want to track:

```html
<img src="https://yourusername.github.io/reponame/pixel.png?source=website&page=homepage" 
     alt="" style="width:1px;height:1px;">
```

Use different parameters for different pages:
```html
<img src="https://yourusername.github.io/reponame/pixel.png?source=website&page=pricing" alt="" style="width:1px;height:1px;">
<img src="https://yourusername.github.io/reponame/pixel.png?source=website&page=features" alt="" style="width:1px;height:1px;">
```

## Tracking Parameters

You can add these parameters to customize your tracking:

| Parameter | Description | Example Values |
|-----------|-------------|----------------|
| source | Traffic source | email, website, social |
| campaign | Campaign name | newsletter, welcome, promotion |
| page | Page identifier | homepage, pricing, features |
| medium | Marketing medium | email, banner, cpc |
| content | Content variant | version_a, button_blue |

## Viewing Analytics Data

In Google Analytics 4:

1. Go to **Reports** → **Acquisition** → **Traffic acquisition**
2. Look for traffic with the source/medium parameters you specified
3. Create custom reports to analyze specific parameters

## Email Tracking Example

To track different email campaigns:

1. Welcome Email:
   ```html
   <img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=welcome" alt="" style="width:1px;height:1px;">
   ```

2. Newsletter:
   ```html
   <img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=newsletter" alt="" style="width:1px;height:1px;">
   ```

3. Promotion:
   ```html
   <img src="https://yourusername.github.io/reponame/pixel.png?source=email&campaign=black_friday" alt="" style="width:1px;height:1px;">
   ```

This lets you compare open rates between different email campaigns.

## Files in this Repository

- `pixel.png`