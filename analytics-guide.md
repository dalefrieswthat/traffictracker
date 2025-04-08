# Tracking Pixel Analytics Guide

This guide explains how to view and analyze the data collected using your tracking pixel.

## Setting Up Google Analytics in Softr

1. **Add Google Analytics to Your Softr Website**:
   - In your Softr dashboard, go to Settings → Integrations
   - Connect Google Analytics by adding your GA4 Measurement ID
   - If you don't have a GA4 property, create one at [analytics.google.com](https://analytics.google.com)

## Viewing Email Tracking Data

When someone opens an email containing your tracking pixel, GA4 captures this as a pageview event. Here's how to view this data:

1. **Email Open Analysis**:
   - In GA4, go to **Reports** → **Acquisition** → **Traffic acquisition**
   - Look for traffic with Source = "email"
   - You can see which email campaigns had the most opens by looking at the Campaign dimension

2. **Email Campaign Comparison**:
   - Go to **Reports** → **Acquisition** → **Traffic acquisition**
   - Add a comparison by clicking "Add comparison" and setting the dimension to "Campaign"
   - You can now compare different email campaigns side by side

## Viewing Website Tracking Data

For tracking pixel views on your Softr pages:

1. **Page View Analysis**:
   - In GA4, go to **Reports** → **Acquisition** → **Traffic acquisition**
   - Look for traffic with Source = "website"
   - You can see which pages were viewed most by looking at the "page" parameter

## Creating Custom Reports for Deeper Analysis

For more detailed analysis, create a custom report:

1. Go to **Customization** → **Custom Reports** → **New Custom Report**
2. Add the following dimensions:
   - Source
   - Campaign
   - Page
   - Medium
   - Content
3. Add metrics:
   - Event count
   - Sessions
4. Save and view your report

## Real-world Examples

### Tracking Email Marketing Effectiveness

If you have these tracking pixels in different email campaigns:
```html
<img src="https://yourusername.github.io/pixel/pixel.png?source=email&campaign=welcome" alt="">
<img src="https://yourusername.github.io/pixel/pixel.png?source=email&campaign=product_update" alt="">
```

In GA4, you can:
- Compare which email had more opens
- See when emails are typically opened (time of day)
- Analyze which devices people use to read emails

### Tracking Website Page Performance

If you have pixels on different pages:
```html
<img src="https://yourusername.github.io/pixel/pixel.png?source=website&page=homepage" alt="">
<img src="https://yourusername.github.io/pixel/pixel.png?source=website&page=pricing" alt="">
```

In GA4, you can:
- See which pages get the most views
- Compare traffic between different sections
- Analyze user engagement patterns

## Data Privacy Considerations

When using tracking pixels, keep these privacy considerations in mind:

- Include information about tracking pixels in your privacy policy
- Be aware of email tracking notifications in modern email clients
- Ensure compliance with privacy regulations like GDPR and CCPA 