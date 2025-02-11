
## Weather App Hosting Guide

### Account Creation

1. Go to [InfinityFree](https://www.infinityfree.com/).
2. Click on the **Register** button.

   [![Register button](images/register.png)](images/register.png)
3. Fill in your email address, password, and agree to the terms of service.

   [![Sign Up form](images/signup_form.png)](images/signup_form.png)
4. Click on the **Sign Up** button.
5. Verify your email address by clicking on the link sent to your email.

### Domain Setup

1. Log in to your InfinityFree account.
2. Click on the **Create Account** button.

   [![Create Account button](images/create_account.png)](images/create_account.png)
3. Choose the option which costs $0.

   [![Free option](images/free_option.png)](images/free_option.png)
4. Enter the Subdomain name, choose domain extension and Check Availability.

   [![Subdomain setup](images/subdomain_setup.png)](images/subdomain_setup.png)
5. Choose **I approve** below the Email Consent and click Create Account.

   [![Email Consent approval](images/email_consent.png)](images/email_consent.png)
6. Once the nameservers are updated, click on the **Create Account** button.
7. Wait for the account to be created and your domain to be set up.

---

## Setting Up the Website using CPanel

### Uploading Files

1. Click on the File Manager.

   [![File Manager](images/dashboard.png)](images/dashboard.png)
2. Open **htdocs** folder, delete any files present and upload your 4 files (HTML, CSS, JS and PHP).

   [![Upload files](images/upload.png)](images/upload_files.png)

### Creating a database for our domain

1. Navigate to the database tab in the Cpanel and click on the **MySQL Databases**

   [![Database tab](images/database.png)](images/database.png)

2. Create a database by any name (E.g. WeatherData) and click on create database

   [![Create database](images/create-db.png)](images/create-db.png)

3. Now, the database is finally created.

4. Note down the MySQL DB name somewhere safe (E.g. Notepad).

   [![Database name](images/dbname.png)](images/dbname.png)


### Saving required credentials

1. Navigate back to the Cpanel (mentioned above)

2. On the right side of Cpanel you be able to see account details section

3. Copy all the required credentials and save somewhere like Notepad.
   - MySQL Hostname
   - MySQL Username

   [![Credentials](images/credentials.png)](images/credentials.png)

4. You will need password too, for that navigate back to this website [Dashboard](https://dash.infinityfree.com/accounts/)

   [![Password](images/password.png)](images/password.png)

   **Copy the password too.**

### Changing Credentials inside connection.php

1. Put the saved MySQL hostname in servername (or hostname) variable

   [![Servername](images/servername.png)](images/servername.png)

2. Put the MySQL username in the username variable

   [![Username](images/username.png)](images/username.png)

3. Likewise put the saved password in the password variable.

4. Comment out the createDB query (if exists)

   [![Create DB query](images/create-db-query.png)](images/create-db-query.png)

5. Put your previously saved database name in the select_db query

   [![Select DB query](images/select-db-query.png)](images/select-db-query.png)

6. Save the changes

### Changing path in JavaScript

Previously, we had hosted the weather app locally on your device and on JavaScript we had used the **localhost/connection.php** path to fetch data but since we are hosting the website on a server so we have to change the path now.

1. Open your JavaScript file.

2. Navigate to this line of code

   [![Fetch code](images/fetch.png)](images/fetch.png)

3. Remove the localhost part and only leave **/connection.php?q={city}** part.

   [![Fetch fix](images/fetchfix.png)](images/fetchfix.png)

4. Save the file

---

If you feel any trouble, contact us on [Discord](https://dsc.gg/devsphere).
