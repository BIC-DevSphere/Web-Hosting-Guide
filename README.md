## Setting Up the Website using CPanel

### Uploading Files

1. Open Cpanel as shown below

![alt text](images/cpanel.png)

2. Open File Manager and navigate inside the htdocs folder

![alt text](images/filemanager.png)

3. Uploads your codes here

![alt text](images/upload.png)

### Creating a database for our domain

1. Navigate to the database tab in the Cpanel and click on the **MySQL Databases**

![alt text](images/database.png)

2. Create a database by any name (E.g. WeatherData) and click on create database

![alt text](images/create-db.png)

3. Now, the database is finally created.

4. Note down the MySQL DB name somewhere safe (E.g. Notepad).

![alt text](images/dbname.png)

### Saving required credentials

1. Navigate back to the Cpanel (mentioned above)

2. On the right side of Cpanel you be able to see account details section

3. Copy all the requird credentials and save somewhere like Notepad. - MySQL Hostname - MySQL Username
   ![alt text](images/credentials.png)

4. You will need password too, for that navigate back to this website https://dash.infinityfree.com/accounts/

![alt text](images/password.png)
Copy the password too.

### Chaning Credentials inside connection.php

1. Put the saved MySQL hostname in servername (or hostname) variable
   ![alt text](images/servername.png)

2. Put the MySQL username in the username variable
   ![alt text](images/username.png)

3. Likewise put the saved password in the password variable.

4. Comment out the createDB query (if exists)

   ![alt text](images/create-db-query.png)
5. Put your previously saved database name in the select_db query

   ![alt text](images/select-db-query.png)

6. Save the changes

### Chaning path in JavaScript

Previously, we had hosted the weather app locally on your device and on JavaScript we had used the **localhost/connection.php** path to fetch data but since we are hosting the website on a server so we have to change the path now.

1. Open your JavaScript file.

2. Navigate to this line of code

   ![alt text](images/fetch.png)

3. Remove the localhost part and only leave **/connection.php?q={city}** part.

   ![alt text](images/fetchfix.png)

4. Save the file