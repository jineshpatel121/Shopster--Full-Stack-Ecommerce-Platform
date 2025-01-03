# Shopster

## Overview

Shopster is a Spring-based web application emulating an e-commerce website offering user authentication, product listing and selling, cart functionality, and payment integration using Stripe. It is designed to provide a streamlined user experience for buying and selling products online.

---

## Features

### User Authentication
- Custom login page for user authentication.
- Signup functionality with validation to prevent duplicate emails.
- Profile management with session-based authentication.

### Product Management
- Browse products with search and price filtering.
- List new products for sale with image uploads.

### Cart Functionality
- Add items to a cart.
- Checkout and payment processing using Stripe integration.
- Success and cancellation pages for payment flows.

### Buying Products Using Stripe
- Securely purchase products using Stripe's test mode.
- Automatically clear the cart upon successful purchase.
- Notify users of transaction success or failure.

---

## Installation

### Prerequisites
- **Java Development Kit (JDK) 17+**
- **Apache Maven**
- **PostgreSQL** (or another compatible database)
- **A valid Stripe API key**
- **SMTP server details** for email functionality

---

## Usage

### Endpoints
- `/custom-login`: Login page for existing users.
- `/signup`: Signup page for new users.
- `/products`: View products with optional search and filters.
- `/sell`: Form to list a new product.
- `/cart`: View items in the cart.
- `/cart/buy`: Initiates the Stripe payment process.
- `/forgot-password`: Request password reset.
- `/reset-password`: Resets password using a token.

### Image Uploads
Images for products are stored in the `uploads` directory. Configure the path as needed in the `HelloController`.

### Payment Integration
Stripe is used for payment processing. Ensure you have a valid Stripe API key and configure it in the environment variables.

### Email Functionality
Emails for password reset are sent using the configured SMTP server. Update the `application.properties` file with valid credentials.

---

## Technologies Used
- **Spring Framework** (Boot, MVC, Data JPA, Mail)
- **Thymeleaf** for templates
- **Stripe** for payment processing
- **MySQL** for database
- **JavaMailSender** for email functionality
