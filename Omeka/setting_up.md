# Setting up Omeka
Technology required:
* XAMPP

## Setting up Omeka Locally
1. Download and unzip Omeka: https://omeka.org/classic/download/
1. Move the downloaded folder into htdocs under /Applications/XAMPP/xamppfiles/htdocs for Mac OS, and C:/XAMPP/xamppfiles/htdocs for Windows
  _Recommended: rename the file to something easy to remember/type_
1. Navigate to the localhost dashboard by typing "localhost" on your browser  
  _You may need to try "localhost/dashboard"_
1. Click on the "phpMyAdmin" tab
1. Click on the "Databases" tab
1. Create a database with a desired name
1. Click on the SQL tab
1. Making sure that the new database is selected, copy and paste in the following. Replace 'username' and 'password' to whatever username and password you want to use
  ![db](/images/db.png)
    ```SQL
    CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
    GRANT ALL PRIVILEGES ON * . * TO 'username'@'localhost';
    ```
1. Change permissions to the omeka installation
    ```shell
    chmod -R 767 path/to/omeka/installation
    ```
1. Find the db.ini folder located at the root directory of your omeka installation. Modify it to match your database setup.
    ```
    [database]
    host     = "localhost"
    username = "YourUserNameFromStep9"
    password = "YourPasswordFromStep9"
    dbname   = "YourDatabaseFromStep7"
    prefix   = "omeka_"
    charset  = "utf8"
    ;port     = ""
    ```
1. Navigate to your omeka instance on your browser by typing localhost/YourOmekaInstallation, and complete set up as prompted.

## Troubleshooting
* Zend_File_Transfer_Exception ‘The given destination is not writable’ error
  1. Create a directory "tmp" under the root directory of the Omeka installation.
  1. Add the following to application/config/config.ini
  ```
  storage.tempDir = "/tmp"
  ```
