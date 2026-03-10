# 📰 NewsPortal — PHP & MySQL News Portal

A full-featured, modern news portal built with **PHP**, **MySQL**, **jQuery**, and **vanilla CSS**. Includes an admin panel, AI tools, user authentication, social login, and much more.

<img width="1920" height="1080" alt="Screenshot 2026-03-10 110325" src="https://github.com/user-attachments/assets/3650ff2b-50ec-4709-a018-f8b9dabad3c1" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110343" src="https://github.com/user-attachments/assets/de616a3d-2b31-43e4-b4d5-d8b4f23b7ee0" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110354" src="https://github.com/user-attachments/assets/39af20ac-749f-4581-9875-9f5fc44ea802" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110401" src="https://github.com/user-attachments/assets/f3aa023f-005a-4d22-abfc-f8c87cde2dca" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110412" src="https://github.com/user-attachments/assets/02eefbd5-35c1-44ab-868d-bd1781f51384" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110420" src="https://github.com/user-attachments/assets/59d240ff-1851-4d4a-a541-407b5165a90d" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110441" src="https://github.com/user-attachments/assets/c7cfef57-ebfc-44b3-9e2f-e6bacb5dd8b9" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110500" src="https://github.com/user-attachments/assets/ebc56b7e-408f-47df-b10b-2df24af17773" />
<img width="1920" height="1080" alt="Screenshot 2026-03-10 110449" src="https://github.com/user-attachments/assets/340e4505-94ba-429b-ba6d-3a538e43b331" />


---

## 🚀 Features

### 🌐 Frontend
- Responsive design with mobile hamburger menu
- Breaking news ticker
- Category & subcategory navigation with dropdowns
- Post detail page with reading progress bar
- Search with live suggestions (AJAX)
- Dark mode toggle (persists via localStorage)
- Google Translate integration (18+ languages)
- Back to top button

### 🤖 AI Tools (Free — No API Key)
- **AI Article Summarizer** — extractive summarization
- **Sentiment Analyzer** — positive/negative/neutral tone detection with progress bar
- **AI Related News** — smart keyword-based article matching
- **AI Chatbot Assistant** — floating chatbot that searches your news database

### 👤 User System
- User registration & login
- Social login — Google, Facebook, Twitter/X (OAuth 2.0)
- User profile page with:
  - Edit profile (name, email)
  - Change password with strength meter
  - My activity (comment history)
- Session-based authentication

### 🔔 Notifications
- Live notification bell for logged-in users
- Read/unread tracking per user
- Admin can create notifications by type (Breaking, Info, Success, Warning)

### 📊 Sidebar Widgets
- **Weather Widget** — real-time weather via Open-Meteo API (PHP server-side, free)
- **Poll / Voting System** — with IP-based duplicate vote prevention
- **Newsletter Subscription** — with subscriber management
- **Social Media Follow** buttons
- **Popular Posts** ranked by views
- **Popular Tags** cloud

### 🛠️ Admin Panel
- Dashboard with stats (posts, views, comments, categories)
- Post management (add, edit, delete, trash)
- Category & subcategory management
- Comment moderation (approve, reject, delete)
- **Manage Users** — activate/deactivate/delete registered users
- **Newsletter Subscribers** — view, filter, manage subscribers
- **Notifications** — create and manage site notifications
- Sub-admin management
- Page management (About, Contact)
- Profile settings

---

## 📁 Project Structure

