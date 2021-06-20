# Starting Omeka Sandbox mode - tips
Technology required:
* XAMPP (version 5.6.3 or above)

## Setting up Omeka Locally
1. Run XAMPP
	>>> for PC, it is under C drive

--------------------
MySQL ISSUE(Windows only):
--------------------
a. Navigate to XAMPP/mysql/data
b. delete (everytime) ib_logfile0, ib_logfile1, ibdata1
--------------------

2. Start "Apache" and "MySQL"

3. You are ready to go (localhost/"nameOfSite"/admin)
	>>> Example: http://localhost/gscholars_sandbox/admin/
	>>> "nameOfSite" can be found from 'db.ini'

4. localhost/phpmyadmin --> access the database info

5. to change your database --> db.ini (inside of your website folder)

6. /theme --> editing them is also documented
