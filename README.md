# News Portal - PHP & MySQL

A complete, fully dynamic News Portal web application built with PHP 7.x and MySQL.

---

## 📋 Project Information

| Item | Details |
|------|---------|
| **Language** | PHP 7.x+ |
| **Database** | MySQL 5.x+ |
| **Frontend** | HTML5, CSS3, jQuery, AJAX |
| **Admin Editor** | Summernote WYSIWYG |
| **Icons** | Font Awesome 6 |

---

## ⚙️ Installation Guide

### Requirements
- PHP 7.2 or higher
- MySQL 5.6 or higher
- Apache/Nginx web server
- XAMPP / WAMP / MAMP / LAMP

### Step 1: Setup Database
1. Open phpMyAdmin (http://localhost/phpmyadmin)
2. Create a new database named `newsportal`
3. Import the file `database.sql` into the database

### Step 2: Configure the Application
1. Open `/includes/config.php`
2. Update the database credentials:
   ```php
   define('DB_HOST', 'localhost');
   define('DB_USER', 'root');      // Your DB username
   define('DB_PASS', '');           // Your DB password
   define('DB_NAME', 'newsportal');
   define('SITE_URL', 'http://localhost/newsportal');
   define('ADMIN_URL', SITE_URL . '/admin');
   ```

### Step 3: Set File Permissions
Ensure the uploads folder is writable:
```bash
chmod 755 uploads/news/
```

### Step 4: Access the Application
- **Website:** http://localhost/newsportal/
- **Admin Panel:** http://localhost/newsportal/admin/

---

## 🔐 Admin Credentials

| Field | Value |
|-------|-------|
| Email | admin@news.com |
| Password | password |

> ⚠️ **Important:** Change the admin password immediately after first login!

---

## 📁 Project Structure

```
newsportal/
├── index.php               # Homepage
├── post.php                # Single post view
├── category.php            # Category listing
├── subcategory.php         # Subcategory listing
├── search.php              # Search results
├── page.php                # Static pages (About/Contact)
├── search-suggest.php      # AJAX search suggestions
├── database.sql            # Database schema + sample data
│
├── includes/
│   ├── config.php          # Configuration & helper functions
│   ├── header.php          # Site header template
│   ├── footer.php          # Site footer template
│   └── sidebar.php         # Sidebar widgets
│
├── assets/
│   ├── css/style.css       # Main stylesheet
│   └── js/main.js          # Main JavaScript
│
├── uploads/
│   └── news/               # Uploaded post images
│
└── admin/
    ├── index.php            # Admin redirect
    ├── login.php            # Admin login
    ├── logout.php           # Admin logout
    ├── dashboard.php        # Admin dashboard
    ├── posts.php            # Post management
    ├── post-add.php         # Add new post
    ├── post-edit.php        # Edit existing post
    ├── categories.php       # Category management
    ├── subcategories.php    # Subcategory management
    ├── comments.php         # Comment moderation
    ├── pages.php            # Static page management
    ├── subadmins.php        # Sub-admin management (Admin only)
    ├── profile.php          # Admin profile
    ├── get-subcats.php      # AJAX subcategory fetcher
    │
    ├── includes/
    │   ├── auth.php         # Authentication middleware
    │   ├── header.php       # Admin header template
    │   └── footer.php       # Admin footer template
    │
    └── assets/
        └── admin.css        # Admin panel stylesheet
```

---

## 🔧 Modules

### User Module (Public)
- Browse all news by category/subcategory
- Search for specific news articles
- Read full articles with related posts
- Leave comments on articles (pending moderation)
- Social sharing (Facebook, Twitter, WhatsApp)
- View About Us and Contact Us pages
- Breaking news ticker
- Reading progress bar

### Admin Module
- **Dashboard** - Statistics overview (posts, comments, views)
- **Posts** - Full CRUD with draft/publish, trash/restore, image upload
- **Categories** - Add/edit/delete/restore categories
- **Sub-Categories** - Manage subcategories with parent assignment
- **Comments** - Approve/reject/delete comment moderation
- **Pages** - Edit About Us and Contact Us content
- **Sub-Admins** - Create and manage sub-admin accounts
- **Profile** - Update own profile and change password

### Sub-Admin Module
- Same as Admin EXCEPT cannot create/manage other sub-admins
- Access to all content management features

---

## ✨ Features

- ✅ Fully responsive design
- ✅ WYSIWYG post editor (Summernote)
- ✅ Image upload for posts
- ✅ Breaking news ticker
- ✅ Search with AJAX suggestions
- ✅ Comment system with moderation
- ✅ Post view counter
- ✅ Tag system
- ✅ Related posts
- ✅ Social sharing buttons
- ✅ Reading progress bar
- ✅ Bulk comment actions
- ✅ Trash/restore for posts and categories
- ✅ Password hashing (bcrypt)
- ✅ SQL injection protection
- ✅ XSS protection
- ✅ Role-based access control

---

## 🛡️ Security Features

- Passwords stored as bcrypt hashes
- All user input sanitized against SQL injection
- HTML special characters escaped to prevent XSS
- Session-based authentication
- Role-based access control (Admin vs Sub-Admin)
- File upload validation (type and size)

---

## 📞 Support

For any issues, check that:
1. Database credentials in `includes/config.php` are correct
2. The `uploads/news/` folder is writable
3. PHP version is 7.2+
4. MySQL version is 5.6+

  <img width="1920" height="1020" alt="Screenshot 2026-02-27 135859" src="https://github.com/user-attachments/assets/457bc775-ccfb-4a1a-8bd9-fa840b9c7c88" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 135932" src="https://github.com/user-attachments/assets/7abdaccc-8071-46e0-8e72-8c78e727f8bd" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 135944" src="https://github.com/user-attachments/assets/373544d7-aa69-4360-9fa9-b117025a56df" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140003" src="https://github.com/user-attachments/assets/c57d029b-23ef-4463-9aaf-63860ff6dc72" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140011" src="https://github.com/user-attachments/assets/f21ec43c-b053-40e8-8f4c-c338bd6aeb9a" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140023" src="https://github.com/user-attachments/assets/acb4ccb0-b7db-41a6-a75c-5a7b04df9dbb" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140034" src="https://github.com/user-attachments/assets/6ed9be9f-f56d-4ac9-827f-eaf925a62734" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140054" src="https://github.com/user-attachments/assets/01085df4-75bb-465c-aa32-75c340ab9652" />
  <img width="1920" height="1080" alt="Screenshot 2026-02-27 140102" src="https://github.com/user-attachments/assets/2611b3e5-7774-4f38-bd0f-95208383f7ea" />