```
newsportal/
│
├── index.php                   # Homepage
├── post.php                    # Single post page (with AI toolbar)
├── category.php                # Category listing
├── subcategory.php             # Subcategory listing
├── search.php                  # Search results
├── search-suggest.php          # AJAX search suggestions
├── page.php                    # Static pages (About, Contact)
├── user-login.php              # Login & Register
├── user-logout.php             # Logout
├── user-profile.php            # User profile
├── social-login.php            # Social OAuth redirect
├── social-callback.php         # Social OAuth callback
├── poll-vote.php               # Poll voting AJAX
├── newsletter-subscribe.php    # Newsletter subscription AJAX
├── mark-notification.php       # Mark notification as read
│
├── includes/
│   ├── config.php              # DB config, session, helper functions
│   ├── header.php              # Site header, nav, dark mode, translator
│   ├── footer.php              # Footer, chatbot, AI scripts
│   ├── sidebar.php             # Weather, poll, newsletter, social widgets
│   ├── ai-features.php         # AI summarizer, sentiment, related, chatbot
│   └── social-config.php       # Social login API keys
│
├── assets/
│   ├── css/
│   │   ├── style.css           # Main stylesheet + dark mode
│   │   └── ai-features.css     # AI toolbar & chatbot styles
│   └── js/
│       ├── main.js             # Core JS (search, comments, scroll)
│       └── ai-features.js      # AI features JavaScript
│
├── uploads/
│   └── news/                   # Uploaded post images
│
├── admin/
│   ├── login.php
│   ├── dashboard.php
│   ├── posts.php
│   ├── post-add.php
│   ├── post-edit.php
│   ├── categories.php
│   ├── subcategories.php
│   ├── comments.php
│   ├── users.php               # Manage registered users
│   ├── newsletter.php          # Manage newsletter subscribers
│   ├── notifications.php       # Manage notifications
│   ├── pages.php
│   ├── subadmins.php
│   ├── profile.php
│   └── includes/
│       ├── auth.php
│       ├── header.php          # Admin sidebar & nav
│       └── footer.php
│
└── database.sql                # Complete database with sample data
```

---

## ⚙️ Installation

### Requirements
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache (XAMPP recommended for local)
- Composer (for social login only)

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/newsportal.git
cd newsportal
```

**2. Import the database**
- Open **phpMyAdmin**
- Create a new database named `newsportal`
- Click **Import** and select `database.sql`
- Click **Go**

**3. Configure the project**

Open `includes/config.php` and update:

```php
define('DB_HOST',   'localhost');
define('DB_USER',   'root');
define('DB_PASS',   '');
define('DB_NAME',   'newsportal');        // your database name
define('SITE_URL',  'http://localhost/newsportal');
define('ADMIN_URL', 'http://localhost/newsportal/admin');
```

**4. Set upload permissions**

Make sure the uploads folder is writable:
```bash
chmod 755 uploads/news/
```
On Windows (XAMPP) this is automatic.

**5. Visit the site**
```
http://localhost/newsportal/
```

**6. Login to Admin Panel**
```
URL:      http://localhost/newsportal/admin/
Email:    admin@news.com
Password: password
```

---

## 🌦️ Weather Widget Setup

The weather widget uses the free **Open-Meteo API** (no API key needed).

To set your city, open `includes/sidebar.php` and update:

```php
$weatherCity = 'Mumbai';    // Your city name
$weatherLat  = 19.0760;    // Your city latitude
$weatherLon  = 72.8777;    // Your city longitude
```

Find coordinates at: **https://www.latlong.net**

Also make sure your `php.ini` has:
```ini
allow_url_fopen = On
extension=openssl
```

---

## 🔐 Social Login Setup (Optional)

Install dependencies:
```bash
composer require league/oauth2-google league/oauth2-facebook happyr/twitter-oauth2
```

Add your API keys to `includes/social-config.php`:

```php
define('GOOGLE_CLIENT_ID',     'your-google-client-id');
define('GOOGLE_CLIENT_SECRET', 'your-google-client-secret');

define('FACEBOOK_APP_ID',      'your-facebook-app-id');
define('FACEBOOK_APP_SECRET',  'your-facebook-app-secret');

define('TWITTER_CLIENT_ID',     'your-twitter-client-id');
define('TWITTER_CLIENT_SECRET', 'your-twitter-client-secret');
```

### OAuth Redirect URIs to register:
| Provider | Redirect URI |
|----------|-------------|
| Google   | `https://yourdomain.com/social-callback.php?provider=google` |
| Facebook | `https://yourdomain.com/social-callback.php?provider=facebook` |
| Twitter  | `https://yourdomain.com/social-callback.php?provider=twitter` |

