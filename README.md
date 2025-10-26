# My Blog System (PHP + MySQL)

## 👤 Author
**Name:** WSLR Perera  
**Index No:** 235084E  
**Course:** Web Programming (IN2120)  
**Lecturer:** Ms. Premadasa M.G.N.N.  
**Degree Program:** Information Technology and Management  
**Faculty:** Faculty of Information Technology  

---

## 📝 Project Description
A complete **Blog Management System** using **PHP + MySQL**, featuring authentication, CRUD blogs, comments, likes, profile pictures, and dark/light themes.

### ✨ Features
- Secure Register / Login / Logout  
- "Remember Me" persistent login (using cookies)  
- Email verification (✅ PHPMailer ready)  
- Profile view & update + profile picture upload  
- Create / Edit / Delete own blog posts  
- Nested comments and likes  
- Search posts by keyword  
- Responsive design with dark & light modes  
- Full input validation + prepared SQL statements  

---

## 🧱 Technologies Used
| Layer | Tools |
|-------|-------|
| **Frontend** | HTML · CSS · JavaScript |
| **Backend** | PHP (Procedural) |
| **Database** | MySQL (XAMPP) |
| **Mailer** | PHPMailer (via Composer) |
| **Server** | Apache |

---

## 🗂️ Folder Structure

my_blog/
      ├── assets/
      │ └── css/style.css
      ├── blog/
      │ ├── create.php
      │ ├── edit.php
      │ ├── delete.php
      │ └── view.php
      ├── includes/
      │ └── config.php
      ├── uploads/
      │ └── profile_pics/
      ├── vendor/ # PHPMailer via Composer
      ├── index.php
      ├── login.php
      ├── register.php
      ├── logout.php
      ├── profile.php
      ├── change_password.php
      ├── forgot_password.php
      ├── verify.php
      └── README.md

---

## ⚙️ How to Run

1. **Install XAMPP** → [apachefriends.org](https://www.apachefriends.org)  

2. **Copy Project** → `C:\xampp\htdocs\my_blog`  

3. **Start Apache & MySQL** 

4. **Create Database**
   ```sql
   CREATE DATABASE blog_app;
   USE blog_app;

5. **add .env file**
   DB_HOST=localhost

   DB_USER=root
   DB_PASS=
   DB_NAME=blog_app
   MAIL_HOST=smtp.gmail.com
   MAIL_PORT=587
   MAIL_USER=your@gmail.com
   MAIL_PASS=app-password
   MAIL_FROM=your@gmail.com
   MAIL_FROM_NAME="MyBlogSpace"
   APP_URL=http://localhost/my_blog

6. **Access the App**  
   Open browser → [http://localhost/my_blog](http://localhost/my_blog)

---

## 🔒 Security Features
   -PHP sessions + cookies for authentication
   -Hashed passwords (using password_hash())
   -HTTPS-ready session cookies
   -Strict SQL prepared statements
---
## 🍪 Remember Me (Persistent Login)

When a user selects “Remember Me” during login, the system securely stores a random remember_token in both:

a browser cookie (for 7 days)

the database (in the user table)

On each visit, if the user’s session is expired but a valid cookie exists, the system automatically logs them back in by matching the token with the database record.

Security measures:

The token is a random 32-character hex string generated with random_bytes().

Cookies are set with the HttpOnly flag, so JavaScript can’t access them.

Tokens can be invalidated anytime by logging out (cookie + DB entry cleared).

This ensures a balance between convenience and security for returning users.
---

## 🌈 Theme
- **Light & Dark modes** supported  
- Color palette:  
  - Blue (Primary)  
  - Green (Accent)  
  - Black/Dark Background for dark mode  

---

## 💡 Future Enhancements
   - Email notifications for new comments

   -Blog image uploads

   -User roles (Admin/Editor)

   -API integration for mobile clients
---

## 🏁 Conclusion
🏁 Conclusion

MyBlogSpace demonstrates how to build a secure, stylish, responsive CRUD application with login, cookies, and email verification — a solid foundation for any modern PHP project.

## 🎯 IMPROVEMENTS MADE:

1. **Fixed code block formatting** - Added proper markdown code fences
2. **Corrected folder structure** - Proper indentation and formatting
3. **Fixed .env example** - Proper code block with language highlighting
4. **Improved readability** - Better spacing and structure
5. **Removed duplicate section** - Eliminated the extra "---" line
