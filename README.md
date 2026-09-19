# SoundPlus

SoundPlus is a web-based music streaming application built with PHP, MySQL, HTML, CSS, and JavaScript.

## Features

* User registration and login
* Music browsing and playback
* Songs, artists, albums, and genres
* Playlists
* Ratings
* Subscription plans
* User profiles
* Admin panel for managing application data

## Technologies Used

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** PHP
* **Database:** MySQL
* **Local Development:** XAMPP
* **Version Control:** Git and GitHub

## Project Structure

```text
soundplus/
│
├── admin/
│   ├── assets/
│   ├── css/
│   ├── images/
│   ├── includes/
│   ├── js/
│   ├── pages/
│   ├── public/
│   └── uploads/
│
├── bhakti songs/
├── song/
├── database/
│   └── soundplus.sql
│
├── .gitignore
└── README.md
```

## Requirements

Before running the project, install:

* XAMPP
* PHP
* MySQL / MariaDB
* A web browser
* Git (if cloning from GitHub)

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/DARSHANKUMAR113/SoundPlus.git
```

Then enter the project directory:

```bash
cd SoundPlus
```

### 2. Create the database

Open phpMyAdmin from XAMPP.

Create a database named:

```text
soundplus
```

Then import:

```text
database/soundplus.sql
```

> `database/soundplus.sql` contains the database structure only. It does not contain the original local users, passwords, songs, or other test data.

### 3. Configure the database connection

The actual database connection files are intentionally not included in the repository because they contain local database credentials.

Two example files are provided:

```text
admin/includes/admin_db_connect.example.php
admin/public/includes/db_connect.example.php
```

Copy them to the exact filenames expected by the application.

#### Admin database connection

Copy:

```text
admin/includes/admin_db_connect.example.php
```

to:

```text
admin/includes/admin_db_connect.php
```

#### Public database connection

Copy:

```text
admin/public/includes/db_connect.example.php
```

to:

```text
admin/public/includes/db_connect.php
```

Then open both new files and enter your own MySQL username and password.

Example:

```php
$servername = "localhost";
$username = "YOUR USERNAME";
$password = "YOUR PASSWORD";
$db = "soundplus";
```

Do not commit these files to GitHub.

They are already excluded through `.gitignore`.

## 4. Add Music Files

The repository does not include the project's MP3 files.

This is intentional because audio files can be large and may have copyright restrictions.

Add your own legally obtained audio files to the appropriate project location when setting up the application locally.

## 5. Run the Project

Start **Apache** and **MySQL** from XAMPP.

Then run the project using your preferred PHP development server.

If using the VS Code PHP Server setup used during development, make sure the server root points to the appropriate project directory.

For the admin section, the login page is located at:

```text
admin/pages/login.php
```

If the server root is already set to the `admin` directory, the login URL will be:

```text
http://localhost:3000/pages/login.php
```

The exact URL may differ depending on your local server configuration.

## Database Tables

The provided database structure contains these tables:

```text
admins
albums
artists
genre
plans
playlists
playlist_songs
ratings
songs
subscriptions
users
```

The schema file contains the table structures, indexes, and auto-increment definitions required by the application.

## Important Files Not Included in GitHub

For security and repository-size reasons, the following are intentionally excluded:

* Real database connection files
* Original local database dump containing data
* MP3/audio files
* Local uploaded profile pictures
* Temporary and local development files

The original local database dump is not included because it contains local/test data.

## Security

Never commit database usernames, passwords, API keys, or other secrets to GitHub.

Use the provided `.example.php` files as templates and keep your actual configuration files local.

## License

This project is provided for educational and development purposes.
