# LMS  Report

## Date: 18/01/2025

### Start Time: 8:53 AM



---

## Doctypes Created and Role Permissions:
1. **Article**
2. **Library Transaction**
3. **Library Membership**
4. **Library Member**
5. **Library Settings**

---

## Actions Taken:

1. **Article Doctype**:
   - Filled the form in the form view of the "Article" doctype, creating one record.
   - Confirmed that a database table named `tabarticle` was created with the specified fields by checking the MariaDB console.
   - Completed doctype features and permissions following the documentation.

2. **Library Member Doctype**:
   - Created the "Library Member" doctype and added one library member following the documentation.
   - Implemented code for automatically computing the full name from the first and last names.

---

## Python Controller Code:

The following code was written for `library_member.py`:

```python
# library_member.py
import frappe
from frappe.model.document import Document

class LibraryMember(Document):
    # this method will run every time a document is saved
    def before_save(self):
        self.full_name = f'{self.first_name} {self.last_name or ""}'
```

---

## Key Notes:

- The `before_save` method is executed every time a document is saved.
- It is one of many hooks provided by the `Document` class.

Learn more about hooks from the [Controller documentation](https://frappeframework.com/docs/user/en/python-api/hooks).

---

## Error Encountered:

- **Error**: Server Error - ImportError: Library member.

**How I Solved It**:
- Identified that the issue was due to using a capital letter in the class name in `library.member.py`. Since the doctype name is "Library Member," I changed the class name to match the doctype.

---

## Issue with "Status" Field:

- The "Status" field for books was not shown initially.

**Cause**:
- Added options "Available" and "Issue" together without proper formatting.

**Solution**:
1. Updated the options to include one option per line.
2. When it still did not work, deleted the "Status" field and added it again, which resolved the issue.

---

## LMS Website Screenshots:


1.  
   ![image](https://github.com/user-attachments/assets/faa300ea-1962-40f7-8f41-84f7e4f5a4e0)


2. 
    ![image](https://github.com/user-attachments/assets/9e195dd9-69cf-4363-9735-488c3b23c98a)
)

---

## Summary:

- Successfully created and tested multiple doctypes.
- Implemented logic in the `library_member.py` file for dynamically computing the full name.
- Resolved issues with the "Status" field and capitalization error in Python class names.
