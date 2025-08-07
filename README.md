# To-Do List Web Application

A full-featured task management system with user authentication and recycle bin functionality.

## Features

- ✅ User registration and login system
- 🔐 Secure session-based authentication
- 📝 Create, edit, and manage tasks
- 🗑️ Recycle bin with restore functionality
- 📅 Task due dates and status tracking
- 🎨 Responsive design light mode
- ✨ Modern UI with animated elements

## Project Structure

```
/todo-app
├── .htaccess            # URL rewrite rules
├── db.sql               # Database schema
├── index.php            # Main entry point
├── /assets
│   ├── /css             
│   │   └── style.css    # Main stylesheet
│   └── /js
│       └── script.js    # JavaScript functionality
├── /includes
│   ├── auth.php         # Authentication functions
│   ├── config.php       # Configuration settings
│   ├── db.php           # Database connection
│   └── functions.php    # Helper functions
└── /pages
    ├── dashboard.php    # Main task interface
    ├── delete-task.php  # Task deletion handler
    ├── edit-task.php    # Task editing page
    ├── login.php        # Login page
    ├── recycle-bin.php  # Recycle bin management
    └── register.php     # User registration
```

## Installation Guide

### 1. Database Setup

Import the database schema:

```bash
mysql -u your_username -p todo_app < db.sql
```

### 2. Configuration

Edit `/includes/config.php`:

```php
// Set your base URL (e.g., http://localhost/todo-app)
define('BASE_URL', 'YOUR_BASE_URL_HERE');

// Enable error logging
define('ERROR_LOG_FILE', __DIR__ . '/../error.log');
```

Edit `/includes/db.php` with your database credentials:

```php
define('DB_HOST', 'localhost');
define('DB_USER', 'your_db_username');
define('DB_PASS', 'your_db_password');
define('DB_NAME', 'todo_app');
```

### 3. Server Requirements

- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache/Nginx with mod_rewrite enabled

## Usage

1. Access the application in your browser
2. Register a new account or login
3. Manage your tasks:
   - Add new tasks with optional due dates
   - Mark tasks as complete/pending
   - Edit or delete tasks
   - Restore deleted tasks from recycle bin

## Troubleshooting

- Check `/error.log` for any system errors
- Ensure the database connection details are correct
- Verify mod_rewrite is enabled on your server
- Make sure all file permissions are set correctly

## Security Notes

For production environments:
1. Implement CSRF protection
2. Set up proper file permissions
3. Use HTTPS
4. Consider rate limiting for authentication endpoints

## License

MIT License

## Credits

Developed by Striker
https://discord.gg/uU3vw7t32c
