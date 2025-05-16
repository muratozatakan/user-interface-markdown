# User Interface Specification for User Management

This document is about user management screen. It includes **Requirements**, **UI Components**, **Interactions**, **Errors** and **Page at the Beggining** sections. Software developers use this document as a guide during the development of this user interface.

## Requirements

Admins of the user management system can:

- View filtered table format for all users.
- Filter to hide disabled user.
- Add new users to the system.
- View information about users such as username, display name, phone, email, user roles.
- Enable or disable user.

## Layout of the Main Page

- **User List Table**: Sortable and filterable table for viewing users.
- **New User Form**: Form to add new user or edit existing user's details.

## UI Components

### 1. User List Section

#### New User Button

- Type: Button
- Label: **+ New User**
- Position: Top left
- Color: White text on blue background
- Behavior: Clicking it brings up the **New User Form** for creating a new user.

#### Hide Disabled Users Checkbox

- Type: Checkbox
- Position: Next to the **New User Button**.
- Behavior: Filters the user list when checked to filter out users with the **Enabled** status set to false.

#### User List Table

All columns of the table should be sortable and filterable.
Each row represents a user.

- **Columns**
  - **ID**: Unique ID for each user.
  - **User Name**: Username of the user.
  - **Email**: User's email address.
  - **Enabled**: Displays true or false to show the status of the account.

---

### 2. New User Form

Displayed when clicking **New User Button**.

When creating a new user, the title is **New User**, when editing an existing user, the title is user's **User Name**.

#### Form Fields

- **Username**
  - Type: Text
  - Position: First field in the form
  - Required: Yes
- **Display Name**
  - Type: Text
  - Position: Second field in the form
  - Required: Yes
- **Phone**
  - Type: Text
  - Position: Third field in the form
  - Required: Optional
- **Email**
  - Type: Text
  - Position: Fourth field in the form
  - Required: Yes
- **User Roles**
  - Type: Dropdown
  - Options: Guest, Admin, SuperAdmin
  - Default: No selection
  - Behavior: Clicking opens dropdown menu
  - Required: Yes
  - Position: Fifth field in the form
- **Enabled**
  - Type: Checkbox
  - Default: Unchecked
  - Behavior: User is active when checked.
  - Position: Last field in the form

#### Save User Button

- Type: Button
- Color: White text on blue background
- Behavior: When this button is clicked, it saves the user with the information entered in the **New User Form**.
- Position: Top right

## Interecations

### Filtering the Table

The table can be sorted and filtered by **ID**, **User Name**, **Email**, **Enabled** properties.

### Creating a New User

1. Admins click the **+ New User** button.
2. The **New User Form** pops up.
3. Admins fill the information about user.
4. Admins click **Save User Button**.
5. If required information filled system saves the user and shows the success message. If not an **error message** displays.

### Editing an Existing User

1. Admins click one of the row from **User List**.
2. Form filled with information about user pops up.
3. Admins make changes about user's information.
4. Admins click **Save User Button**.
5. If required information filled system saves the changes about user and shows the success message. If not an **error message** displays.

## Errors

If the required information is not filled in, the system displays an error on the screen and indicates which information needs to be filled in.

It does not save the new user or allow changes to be made to the existing user unless this information is filled in.

## Page at the Beggining

- When the page loads the **User List Table** displays **all users**.
- **Hide Disabled Users Checkbox** should be checked.
- **User List Table** should sort all users by their IDs in ascending order.