---

## 🗄️ Database Tables

| Table | Description |
|-------|-------------|
| `admins` | Admin panel users |
| `categories` | News categories |
| `subcategories` | News subcategories |
| `posts` | News articles |
| `comments` | Post comments |
| `pages` | Static pages (About, Contact) |
| `users` | Registered frontend users |
| `notifications` | Site notifications |
| `user_notifications` | Read/unread tracking per user |
| `polls` | Poll questions |
| `poll_options` | Poll answer options |
| `poll_votes` | Vote tracking (IP-based) |
| `newsletter` | Newsletter subscribers |

---

## 🎨 Customization

### Change Site Name & Colors
- **Site name:** `includes/config.php` → `SITE_NAME`
- **Primary color:** `assets/css/style.css` → `:root { --primary: #c0392b; }`
- **Logo:** `includes/header.php` → site-logo section

### Add Social Media Links
Open `includes/sidebar.php` → Follow Us section and replace `href="#"` with your real URLs:

```php
<a href="https://facebook.com/YourPage">Facebook</a>
<a href="https://twitter.com/YourHandle">Twitter</a>
<a href="https://instagram.com/YourProfile">Instagram</a>
<a href="https://youtube.com/@YourChannel">YouTube</a>
<a href="https://wa.me/91XXXXXXXXXX">WhatsApp</a>
```

### Change Weather City
```php
$weatherCity = 'Nashik';
$weatherLat  = 19.9975;
$weatherLon  = 73.7898;
```

---

## 🚀 Deploying to Live Server

1. Upload all files via **FTP** (FileZilla) or **cPanel File Manager**
2. Import `database.sql` via **phpMyAdmin**
3. Update `includes/config.php`:
```php
define('DB_HOST',  'localhost');
define('DB_USER',  'your_db_user');
define('DB_PASS',  'your_db_password');
define('DB_NAME',  'your_db_name');
define('SITE_URL', 'https://yourdomain.com');
```
4. Update social login redirect URIs to use your live domain

---

## 📦 Tech Stack

| Technology | Usage |
|------------|-------|
| PHP 7.4+   | Backend logic |
| MySQL 5.7+ | Database |
| HTML5/CSS3 | Frontend markup & styling |
| jQuery 3.x | AJAX, DOM manipulation |
| Font Awesome 6 | Icons |
| Open-Meteo API | Free weather data |
| Google Translate | Multi-language support |
| League OAuth2 | Social login |

---

## 🔧 .gitignore

Create a `.gitignore` file in your project root:

```gitignore
# Dependencies
vendor/

# Uploaded files
uploads/news/*
!uploads/news/.gitkeep

# Config with sensitive data
includes/social-config.php

# OS files
.DS_Store
Thumbs.db

# IDE files
.vscode/
.idea/
*.sublime-project
*.sublime-workspace

# PHP error logs
error_log
*.log
```

---

## 📤 Upload to GitHub

```bash
# 1. Initialize git in your project folder
cd C:\xampp\htdocs\newsportal
git init

# 2. Add all files
git add .

# 3. First commit
git commit -m "Initial commit: NewsPortal PHP & MySQL"

# 4. Create repo on GitHub then add remote
git remote add origin https://github.com/YOUR_USERNAME/newsportal.git

# 5. Push
git branch -M main
git push -u origin main
```

---

## 🙏 Credits

- [Font Awesome](https://fontawesome.com) — Icons
- [Open-Meteo](https://open-meteo.com) — Free weather API
- [Google Translate](https://translate.google.com) — Translation widget
- [League OAuth2](https://oauth2-client.thephpleague.com) — Social login

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 📸 Screenshots

> Add screenshots of your portal here after uploading to GitHub.
> Go to your repo → Edit README → drag and drop images.

---

<p align="center">
  Made with ❤️ using PHP & MySQL
</p>
