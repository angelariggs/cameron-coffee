#Setting Up Your Drupal Environment

##Downloading MAMP
1. Download [MAMP](https://www.mamp.info/en/downloads/)

##Starting Your Servers
1. In your computer's file directory, go to Applications/MAMP, and launch MAMP.app.
2. Click 'Start Servers'
	- You'll see the indicators for Apache Server and MySQL Server light up.

##Database Setup with MAMP
1. Go to [localhost 8888](http://localhost:8888/MAMP/) in your browser, or click on 'Open WebStart Page' in the MAMP application.
2. Under the "Tools" menu, select "phpMyAdmin".
3. Click the "Databases" tab.
4. Enter a name for the database.
5. Select "utf8_general_ci" under the "Collation" drop-down.
6. Click the "Create" button.
7. Click on the name of the new database we just created.
8. Select "Privileges" tab.
9. Click "Add user". (Drupal will use the username and password to access the database, so that it can automatically store all of your content and configuration).
10. Enter a username into the "User name" field.
11. In the "Host" field, select "Local".
12. Enter a password and retype it. Leave the "Password generate" field blank.
13. Under the "Database for User" section, select only "Grant all privileges on database - yourdatabasename".
14. Click the "Go" button in the lower right.

##Drupal Core Setup
1. Download the [Drupal Core](https://www.drupal.org/download) folder, then rename the folder for your project.
2. You should never delete or modify these core folders.
3. In terminal, `cd` to your project directory, and run these two commands:
	- `cp sites/default/default.settings.php sites/default/settings.php`
		- This copies the file `default.settings.php` into a new file, `settings.php`
	- `chmod -R a+w sites/default`
		- This gives you admin permissons for the `defaults` folder
4. When you run Drupal, it will save configuration settings inside `settings.php`
5. During installation, Drupal will write your log-in info and other site settings into this file. Then it will change the permissions back to read-only, so that nobody can delete or modify it. 

##Installing Drupal
1. Open your MAMP application, and click 'Preferences', then click the 'Web Server' tab.
2. Set your document route folder to point at the project directory (e.g. Sites/cameron-coffee/cameron-site).
3. Point your browser to [localhost:8888](http://localhost:8888/).
4. Select the standard install, then click 'Save and Continue'.
5. Select English as the language, then click 'Save and Continue'.
6. Under 'Database Type', select the radio button for 'MySQL, MariaDB, or equivalent'.
7. Type in the name of your database that you set earlier.
8. Then enter the username and password that you created in the MyPHPAdmin.


