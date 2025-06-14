# pla-ng - a phpLiteAdmin fork (aka phpLiteAdmin 2)

## What is pla-ng?

phpLiteAdmin development is stalling: pla-ng is a fork of this well known tool 
which integrates recent updates and small patches.

pla-ng is not a rewrite of phpLiteAdmin, nor will never be. Consider pla-ng just 
an "updated version of phpLiteAdmin", usable on PHP >= 8.0 without much troubles.


## What is phpLiteAdmin?

phpLiteAdmin is a web-based SQLite database admin tool written in PHP with
support for SQLite3 and SQLite2. Following in the spirit of the flat-file system
used by SQLite, phpLiteAdmin consists of a single source file, phpliteadmin.php,
that is dropped into a directory on a server and then visited in a browser.
There is no installation required. The available operations, feature set,
interface, and user experience is comparable to that of phpMyAdmin.

Official Website of the original version: https://www.phpliteadmin.org/

phpLiteAdmin 2 Github: https://github.com/emanueleg/pla-ng/

## News

**12.06.2025: pla-ng 2.0.2 released [Download now](https://github.com/emanueleg/pla-ng/releases/tag/v2.0.2)**

**27.01.2024: pla-ng 2.0.1 released**

**19.01.2024: pla-ng 2.0.0 released**

**05.09.2019: phpLiteAdmin 1.9.8.2 released [Download now](https://www.phpliteadmin.org/download/)**

## Features

-   Lightweight - consists of a single 250KB source file for portability
-   Supports SQLite3 and SQLite2 databases
-   Translated and available in [15 languages](https://github.com/emanueleg/pla-ng/wiki/Localization) - and counting
-   Specify and manage an unlimited number of databases
-   Specify a directory and optionally its subdirectories to scan for databases
-   Create and delete databases
-   Add, delete, rename, empty, and drop tables
-   Browse, add, edit, and delete records
-   Add, delete, and edit table columns
-   Manage table indexes
-   Manage table triggers
-   Import and export tables, structure, indexes, and data (SQL, CSV)
-   View data as bar, pie, and line charts
-   Graphical search tool to find records based on specified field values
-   Create and run your own custom SQL queries in the free-form query editor/builder
-   Easily apply core SQLite functions to column values using the GUI
-   Write your own PHP functions to be available to apply to column values
-   Design your own theme using CSS or install a pre-made [theme from the community](https://github.com/emanueleg/pla-ng/wiki/Themes)
-   All presented in an intuitive, easy-to-use GUI that allows non-technical, SQL-illiterate users to fully manage databases 
-   Allows multiple installations on the same server, each with a different password
-   Secure password-protected interface with login screen and cookies


## Demo

A live demo of the original phpLiteAdmin can be found here:
https://demo.phpliteadmin.org/


## Requirements

-   a server with PHP >= 5.2.4 installed
-   at least one PHP SQLite library extension installed and enabled: PDO,
    SQLite3, or SQLiteDatabase
    
PHP version 5.3.0 and greater usually comes with the SQLite3 extension installed
and enabled by default so no custom action is necessary.


## Download

The files in the source repositories are meant for development, not for use in production.

You can find the latest downloads here:
https://github.com/emanueleg/pla-ng/releases

## Installation

See instructions at https://github.com/emanueleg/pla-ng/wiki/Installation

## Configuration

**NEW** as of 1.9.4: You can now configure phpLiteAdmin in an external file. If
you want to do this:

-   rename `phpliteadmin.config.sample.php` into `phpliteadmin.config.php`
-   do not change the settings in `phpliteadmin.php` but in
    `phpliteadmin.config.php`

See https://github.com/emanueleg/pla-ng/wiki/Configuration for details.

1.   Open `phpliteadmin.config.php` (or `phpliteadmin.php` before 1.9.4) in
     a text editor.
	
2.   If you want to have a directory scanned for your databases instead of
     listing them manually, specify the directory as the value of the 
     `$directory` variable and skip to step 4. 
	
3.   If you want to specify your databases manually, set the value of the
     `$directory` variable as false and modify the `$databases` array to
     hold the databases you would like to manage.
	
    -   The path field is the file path of the database relative to where
        `phpliteadmin.php` will be located on the server. For example, if
        `phpliteadmin.php` is located at "databases/manager/phpliteadmin.php" and
        you want to manage "databases/yourdatabase.sqlite", the path value
        would be "../yourdatabase.sqlite".
		
    -   The name field is the human-friendly way of referencing the database
        within the application. It can be anything you want.

4.   Modify the `$password` variable to be the password used for gaining access
     to the phpLiteAdmin tool.
	
5.   If you want to have multiple installations of phpLiteAdmin on the same
     server, change the `$cookie_name` variable to be unique for each installation
     (optional).

6.   Save and upload `phpliteadmin.php` to your web server.
	
7.   Open a web browser and navigate to the uploaded `phpliteadmin.php` file. You
     will be prompted to enter a password. Use the same password you set in step 4.
     
## Code Repository and pull requests

The code repository is available both on github:

Github: https://github.com/emanueleg/pla-ng

You are welcome to fork the project and send us pull requests on any of these
platforms.


## Installing a theme
	
1.   Download the themes package from the [original phpLiteAdmin Download page](https://www.phpliteadmin.org/download/).
	
2.   Unzip the file and choose your desired theme.
	
3.   Upload `phpliteadmin.css` from the theme's directory alongside
     `phpliteadmin.php`.
	
4.   Your theme will automatically override the default.


## Getting help

The project's wiki provides information on how to do certain things and is
located at https://github.com/emanueleg/pla-ng/wiki/Home .


## Reporting errors and bugs

If you find any issues while using the tool, please report them at
https://github.com/emanueleg/pla-ng/issues .

## License

This program is free software: you can redistribute it and/or modify
it under the terms of the **GNU General Public License** as published by
the Free Software Foundation, either **version 3** of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <[https://www.gnu.org/licenses/](https://www.gnu.org/licenses/)>.
