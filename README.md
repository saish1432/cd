# CAR DECORE - Complete E-commerce Website

## 🚗 Project Overview
CAR DECORE is a comprehensive car accessories e-commerce website built with PHP, HTML5, CSS3, JavaScript, and MySQL. It features a responsive design, animated elements, WhatsApp integration, and a powerful admin panel.

## 📁 Folder Structure
```
car-decore/
├── index.php                 # Main website homepage
├── config/
│   └── database.php          # Database configuration
├── assets/
│   ├── css/
│   │   ├── style.css         # Main website styles
│   │   └── admin.css         # Admin panel styles
│   └── js/
│       └── script.js         # Main website JavaScript
├── admin/
│   ├── index.php             # Admin dashboard
│   ├── login.php             # Admin login page
│   ├── logout.php            # Admin logout
│   ├── products.php          # Product management
│   ├── categories.php        # Category management
│   └── orders.php            # Order management
├── api/
│   └── record_order.php      # Order recording API
├── uploads/                  # File upload directory
│   ├── videos/               # Video uploads
│   └── thumbnails/           # Video thumbnails
├── database.sql              # Database structure
└── README.md                 # This file
```

## 🛠️ Installation Instructions

### Step 1: Database Setup
1. Open phpMyAdmin on your hosting panel (Hostinger/cPanel)
2. Create a new database named `car_decore`
3. Import the `database.sql` file to create all tables and sample data

### Step 2: Database Configuration
1. Open `config/database.php`
2. Update the database credentials:
   ```php
   $host = 'localhost';        # Your database host
   $dbname = 'car_decore';     # Your database name
   $username = 'your_username'; # Your database username
   $password = 'your_password'; # Your database password
   ```

### Step 3: Upload Files
1. Upload all files to your hosting directory (public_html or htdocs)
2. Ensure proper file permissions (755 for directories, 644 for files)
3. Create `uploads/videos/` and `uploads/thumbnails/` directories with write permissions

### Step 4: WhatsApp Configuration
1. Open `assets/js/script.js`
2. Find the WhatsApp number (currently set to `1234567890`)
3. Replace with your actual WhatsApp number (include country code)
4. Update in multiple places:
   - `inquireProduct()` function
   - `buyNow()` function
   - `confirmPurchase()` function

## 🔐 Admin Panel Access

### Default Login Credentials
- **Username:** `admin`
- **Password:** `password`
- **Bypass Login:** You can also login with just username (check the bypass option)

### Admin Panel Features
- **Dashboard:** Sales analytics, visitor tracking, revenue charts
- **Products:** Add/Edit/Delete products with images and pricing
- **Categories:** Manage car brand categories
- **Orders:** View and manage WhatsApp orders
- **Videos:** Upload product demo videos (max 5MB each)
- **Analytics:** Sales reports and visitor statistics

### Admin Panel URL
Access at: `yourwebsite.com/admin/`

## 📱 Website Features

### Frontend Features
1. **Animated Header** with company branding
2. **Auto-scrolling Banner** with product images
3. **Product Catalog** with zoom effects and cart functionality
4. **WhatsApp Integration** for orders and inquiries
5. **Category Management** with brand logos
6. **Video Demos** section with play controls
7. **Visitor Counter** tracking mobile/tablet/desktop users
8. **Responsive Design** for all devices

### Backend Features
1. **Order Tracking** - All WhatsApp orders are automatically recorded
2. **Sales Analytics** - Daily/weekly/monthly reports with charts
3. **Product Management** - Full CRUD operations
4. **Video Management** - Upload videos up to 5MB
5. **Visitor Analytics** - Track website visits by device type

## 🔧 Customization Guide

### Changing Company Information
1. **Company Name & Tagline:** Edit in `index.php` header section
2. **Office Address:** Update in footer section of `index.php`
3. **Contact Information:** Modify in database settings table

### Adding Products
1. Login to admin panel
2. Go to Products section
3. Click "Add Product"
4. Fill in product details, images (use Pexels URLs), and pricing
5. Set product tags (Hot, New, Most Selling)

### Managing Categories
1. Access Categories in admin panel
2. Add/Edit car brand categories
3. Upload brand logos (use image URLs)
4. Categories automatically appear on homepage

### Video Management
1. Go to Videos section in admin
2. Upload videos (supports .MP4, .MOV, .WMV, .AVI, .MKV, .FLV, .MPEG)
3. Maximum file size: 5MB per video
4. Videos automatically display on homepage

## 📊 Order Tracking System

### How Orders Are Recorded
1. When customer clicks "Confirm to Buy" or "Buy Now"
2. Order details are sent to WhatsApp
3. Simultaneously, order is recorded in database with:
   - Product names and quantities
   - Total amount
   - Order date and time
   - Customer information (if available)

### Viewing Orders
1. Login to admin panel
2. Go to Orders section
3. View all orders with status tracking
4. Update order status (Pending/Completed/Cancelled)
5. Delete orders if needed

## 🎨 Design Customization

### Color Scheme
Update CSS variables in `assets/css/style.css`:
```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #e74c3c;
    --accent-color: #f39c12;
    /* Modify these colors as needed */
}
```

### Animations
- All animations are CSS-based for better performance
- Modify animation timings in the CSS file
- Add new animations using CSS keyframes

## 🔒 Security Features

### Admin Security
- MD5 password hashing (can be upgraded to bcrypt)
- Session management
- SQL injection protection with prepared statements
- XSS protection with htmlspecialchars

### File Upload Security
- File type validation for videos
- File size limits (5MB for videos)
- Secure file naming and storage

## 📱 Mobile Optimization

### Responsive Features
- Mobile-first design approach
- Touch-friendly interface
- Optimized images for different screen sizes
- Mobile-specific cart and product views

### Performance
- Lazy loading for images
- Compressed CSS and JavaScript
- Optimized database queries
- CDN integration for external libraries

## 🐛 Troubleshooting

### Common Issues

1. **Database Connection Error**
   - Check database credentials in `config/database.php`
   - Ensure database exists and is accessible

2. **Images Not Loading**
   - Verify image URLs are accessible
   - Check file permissions
   - Ensure uploads directory exists

3. **Admin Login Not Working**
   - Verify admin_users table exists
   - Check default credentials
   - Clear browser cache

4. **WhatsApp Links Not Working**
   - Update WhatsApp number in JavaScript files
   - Ensure proper number format (+countrycode + number)

5. **Orders Not Recording**
   - Check `api/record_order.php` file permissions
   - Verify database connection
   - Check browser console for JavaScript errors

### File Permissions
Set these permissions on your server:
- Directories: 755
- PHP files: 644
- uploads/ directory: 755 (with write permissions)

## 🔄 Updates and Maintenance

### Regular Maintenance
1. **Database Backup:** Regular backups of the database
2. **File Backup:** Backup all website files
3. **Security Updates:** Keep PHP and MySQL updated
4. **Performance Monitoring:** Monitor website speed and uptime

### Adding New Features
1. Follow the existing code structure
2. Update database schema if needed
3. Test all functionality before deployment
4. Update documentation

## 📞 Support

### Getting Help
1. Check this README file first
2. Verify database and file permissions
3. Check error logs in your hosting panel
4. Test with sample data provided

### Development Notes
- Built with vanilla PHP (no frameworks)
- Uses modern CSS Grid and Flexbox
- ES6 JavaScript features
- MySQL with prepared statements
- Mobile-first responsive design

---

**© 2025 CAR DECORE. All Rights Reserved.**
**Developed & Managed by GTAi.in**

This website is ready for production use on any shared hosting provider like Hostinger, cPanel, or similar platforms. All components are optimized for performance and security.