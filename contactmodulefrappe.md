# Contacts Module of Frappe with Its DocTypes Description

## Overview
The Contacts Module in Frappe contains several DocTypes to handle contact-related data. These DocTypes include:

- Contact
- Address
- Salutation
- Gender
- Address Template
- Contact Phone
- Contact Email

In this document, I will explore each of these DocTypes in detail, explaining what they are, how they work, and which roles can perform certain actions.

---

## 1. Contact DocType
The **Contact** DocType is used to store contact information, such as names and details of a person or entity.

### Key Fields and Features:
- **Is Submittable**: Restricts submission unless all required fields are filled.
- **Single**: Restricts the Contact DocType to only have one record with a name.
- **Fields**:
  - Contact Name(s): This is where you enter the names of the contact.
- **Permissions**: You can set the role **"All"** with permissions to only **read** other users' contact names.

---

## 2. Address DocType
The **Address** DocType stores addresses for contacts. It can be used to manage multiple addresses like home and office.

### Key Fields:
- **Address** (Label: Data): The address field to store the full address.
- **Address Type** (Select): Options like "home", "office", etc.
- **Address Line** (Label: Data, Mandatory): The street address.
- **City** (Label: Data): The city for the address.
  
---

## 3. Salutation DocType
The **Salutation** DocType is used to store different salutations for contacts.

### Key Fields:
- **Salutation** (Label: Select):
  - Options include: Mr., Mrs., Ms., Dr., Prof., or any other salutation.

---

## 4. Gender DocType
The **Gender** DocType stores gender information for contacts.

### Key Fields:
- **Gender** (Label: Data):
  - Fieldname: gender
  - This field is typically used for gender identification (e.g., Male, Female, Other).
- **Permissions**:
  - The role **"ALL"** has permission to **read** the gender field.

---

## 5. Address Template DocType
The **Address Template** DocType is used to store templates for addresses that can be reused for multiple contacts.

### Key Fields:
- **Country** (Label: Data, Fieldname: country)
- **Is Default** (Check): A checkbox to set the template as default.
- **Template** (Label: Code):
  - Options: home, office, or any other custom options.

---

## 6. Contact Phone DocType
The **Contact Phone** DocType stores phone numbers associated with contacts.

### Key Fields:
- **Phone No** (Label: Data, Fieldname: phone_no, Mandatory): The phone number for the contact.
- **Is Primary Phone** (Label: Check):
  - A checkbox to mark the phone number as the primary contact number.

---

## 7. Contact Email DocType
The **Contact Email** DocType stores email addresses for contacts.

### Key Fields:
- **Email Address** (Label: Data, Mandatory): The email address for the contact.
- **Is Primary** (Label: Check): A checkbox to mark the email as primary.
  
### Features:
- **Is Child Table**: Used to allow adding multiple email addresses for a contact.
- **Is Editable Grid**: Allows users to interact with and edit email entries directly within the form.

---

This document provides a comprehensive overview of the **Contacts** module's DocTypes, explaining their key fields and features. 

