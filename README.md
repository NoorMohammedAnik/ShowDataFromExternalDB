# ShowDataFromExternalDB

This projects explains the usage of an Android library which is helpful to import and use external SQLite database into your Android application. It has been a problem for Android developers to release an application with some existing rows of data in the database. For example if you are developing a static application which is used to display some tourist spots in your country, probably you need to release the database with predefined details about the tourist places inside it. However, there are no native ways to import external database easily into your Android application.
 
 The Android SQLiteAssetHelper library allows you to build your SQLite database in your desktop computer, and to import and use it in your Android application. Let's create a simple application to demonstrate the application of this library.
 
# Step 1:
Create a database quotes.db using your favorite SQLite database application (DB Browser for SQLite is a portable cross platform freeware, which can be used to create and edit SQLite databases). Create a table 'quotes' with a single column 'quote'. Insert some random quotes into the table 'quotes'.
http://sqlitebrowser.org/

# Step 2:
The database can be imported into project either directly as it is, or as a compressed file. The compressed file is recommended, if your database is too large in size. You can create either a ZIP compression or a GZ compression.

The file name of the compressed db file must be quotes.db.zip, if you are using ZIP compression or quotes.db.gz, if you are using GZ compression.

# Step 3:
Create a new application or project in Android Studio

# Step 4:
Open the build.gradle (Module: app) file and add the following dependency.
dependencies {
    implementation 'com.readystatesoftware.sqliteasset:sqliteassethelper:+'
}

Once you have saved the build.gradle file click on the 'Sync Now' link to update the project. You can synchronize the build.gradle, by right clicking on the build.gradle file and selecting "Synchronize build.gradle' option as well.

# Step 5:
Right click on the app folder and create new assets folder.

# Step 6:
Create a new folder 'databases' inside the assets folder.

# Step 7:
Copy and paste the  quotes.db.zip file inside the assets/databases folder.

# Step 8:
Finaly your external sqlite database in assets/databases folder. Than follow the codes of this project.

