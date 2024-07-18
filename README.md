# FoodPanda README

## Overview
FoodPanda is a comprehensive food ordering system built with Spring Boot, React, Tailwind CSS, and integrated with Stripe for seamless payment processing. This application allows users to browse menus, place orders, and make payments online, providing a streamlined experience for both customers and restaurant owners.

## Table of Contents
1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Project Structure](#project-structure)
7. [Configuration](#configuration)
8. [Contributing](#contributing)
9. [License](#license)

## Features
- User authentication and authorization
- Browse restaurant menus and items
- Add items to the cart and place orders
- Stripe payment integration for secure transactions


## Tech Stack
- **Backend**: Spring Boot, Java
- **Frontend**: React, JavaScript, Tailwind CSS
- **Payment Gateway**: Stripe
- **Database**: MySQL
- **Build Tools**: Maven, npm

## Prerequisites
- Java 11 or higher
- Node.js 14.x or higher
- npm 6.x or higher
- MySQL 5.7 or higher
- Stripe account

## Installation

### Backend Setup
1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/foodpanda.git
    cd foodpanda/backend
    ```

2. **Configure MySQL database:**
   - Create a new database in MySQL.
   - Update the `application.properties` file with your MySQL database details:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
     spring.datasource.username=your_username
     spring.datasource.password=your_password
     ```

3. **Build the backend:**
    ```sh
    mvn clean install
    ```

4. **Run the backend:**
    ```sh
    mvn spring-boot:run
    ```

### Frontend Setup
1. **Navigate to the frontend directory:**
    ```sh
    cd ../frontend
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Install Tailwind CSS:**
    ```sh
    npm install -D tailwindcss
    npx tailwindcss init
    ```

4. **Configure Tailwind CSS:**
    - Add the paths to all of your template files in `tailwind.config.js`:
      ```js
      module.exports = {
        content: [
          "./src/**/*.{js,jsx,ts,tsx}",
        ],
        theme: {
          extend: {},
        },
        plugins: [],
      }
      ```

    - Add the Tailwind directives to your CSS in `src/index.css`:
      ```css
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
      ```

5. **Start the frontend server:**
    ```sh
    npm start
    ```

## Usage
1. Open your browser and navigate to `http://localhost:3000`.
2. Register a new account or log in with existing credentials.
3. Browse restaurants, add items to the cart, and place an order.
4. Use the Stripe payment gateway to complete the purchase.

## Configuration
### Stripe Integration
1. **Create a `.env` file in the `frontend` directory with your Stripe API keys:**
    ```env
    REACT_APP_STRIPE_PUBLIC_KEY=your_public_key
    REACT_APP_STRIPE_SECRET_KEY=your_secret_key
    ```

2. **Update the backend with your Stripe secret key in `application.properties`:**
    ```properties
    stripe.apiKey=your_secret_key
    ```

## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

