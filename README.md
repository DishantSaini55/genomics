# 🧬 Genomics Research & Diagnostics Centre

A modern, responsive medical diagnostics laboratory website built with HTML5, CSS3, and JavaScript with EmailJS integration for contact form functionality.

---

## 📋 Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [File Structure](#file-structure)
- [Setup Instructions](#setup-instructions)
- [EmailJS Configuration](#emailjs-configuration)
- [Deployment](#deployment)
- [Customization Guide](#customization-guide)
- [Browser Support](#browser-support)
- [Contact](#contact)

---

## ✨ Features

### Core Features
- ✅ **Fully Responsive Design** - Works seamlessly on mobile, tablet, and desktop
- ✅ **Modern UI/UX** - Clean, professional medical-grade design
- ✅ **Lab Tests Catalog** - 9 different medical tests with details and pricing
- ✅ **Search & Filter** - Real-time search and sort functionality for tests
- ✅ **Booking System** - Modal-based and form-based booking options
- ✅ **EmailJS Integration** - Automated email notifications for enquiries
- ✅ **Form Validation** - Client-side validation with error messages
- ✅ **Smooth Animations** - Scroll animations and hover effects
- ✅ **Sticky Navigation** - Fixed navbar with smooth scroll
- ✅ **Toast Notifications** - Success/error messages for user feedback
- ✅ **Google Maps Integration** - Interactive map showing lab location
- ✅ **Scroll to Top Button** - Easy navigation back to top
- ✅ **Animated Statistics** - Counter animations for key metrics

### Design Features
- 🎨 **Color Scheme**: White + Blue (#0066cc) + Light Red (#ff4757)
- 🎨 **Modern Typography**: Segoe UI font family
- 🎨 **CSS Variables**: Easy customization
- 🎨 **Smooth Transitions**: 0.3s ease transitions throughout
- 🎨 **Box Shadows**: Modern depth and elevation
- 🎨 **Gradient Overlays**: Professional hero section

---

## 🛠 Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with Flexbox & Grid
- **JavaScript (ES6+)** - Interactive functionality
- **EmailJS** - Email service integration
- **Font Awesome 6.4.0** - Icon library
- **Google Maps** - Location embedding

---

## 📁 File Structure

```
GENOMICS/
│
├── index.html          # Main HTML file with all sections
├── style.css           # Complete CSS styling
├── script.js           # JavaScript functionality
└── README.md          # Documentation (this file)
```

---

## 🚀 Setup Instructions

### Step 1: Download Files

1. Ensure you have all three files in the same directory:
   - `index.html`
   - `style.css`
   - `script.js`

### Step 2: Open the Website

**Option A: Direct Opening**
- Double-click `index.html`
- The website will open in your default browser

**Option B: Using Live Server (Recommended for Development)**
- Install VS Code with Live Server extension
- Right-click `index.html` → "Open with Live Server"
- Website opens at `http://localhost:5500`

### Step 3: Test the Website

1. Navigate through all sections
2. Test search and filter functionality
3. Try booking a test (modal and form)
4. Verify responsive design on different screen sizes

---

## 📧 EmailJS Configuration

EmailJS is used to send form submissions directly to your email without a backend server.

### Step 1: Create EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

### Step 2: Add Email Service

1. Go to **Email Services** in your EmailJS dashboard
2. Click **Add New Service**
3. Choose your email provider (Gmail, Outlook, etc.)
4. Follow the connection wizard
5. **Copy the Service ID** (e.g., `service_abc123`)

### Step 3: Create Email Template

1. Go to **Email Templates** in dashboard
2. Click **Create New Template**
3. Use this template structure:

```
Subject: New Test Booking Enquiry - {{test_name}}

From: {{from_name}}
Email: {{from_email}}
Mobile: {{from_mobile}}

Selected Test: {{test_name}}

Message:
{{message}}

---
This enquiry was submitted through the Genomics Centre website.
```

4. **Copy the Template ID** (e.g., `template_xyz789`)

### Step 4: Get Public Key

1. Go to **Account** → **General**
2. Find your **Public Key** (e.g., `abc123XYZ`)
3. Copy this key

### Step 5: Update script.js

Open `script.js` and replace the placeholder values:

```javascript
const EMAILJS_CONFIG = {
    SERVICE_ID: 'service_abc123',      // Your Service ID
    TEMPLATE_ID: 'template_xyz789',    // Your Template ID
    PUBLIC_KEY: 'abc123XYZ'            // Your Public Key
};
```

### Step 6: Test Email Functionality

1. Open the website
2. Fill out the booking form
3. Click "Send Enquiry"
4. Check your email inbox for the notification
5. Verify all details are correctly received

### EmailJS Template Variables

The form sends these variables to your email:

- `{{to_name}}` - "Genomics Centre Team"
- `{{from_name}}` - Customer's full name
- `{{from_email}}` - Customer's email
- `{{from_mobile}}` - Customer's mobile number
- `{{test_name}}` - Selected test name
- `{{message}}` - Additional message/notes
- `{{reply_to}}` - Customer's email for replies

---

## 🌐 Deployment

### Option 1: Netlify (Recommended - FREE)

#### Step-by-Step:

1. **Create Account**
   - Go to [Netlify.com](https://www.netlify.com/)
   - Sign up with GitHub, GitLab, or email

2. **Deploy via Drag & Drop**
   - Click "Sites" → "Add new site" → "Deploy manually"
   - Drag your project folder (containing all 3 files)
   - Wait 30 seconds for deployment

3. **Get Your URL**
   - You'll receive a URL like: `https://random-name-123.netlify.app`
   - Your site is now live!

4. **Custom Domain (Optional)**
   - Go to Site Settings → Domain Management
   - Add your custom domain
   - Follow DNS configuration instructions

#### Netlify Features:
- ✅ Free hosting
- ✅ HTTPS by default
- ✅ Automatic deployments
- ✅ Custom domain support
- ✅ Form handling (alternative to EmailJS)

---

### Option 2: Vercel (FREE)

#### Step-by-Step:

1. **Create Account**
   - Go to [Vercel.com](https://vercel.com/)
   - Sign up with GitHub, GitLab, or email

2. **Deploy**
   - Click "New Project"
   - Import your project or drag & drop files
   - Click "Deploy"

3. **Get Your URL**
   - URL format: `https://your-project.vercel.app`
   - Instant global CDN deployment

4. **Custom Domain**
   - Project Settings → Domains
   - Add custom domain

#### Vercel Features:
- ✅ Free hosting
- ✅ Global CDN
- ✅ HTTPS automatic
- ✅ Instant deployments
- ✅ Analytics

---

### Option 3: GitHub Pages (FREE)

#### Step-by-Step:

1. **Create GitHub Repository**
   - Go to [GitHub.com](https://github.com/)
   - Create new repository (public)
   - Upload your 3 files

2. **Enable GitHub Pages**
   - Repository Settings → Pages
   - Source: Deploy from branch
   - Branch: main / master
   - Folder: / (root)
   - Click Save

3. **Access Your Site**
   - URL: `https://username.github.io/repository-name`
   - Wait 2-3 minutes for deployment

#### GitHub Pages Features:
- ✅ Free hosting
- ✅ Version control
- ✅ Custom domain support
- ✅ HTTPS

---

### Option 4: Traditional Web Hosting

If you have a hosting provider (Bluehost, GoDaddy, HostGator, etc.):

1. **Upload Files via FTP**
   - Use FileZilla or cPanel File Manager
   - Upload all 3 files to `public_html` folder

2. **Access Your Site**
   - Visit your domain: `https://yourdomian.com`

---

## 🎨 Customization Guide

### Change Colors

Edit CSS variables in `style.css`:

```css
:root {
    --primary-blue: #0066cc;           /* Main blue color */
    --secondary-red: #ff4757;          /* Accent red color */
    --primary-dark-blue: #004999;      /* Darker blue */
}
```

### Add More Tests

In `index.html`, copy this block and modify:

```html
<div class="test-card" data-name="Test Name" data-price="500">
    <div class="test-icon">
        <i class="fas fa-vial"></i>
    </div>
    <h3 class="test-name">Test Name</h3>
    <p class="test-description">Test description here...</p>
    <div class="test-price">₹500</div>
    <button class="btn btn-book" onclick="openBookingModal('Test Name', '500')">
        <i class="fas fa-calendar-check"></i> Book Now
    </button>
</div>
```

Also add to the form dropdown in both forms:

```html
<option value="Test Name">Test Name - ₹500</option>
```

### Change Contact Information

Edit in `index.html` - search for:
- Phone: `+91 8572851031`
- Email: `Info.genomicscentre@gmail.com`
- Address: `97, Street No 8, Vasant Vihar, Karnal, Haryana 132001`

### Modify Google Map

In `index.html`, find the iframe and replace the `src` with your location:

1. Go to [Google Maps](https://www.google.com/maps)
2. Search for your location
3. Click "Share" → "Embed a map"
4. Copy the iframe code
5. Replace the existing iframe in HTML

### Change Logo/Branding

Current icon: `<i class="fas fa-dna"></i>`

To use a custom logo:
```html
<img src="your-logo.png" alt="Genomics Centre" style="height: 40px;">
```

---

## 📱 Browser Support

| Browser | Version |
|---------|---------|
| Chrome | 90+ |
| Firefox | 88+ |
| Safari | 14+ |
| Edge | 90+ |
| Opera | 76+ |

**Mobile Browsers:**
- iOS Safari 14+
- Chrome Mobile
- Firefox Mobile
- Samsung Internet

---

## ⚙️ Advanced Features (Optional)

### Add Google Analytics

Add before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Add Facebook Pixel

Add before `</head>` in `index.html`:

```html
<!-- Facebook Pixel -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

### Add WhatsApp Chat Button

Add before `</body>` in `index.html`:

```html
<!-- WhatsApp Chat Button -->
<a href="https://wa.me/918572851031" class="whatsapp-float" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<style>
.whatsapp-float {
    position: fixed;
    bottom: 90px;
    right: 30px;
    width: 60px;
    height: 60px;
    background: #25D366;
    color: white;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 32px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    z-index: 999;
    transition: 0.3s;
}
.whatsapp-float:hover {
    transform: scale(1.1);
}
</style>
```

---

## 🐛 Troubleshooting

### Form Not Sending Emails

1. **Check EmailJS Configuration**
   - Verify Service ID, Template ID, and Public Key
   - Ensure they're correctly pasted in `script.js`

2. **Check Browser Console**
   - Press F12 → Console tab
   - Look for error messages

3. **EmailJS Quota**
   - Free plan: 200 emails/month
   - Check your EmailJS dashboard for quota

4. **Email Provider**
   - Some providers block automated emails
   - Try a different email service in EmailJS

### Responsive Issues

1. **Clear Browser Cache**
   - Press Ctrl+Shift+Delete
   - Clear cached images and files

2. **Test on Real Devices**
   - Emulators may not show accurate results
   - Test on actual phones/tablets

### Slow Loading

1. **Optimize Images**
   - If you add images, compress them
   - Use WebP format for better performance

2. **Enable CDN**
   - Deploy on Netlify/Vercel for automatic CDN

---

## 📞 Contact Information

**Genomics Research & Diagnostics Centre**

- 👤 **Contact Person**: Akash Rana (Business Development Executive)
- 📱 **Mobile**: +91 8572851031
- 📧 **Email**: Info.genomicscentre@gmail.com
- 📍 **Address**: 97, Street No 8, Vasant Vihar, Karnal, Haryana 132001

---

## 📄 License

This website is proprietary software created for Genomics Research & Diagnostics Centre.
All rights reserved © 2025 Genomics Research & Diagnostics Centre.

---

## 🙏 Credits

- **Design & Development**: Custom built for medical diagnostics
- **Icons**: Font Awesome 6.4.0
- **Email Service**: EmailJS
- **Maps**: Google Maps

---

## 📝 Changelog

### Version 1.0.0 (December 2025)
- ✅ Initial release
- ✅ Full responsive design
- ✅ EmailJS integration
- ✅ Search and filter functionality
- ✅ Modal booking system
- ✅ Smooth animations
- ✅ Mobile-friendly navigation

---

## 🔮 Future Enhancements (Optional)

- [ ] Online payment integration
- [ ] User account system
- [ ] Test report download portal
- [ ] Real-time chat support
- [ ] Mobile app (React Native)
- [ ] Backend API (Node.js/PHP)
- [ ] Database integration
- [ ] SMS notifications
- [ ] Multi-language support

---

## 📚 Additional Resources

- [EmailJS Documentation](https://www.emailjs.com/docs/)
- [Netlify Documentation](https://docs.netlify.com/)
- [Vercel Documentation](https://vercel.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)

---

**Made with ❤️ for better healthcare**

🧬 Genomics Research & Diagnostics Centre
