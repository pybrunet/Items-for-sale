# Items for Sale Landing Page

A beautiful, responsive landing page to showcase and sell your items with integrated Google Forms for offer submissions.

## Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Clean, professional design with hover effects and smooth animations
- **Google Forms Integration**: Collects offers and contact information automatically
- **SEO Friendly**: Optimized for search engines
- **Fast Loading**: Lightweight code with optimized images

## Items Included

1. Air Purifier - $75 OBO
2. Baby Bottles Set - $25 OBO
3. Child Car Seat - $120 OBO
4. Convertible Car Seat - $150 OBO
5. Coffee Maker - $60 OBO
6. Diaper Pack - $20 OBO
7. Humidifier - $45 OBO
8. Area Rug - $80 OBO
9. Decorative Rug - $65 OBO
10. Dinnerware Set - $40 OBO
11. Sleep Aid Product - $35 OBO

## Setup Instructions

### 1. Create Google Form

1. Go to [Google Forms](https://forms.google.com)
2. Create a new form with these fields:
   - **Item Name** (Short answer)
   - **Your Name** (Short answer)
   - **Email Address** (Short answer)
   - **Phone Number** (Short answer, optional)
   - **Offer Amount** (Short answer)
   - **Message/Questions** (Paragraph)

### 2. Get Your Form URL

1. Click the "Send" button in your Google Form
2. Copy the form URL
3. Extract the form ID from the URL (the long string after `/forms/d/` and before `/viewform`)

### 3. Update the Landing Page

Replace `YOUR_FORM_ID_HERE` in the HTML file with your actual Google Form ID:

```html
<!-- Line 386 -->
<a href="https://docs.google.com/forms/d/e/1FAIpQLSf_YOUR_ACTUAL_FORM_ID/viewform" class="google-sheets-btn" target="_blank">

<!-- Line 398 -->
const googleFormUrl = 'https://docs.google.com/forms/d/e/1FAIpQLSf_YOUR_ACTUAL_FORM_ID/viewform?usp=pp_url&entry.YOUR_ITEM_FIELD_ID=' + encodeURIComponent(itemName);
```

### 4. Pre-fill Item Names (Optional)

To automatically fill the item name when someone clicks "Make an Offer":

1. In your Google Form, click on the "Item Name" field
2. Click the three dots menu → "Get pre-filled link"
3. Enter a test item name and click "Get link"
4. From the URL, copy the `entry.XXXXXXXXX` number
5. Replace `YOUR_ITEM_FIELD_ID` in the JavaScript with this number

### 5. Customize Colors (Optional)

To match your pybrunet.com theme, update these CSS variables:

```css
/* Current gradient colors */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Update with your brand colors */
background: linear-gradient(135deg, #YOUR_COLOR_1 0%, #YOUR_COLOR_2 100%);
```

## File Structure

```
/
├── index.html          # Main landing page
├── README.md          # This file
├── Air_Purifier.jpg   # Product images
├── Baby_Bottles.jpg
├── Carseat1.jpg
├── Carseat4.jpg
├── Coffe1.jpg
├── Diaper.jpg
├── Humidifyer.jpg
├── Rug1.JPG
├── Rug2.JPG
├── Set1.jpg
└── Sleep.jpg
```

## Hosting

You can host this landing page on:
- **GitHub Pages** (free)
- **Netlify** (free)
- **Vercel** (free)
- Any web hosting service

## Contact

For questions about items, please use the offer form on the website.

---

*All items are sold as-is. Serious inquiries only.* 