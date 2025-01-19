# Report: Library Management System Setup

**Date:** 17/01/2025  
**Task:** Library Management System Setup  
**Time Frame:** 2:00 PM to 6:30 PM  

---

### **2:00 PM - 3:00 PM: Create an App**

1. **Objective:** To create the custom app for the library management system.
   
2. **Steps Taken:**
   - Opened the terminal and navigated to the `frappe-bench` directory.
   - Ran the following command to create a new app:
     ```bash
     $ bench new-app library_management
     ```
   - Entered the details for the app:
     - **App Title:** Library Management
     - **App Description:** This is a library management system app for managing library books.
     - **App Publisher:** Manvir Singh
     - **App Email:** manvirsingh6656@gmail.com
     - **App License:** Provided 'N', which caused an error since only valid licenses are allowed. 
     - **GitHub Workflow action for unittests:** 'N' (declined creating workflow action).
   
3. **Outcome:**
   - The app `library_management` was successfully created and located at `/home/abc12/frappe-bench/apps/library_management`.

4. **Duration:** 1 hour

---

### **3:00 PM - 4:30 PM: Create a Site**

1. **Objective:** To create a new site where the app will be installed.

2. **Steps Taken:**
   - Ran the following command to create the new site:
     ```bash
     $ bench new-site library.localhost
     ```
   - Entered the MySQL root password when prompted.
   - Encountered a warning about MariaDB version compatibility with Frappe (`MariaDB version ['10.11', '6']`), but the installation proceeded.
   - Set the Administrator password and completed the installation.
   - The site was successfully created with the message: "THE SITE HAS BEEN CREATED SUCCESSFULLY."
   
3. **Next Step:**
   - To make `library.localhost` accessible, added an entry to the `/etc/hosts` file with the following command:
     ```bash
     $ bench --site library.localhost add-to-hosts
     ```
     - This added the line `127.0.0.1 library.localhost` to the `/etc/hosts` file.

4. **Outcome:**
   - The site `library.localhost` was successfully created and pointed to `localhost`.

5. **Duration:** 1.5 hours

---

### **4:30 PM - 6:20 PM: Install the App on the Site**

1. **Objective:** To install the newly created app `library_management` on the `library.localhost` site.

2. **Steps Taken:**
   - Ran the following command to install the app on the site:
     ```bash
     $ bench --site library.localhost install-app library_management
     ```
   - Confirmed the app installation by running the command:
     ```bash
     $ bench --site library.localhost list-apps
     ```
     - The output showed:
       ```
       frappe
       library_management
       ```
   - Successfully logged into the site and completed the setup wizard.

3. **Outcome:**
   - The app `library_management` was successfully installed on the site, and the setup wizard completed successfully.

4. **Duration:** 1.5 hours

---

### **6:20 PM - 6:30 PM: Frappe Site Issue**

1. **Issue:** Encountered the "Unable to connect" error when attempting to refresh the page on the browser (Firefox).

2. **Steps Taken:**
   - Checked the server and confirmed it was running.
   - Cleared the browser cache and reloaded the page.
   - The Frappe site opened successfully in the browser after clearing the cache.

3. **Outcome:**
   - The site was successfully opened in the browser after clearing the cache.

4. **Duration:** 10 minutes

---

### **6:30 PM: Create Doctype**

1. **Objective:** To create a new DocType for the Library Management System.

2. **Steps Taken:**
   - Searched for **DocType** in the search bar within the Frappe interface.
   - Created a new module titled **Library Management System** and a DocType titled **Article**.

3. **Outcome:**
   - The DocType **Article** was successfully created under the **Library Management System** module.

---

### **Summary of Time Log**

- **2:00 PM - 3:00 PM:** Created the custom app `library_management`.
- **3:00 PM - 4:30 PM:** Created the site `library.localhost` and set it to point to localhost.
- **4:30 PM - 6:20 PM:** Installed the `library_management` app on the site and completed the setup wizard.
- **6:20 PM - 6:30 PM:** Resolved the "Unable to connect" error by clearing the cache and accessing the site successfully.
- **6:30 PM:** Created a new DocType titled **Article** under the **Library Management System** module.

---

**Task Completed Successfully!**
