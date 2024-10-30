# head_shop
Here’s a polished and professional version of your `README.md` that maintains clarity without being overly flashy:

---

# Product Order System with Telegram Bot

Welcome to the **Product Order System**! This project enables users to order products through a web interface and receive order confirmations via a Telegram bot. The system is built with a PHP backend, a MySQL database for data storage, and a Telegram bot for real-time notifications.

## Project Structure

```
.
├── tg.py                     # Telegram bot script
├── index.html                # Main landing page
├── registration.html         # User registration page
├── order_confirmation.html    # Order confirmation page
├── style.css                 # Styles for the frontend
├── submit_order.php          # PHP script to process order submissions
├── .env                      # Environment variables for sensitive data
├── config.py                 # Configuration file for Python
└── db/                       # Database files (if applicable)
```

## Features

- **Product Ordering**: Users can easily order products by filling out a simple form.
- **Order Confirmation via Telegram**: Users receive real-time notifications about their orders through a Telegram bot.
- **Data Storage**: All orders and user information are securely stored in a MySQL database.

## Setup Instructions

### Prerequisites

Before you begin, ensure you have the following installed:

- **PHP** and **MySQL** on your machine.
- **Python 3** with necessary libraries.
- **Composer** for PHP dependency management.
- A **Telegram Bot Token** from [BotFather](https://core.telegram.org/bots#botfather).

### Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd project-folder
   ```

2. **Install PHP dependencies**:
   ```bash
   composer install
   ```

3. **Set up the environment file**:
   Create a `.env` file in the root directory with the following content:

   ```plaintext
   DB_SERVERNAME=localhost
   DB_USERNAME=root
   DB_PASSWORD=your_password
   DB_NAME=shop

   TELEGRAM_API_TOKEN=your_telegram_api_token
   ```

4. **Set up the MySQL database**:
   - Create a MySQL database named `shop`.
   - Import the database schema or create the necessary tables. For example:

     ```sql
     CREATE TABLE orders (
         id INT AUTO_INCREMENT PRIMARY KEY,
         product VARCHAR(255) NOT NULL,
         quantity INT NOT NULL,
         name VARCHAR(255),
         email VARCHAR(255),
         phone VARCHAR(20),
         address TEXT,
         cap_color VARCHAR(50)
     );
     ```

5. **Update `config.py`**:
   Ensure `config.py` has the correct API token and database credentials.

### Running the Project

- **Run the web server**:
  Use a local server like Apache or the built-in PHP server:
  ```bash
  php -S localhost:8000
  ```

- **Run the Telegram bot**:
  ```bash
  python3 tg.py
  ```

### Deploying to Production

Deploy the project to a hosting provider that supports PHP and Python. Be sure to update the `.env` file with production credentials.

## Usage

1. **Place an Order**: Navigate to `index.html` in your browser, fill out the order form, and submit.
2. **Receive Confirmation**: You will receive an order confirmation via Telegram if set up correctly.

## Troubleshooting

- **Database Connection Issues**: Check that your `.env` file contains the correct credentials and that the database is accessible.
- **Telegram Bot Not Responding**: Ensure that the `TELEGRAM_API_TOKEN` in your `.env` file is valid and that `tg.py` is running.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it as you wish!

---

This version keeps it professional and straightforward while ensuring all necessary information is presented clearly. Let me know if you need any further adjustments!
