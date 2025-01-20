<h1>Library management system</h1>

This app is developing in debian version 12.9
So,i am going to develop the LMS(Library management system)
using frappe 
First of all lets create an app:
open terminal(ctrl+alt+t)
Run this command under frappe-bench directory

<br>

``` bash
$ bench new-app library_management
```
we have made our app successfully
Now we are going to create our site.
Run this command under frappe-bench directory
for this we will run this command

```bash
$ bench  new-site library.localhost
```

Now ,we have created our site successfully
So now we will open the browser and can do further process
but before going to browser we have to tell our operating system that library.localhost should point to localhost.
So to do this we need to add this entry to /etc/hosts file
127.0.0.1 library.localhost
this will map library.localhost to localhost.This command is used for this

```bash
bench --site library.localhost add-to-tests
```

this will ask for root password and will add entry to your /etc/hosts file
After that i am able to access site at http://library.localhost:8000

<br>
Now install app on site
Run this command under frappe-bench directory
<br>

```bash 
 $ bench --site library.localhost library_management
 ```
 <br>
 To check whether the app is installed or not we can  run this command

``` bash
$ bench --site library.localhost list-apps
```
<br>
This will show our app(library_management) and frappe(default)
<br>

### let's setup desk of application
First of all create the all doctypes that needed
#### Create article doctype

-  Step1: search for doctype list in search bar

<br>

- Step 2:click on button +add doctype

<br>

- Step 3:File module with library management system and doctype name is article.

<br>

- Step 4: Save

<br>

- Step 5:Go to fields

<br>

We can add any number of fields in this doctype with roles and permissions whatever we want to create and give to someone else
<br>

Once we have creatd article doctype database with name tabarticle was created and we can check it from mariadb console

```bash
bench --site library.localhost mariadb
```
It will show the table with all columns 
# Similarly i have created other doctypes as well like,

Library member,library transactions,Library Membership,LibrarySettings
<br>
Now we can adjust each doctype with permissions ,roles and restrictions we want to add in this our all doctypes will be created completely and made necessary changes in the files according to documentation.
<br>
After doing all these steps we have now to render our pages for website vistiors and these pages are called 

**Portal Pages**

Basically we are workig with desk which is the admin interface accessible by System Users,but if we want to give limited access to our customers as in our case we want library members to be able to view available articles that they can issue from our website for this we will use protal pages which will helps us to achieve this.Follow this steps to achieve it
Go to Article doctype, and scroll down to the Web View section.

## steps:-
  - Enable Has Web View and Allow Guest to View
 - Enter articles in the Route field
  - Add a field named Route in the fields table
  - Click on Save
  
  <br>

  After these steps we have now enabled the web view for article doctype.This means that we can now view details of an article on our website without logging into desk.
  After doing this we have to customize our web view template
  <br>
   The default web view that is created is very basic and just serves as a starting point for us to customize and improve it."
When we made article web view two files were created namely:-

- article.html and
- article_row.html
After this we have to style our pages as frappe use bootstrap 4 by default for its web views and for styling our page we have to  do necessary addition or chnages to article.html file.
<br>
After we can go to any article and click on see on website and
if we have fill the all fields of the article we wish to see ,
 it will show page according to our amendments in the article.html file .It will show only the article we want to see ,but if we want to have complete list of articles on page and whatever we want to read the details or decription by clicking on it then we want to make necessary changes in the article_row.html file .It will show page with list of all articles and can read according to our choice.

<br>

This is all about the Library management system that i have learned and elaborate here
<br>

# Image
![lms](https://github.com/user-attachments/assets/9e195dd9-69cf-4363-9735-488c3b23c98a))
