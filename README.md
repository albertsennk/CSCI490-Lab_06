# CSCI490-Lab_5

Android comes standard with an SQLite relational database, however working with the common libraries surrounding this can be quite cumbersome with lots of boilerplate code to write. Android developers are currently working on an improved API and abstraction layer that makes sending data in and out of the SQLite database "easy". 

## Problem
This lab will have you create a database, an entity class to represent our data, a dao to transport the data to and from the database, related AsyncTask classes to perform the database operations, and simple layout/activities to interact with our data layer. Databases usually will have more than one table, but the database will only contain one table to simplify the learning process. The database will contain a **Person** table with only one field **name**. We will write names to the database and retrieve all the names. This will require one **Dao** with two SQL statements. One **insert** and one **query

## Purpose
This lab will create a practical application of the Android Room Database theory covered in class.

# Jargon
First, it helps to cover some of the database jargon that might be covered.
  * **Database** - A collection of related tables
  * **Table** - Related data held in a structured format
  * **Entity** - An object in our system that we want to store in a Table
  * **Dao** - Data Access Object. The object that transports the data to/from database

## Steps
### Add dependencies:
* Add the following dependencies in the app:gradle file:
```
implementation "android.arch.persistence.room:runtime:1.0.0"
annotationProcessor "android.arch.persistence.room:compiler:1.0.0"
```

### Create package structure:
Create packages to organize your classes. There are several methods of organization. Some developers prefer to organize by feature while others group by the architecture. The choice is yours, but by architecture is a simple way. 
* entities, data, asyncs (one possibility)

### Create the classes
In the appropriate packages create the following:
## Create the Entity class
  * Create **Person.java** and mark it with the **@Entity** annotation. Add the following attributes and make appropriate getters/setters
  ```
   @PrimaryKey(autoGenerate = true)
   private int id;

   private String name;
```   
## 
    
```xml
<ListView
    ...
    android:dividerHeight="5.0sp"
    android:divider="@android:color/black"
    android:padding="45sp">
</ListView>
```
* Test your code one final time.
* Share, commit, and push lab to your GitHub account
