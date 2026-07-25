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

### Models
 - User 
    - 

## Logout

## Password Recovery

## My Account

## Home Page

## Product Categories

## Product Page

## Search Page

## Add to cart

## Mini cart

## Cart

## Address

## Shipping/Delivery

## Payments

## Checkout proccess

## Order page

## Order history