# 🎓 php-student-admin

A **PHP MVC web application** for managing students and sections in an academic administration context. Built from scratch with a custom MVC architecture and a PDO-based database layer — no external framework. Features user authentication, student/section CRUD, search, and a dashboard interface.


---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Contributing](#contributing)

---

## Overview

**php-student-admin** is a full-stack web application built in pure PHP following the **MVC (Model-View-Controller)** design pattern. It allows administrators to log in and manage **students** and **sections** — adding, modifying, deleting, searching, and listing records — through a clean, role-protected interface.

---

## Features

- 🔐 **Authentication** — Login (`seconnecter.php`) and logout (`deconnexion.php`) with session-based access control via `login-verification.php`
- 👨‍🎓 **Student Management** — Add, modify, delete, search, and view student details
- 🗂️ **Section Management** — Add, modify, and delete academic sections
- 📋 **Listings** — View full list of students (`show-students-list.php`) and sections (`show-sections-list.php`)
- 🔍 **Student Search** — Search students by criteria (`search-student.php`)
- 📊 **Dashboard** — Central platform view (`platform.php`) after login
- 🗄️ **PDO Database Layer** — Database connectivity through `connexionPdo.php`
- 🔄 **Custom Autoloader** — Class autoloading across `model/` and `controller/` without Composer

---

## Tech Stack

| Component | Technology |
|---|---|
| Language | PHP |
| Architecture | Custom MVC (no framework) |
| Database Access | PDO (PHP Data Objects) |
| Views | PHP + HTML templates (`vue/` directory) |
| Frontend | HTML, CSS, JavaScript |
| Deployment | Vercel |

---


---

## Getting Started

### Prerequisites

- PHP 7.4+
- A local web server: [XAMPP](https://www.apachefriends.org/), [WAMP](https://www.wampserver.com/), or [Laragon](https://laragon.org/)
- MySQL

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MohamedAliHG/php-student-admin.git
   cd php-student-admin
   ```

2. **Move to your web server root:**
   ```bash
   # XAMPP example
   cp -r php-student-admin /xampp/htdocs/
   ```

3. **Set up the database** (see [Configuration](#configuration))

4. **Open in your browser:**
   ```
   http://localhost/php-student-admin/
   ```
   You will be automatically redirected to the login page.

---

## Configuration

Update the PDO connection settings in `model/connexionPdo.php`:

```php
$host = 'localhost';
$dbname = 'student_admin';
$username = 'root';
$password = '';

$pdo = new PDO("mysql:host=$host;dbname=$dbname;charset=utf8", $username, $password);
```

Create the MySQL database:

```sql
CREATE DATABASE student_admin;
```

---

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## Author

**Mohamed Ali HG** — [@MohamedAliHG](https://github.com/MohamedAliHG)

---

*Built with 🐘 PHP — custom MVC architecture with PDO, no framework.*
