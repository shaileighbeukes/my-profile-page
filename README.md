# My Profile Page

A professional personal profile dashboard built with HTML, CSS, JavaScript, and PHP. Perfect for a 3rd year Information Systems student project.

## Features

✅ **Responsive Design** - Works on desktop, tablet, and mobile  
✅ **Profile Management** - Edit personal information  
✅ **Reports Dashboard** - View and manage submitted reports  
✅ **Account Settings** - Change password, notification settings  
✅ **Modern UI** - Clean and professional interface  
✅ **Simple PHP Backend** - Easy to understand code  

## Project Structure

```
my-profile-page/
├── index.html              # Main profile page
├── all_reports.html        # All reports page
├── styles.css              # CSS styling
├── script.js               # JavaScript functionality
├── get_profile.php         # Fetch profile data
├── get_reports.php         # Fetch reports data
├── update_profile.php      # Update profile data
├── logout.php              # Handle logout
└── README.md               # This file
```

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/shaileighbeukes/my-profile-page.git
cd my-profile-page
```

### 2. Local Development (Using PHP Built-in Server)
```bash
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

### 3. Using Apache/Nginx
Copy all files to your web server's public directory and access through your browser.

## File Descriptions

### HTML Files
- **index.html** - Main profile dashboard with personal info, reports, and settings
- **all_reports.html** - Full page view of all submitted reports

### CSS
- **styles.css** - All styling for responsive design, cards, modals, and animations

### JavaScript
- **script.js** - Handles interactivity: modals, data loading, form submissions, notifications

### PHP Backend
- **get_profile.php** - Returns user profile data as JSON
- **get_reports.php** - Returns user reports as JSON
- **update_profile.php** - Handles profile updates (receives JSON)
- **logout.php** - Handles user logout and session destruction

## Key Features Explained

### Edit Profile Modal
Click "Edit Profile" button to open a modal where you can update:
- Full name
- Email address
- Phone number
- Ward
- Address

### Reports Dashboard
- View total, pending, and resolved reports
- See recent reports with status badges
- Click "View all reports" to see complete list

### Account Settings
- Change password
- Notification settings
- Logout

## Database Integration (For Future Enhancement)

The PHP files currently use simulated data. To connect to a database:

1. Create a database connection file:
```php
<?php
$connection = mysqli_connect('localhost', 'username', 'password', 'database_name');
if (!$connection) {
    die('Connection failed: ' . mysqli_connect_error());
}
?>
```

2. Update `get_profile.php` to query the database:
```php
$query = "SELECT * FROM users WHERE id = " . $_SESSION['user_id'];
$result = mysqli_query($connection, $query);
$profile = mysqli_fetch_assoc($result);
```

## Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Flexbox, Grid, Animations
- **JavaScript (ES6)** - DOM manipulation, Fetch API
- **PHP 7+** - Backend processing, JSON responses

## Responsive Breakpoints

- **Desktop**: Full layout with 2-column grid
- **Tablet** (768px): Adjusts spacing and font sizes
- **Mobile** (<768px): Single column layout, optimized touch targets

## Learning Outcomes

This project demonstrates:
- Frontend form handling and validation
- Backend data processing with PHP
- Async communication using Fetch API
- DOM manipulation with vanilla JavaScript
- CSS modern layouts (Flexbox, Grid)
- Responsive web design principles
- RESTful API concepts

## Future Enhancements

- [ ] Database integration (MySQL/PostgreSQL)
- [ ] User authentication and login system
- [ ] Password hashing (bcrypt)
- [ ] File upload for profile pictures
- [ ] Form validation (client & server-side)
- [ ] Email notifications
- [ ] Search and filter reports
- [ ] Data pagination

## Tips for Learning

1. **Start with HTML** - Understand the structure of the page
2. **Study CSS** - See how styling creates the professional look
3. **Learn JavaScript** - Focus on DOM manipulation and Fetch API
4. **Understand PHP** - See how backend processes data
5. **Practice modifications** - Try adding new features!

## Troubleshooting

### PHP files not executing
- Ensure PHP is installed: `php -v`
- Use `php -S localhost:8000` to run built-in server
- Check file permissions

### Fetch API not working
- Check browser console (F12) for errors
- Ensure PHP files return valid JSON
- Verify file paths in fetch() calls

### Styling not applied
- Clear browser cache (Ctrl+Shift+Delete)
- Check if styles.css is in the same directory
- Verify CSS file path in HTML

## License

This project is open source and available for educational purposes.

## Author

Shaileigh Beukes - 3rd Year Information Systems Student

---

**Happy Coding!** 🚀
