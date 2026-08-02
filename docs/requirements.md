# Requirements

 - The purpose of this page is to describe the functional and business requirements of the TechStore ecommerce system.
 - This document contains the main rules, validations and expected behaviors for each feature.


## Sign up
    
### Description    
 - The system must allow users to create an account by providing their personal information.

### Business rules
 - The registration form must contain the following fields: 
    - Fullname, Age, identification number, Username, Email, cellphone and Password.
 - Password requirements: 
    - Minimum of 8 characters.
    - At least one uppercase letter.
    - At least one lowercase letter.
    - At least one number.
 - Username, identification number and email must be unique
 - Cellphone and email must have valid formats
 - all fields are mandatory
 - The system must display an error message when a field contains invalid information.
 - Users must not be able to complete registrations if the information is invalid

### Data Requirements 
 - User 
    - ID
    - fullname
    - age
    - identification number
    - username
    - email
    - cellphone
    - password

## Login

### Description    
 - The system must allow users to authenticate by providing their username or email and password

### Business rules
 - The login form must have the following fields:
    - user (username or email)
    - password
 - Username/email and password fields must be mandatory
 - The system must display an error message when a field contains invalid information.
 - Users must not be able to authenticate with invalid credentials
 - After successful authentication, the user must be redirect to the home page

### Data Requirements 
 - User 

## Logout

### Description    
- The system must allow authenticated users to log out of the platform.

### Business Rules

- Authenticated users must be able to log out at any time.
- After a successful logout, the user must be redirected to the home page.
- After logout, the user must no longer have access to authenticated pages without logging in again.
- The user session must be terminated.

### Data Requirements 
 - User 

## Password Recovery
### Description    
- The system must allow users to recover their password.

### Business Rules

- Both authenticated and unauthenticated users must be able to access the password recovery process.
- Users must provide a valid email address associated with an existing account.
- The system must send a verification code or recovery link to the registered email address.
- Users must enter the valid verification code before they are allowed to create a new password.
- Only registered users can recover their password.
- The system must display an error message if the provided email address does not exist or is invalid.
- The new password must meet the password policy requirements:
   - Minimum of 8 characters.
   - At least one uppercase letter.
   - At least one lowercase letter.
   - At least one number.

### Data Requirements 
 - User 

## My Account
### Description    
- The "My account" page displays the user's personal information and provides quick access to account management features.

### Business Rules
- Only authenticated users must be able to access "My account" page
- The page must display only the authenticated user's information.
- Users must not be able to view another user's account information.
- If an unauthenticated user attemps to access "My account" page, they must be redirect to the home page
- The "My account" page must display the following information:
   - First name
   - Last name
   - E-mail
   - Default address
   - Lastest order
- The page must provide quick access to:
   - Address Management
   - Order History
   - Edit Personal Information
   - Change Password

### Data Requirements 
   User model

## Address management
### Description
- The Address Management page allows users to view, create, edit and delete their registered addresses.

### Business Rules
- Only authenticated users must be able to access "Address management" page
- Users must be able to define a default address.
- Users must only be able to access their own addresses
- The system must allow users to register new addresses
- The system must allow users to edit any previously registered address
- The system must allow users to delete any previously registered address
- The page must display every registered address with the following information:
   - Postcode
   - Street
   - Number
   - City
   - State
   - Phone Number
   - Recipient Name
   - button or link to edit the address
   - button or link to delete the address
- The page must provide a link or button to add a new address

### Data Requirements
   - Address
      - ID
      - User ID (Foreign Key -> User.ID)
      - Postcode
      - Street
      - Number
      - City
      - State
      - Phone Number
      - Recipient Name

### Add address
#### Description
- The system must allow users to add a new address 

#### Business Rules
- The user can access address registration page by clicking the add address link available on in Address management page or by clicking the add address link available on in the address part of the checkout process
- Only authenticated users must be able to access address registration page
- All required fields must be validated before saving the address
- The user must provide the following information:
   - Postcode
   - Street
   - Number
   - City
   - State
   - Phone Number
   - Recipient Name

### Edit address
#### Description
- The system must allow users to edit an address 

#### Business Rules
- The user can edit any address by clicking the edit address link available on in "Address management page" or by clicking the edit address link available on in the address part of the checkout process
- Only authenticated users must be able to edit an address
- Users must only be able to edit their own addresses.
- Users must edit only the address they select
- The user must be able to edit any of the following information:
   - Postcode
   - Street
   - Number
   - City
   - State
   - Phone Number
   - Recipient Name

### Delete address
#### Description
- The system must allow users to delete an address 

#### Business Rules
- The user can delete any address by clicking the delete address link available on in Address management page or by clicking the delete address link available on in the address part of the checkout process
- Only authenticated users must be able to delete an address
- Users must delete only their own addresses
- Users must delete only the address they select
- When the user clicks the Delete button, the system must display a confirmation modal
- The confirmation modal must have the following information:
   - Title: Do you really want to delete this address?
   - Text: This action cannot be undone.
   - Button "Yes", clicking this button must permanently delete the selected address.
   - Button "No", The modal must be closed without deleting the address.
- If the user clicks the "Yes" button in the confirmation modal, the selected address must be permanently deleted and a toast message saying "Address successfully deleted." must be displayed.

## Home Page
### Description
### Business Rules
### Data Requirements

## Product Categories
### Description
### Business Rules
### Data Requirements

## Product Page
### Description
### Business Rules
### Data Requirements

## Search Page

## Add to cart

## Mini cart

## Cart

## Address

## Shipping/Delivery

## Payments

## Checkout process

## Order page

## Order history