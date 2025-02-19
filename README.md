# Subscription Manager API

A comprehensive subscription management API built with Express.js, Mongoose, and Nodemailer, designed to streamline the process of managing user subscriptions and sending timely reminders. The API features secure user authentication using JWT, robust error handling, and middleware for rate limiting and bot detection via Arcjet. It integrates with Upstash for workflow automation, ensuring that subscription reminders are sent at the right time. The project is configured for different environments using dotenv and supports email notifications through Nodemailer. Designed for scalability and ease of use, this API provides a solid foundation for managing subscriptions and user interactions efficiently.

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#-tech-stack">Tech Stack</a>
    </li>
    <li>
      <a href="#-features">Features</a>
    </li>
    <li>
      <a href="#-getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#-key-components">Key Components</a></li>
    <li><a href="#-middleware">Middleware</a></li>
    <li><a href="#-database-schema">Database Schema</a></li>
    <li><a href="#-future-improvements">Future Improvements</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## 🚀 Tech Stack

- **Framework**: Express.js
- **Language**: JavaScript (Node.js)
- **Authentication**: JWT
- **Database**: MongoDB (with Mongoose)
- **Email**: Nodemailer
- **Workflow Automation**: Upstash
- **Rate Limiting & Bot Detection**: Arcjet

## 🛠 Getting Started

### Prerequisites

- npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. **Clone the repository**

```sh
git clone https://github.com/xeo3221/subscription-manager-api.git
cd subscription-manager-api
```

2. **Install dependencies**

```sh
npm install
```

3. **Set up environment variables**

```sh
cp .env.example .env
```

Fill in the required environment variables:

- `DB_URI`
- `JWT_SECRET`
- `ARCJET_KEY`
- `QSTASH_TOKEN`
- `ACCOUNT_EMAIL`
- `EMAIL_PASSWORD`

4. **Start the development server**

```sh
npm run dev
```

## 🌟 Features

- **Authentication & Authorization**

  - Secure user authentication with JWT
  - Protected routes and API endpoints

- **Subscription Management**

  - Create, update, and delete subscriptions
  - Send subscription reminders via email

- **Error Handling**

  - Centralized error handling middleware
  - Custom error messages and status codes

- **Rate Limiting & Bot Detection**

  - Protect endpoints from abuse with Arcjet

## 📦 Key Components

- `auth.middleware.js`: Middleware for JWT authentication
- `error.middleware.js`: Centralized error handling
- `subscription.controller.js`: Controller for subscription-related operations
- `user.controller.js`: Controller for user-related operations

## 🛡️ Middleware

- `authorize`: Middleware to verify JWT tokens and protect routes
- `errorHandler`: Middleware to handle errors and send appropriate responses

## 📝 Database Schema

The application uses a MongoDB database with the following main collections:

- `users`: User profiles
- `subscriptions`: Subscription details

## 🔮 Future Improvements

- **Enhanced Notification System**

  - SMS notifications for subscription reminders

- **Advanced Subscription Features**

  - Tiered subscription plans
  - Subscription analytics and reporting

## Acknowledgments

- [Express.js](https://expressjs.com/)
- [Mongoose](https://mongoosejs.com/)
- [Nodemailer](https://nodemailer.com/)
- [JWT](https://jwt.io/)
- [Upstash](https://upstash.com/)
- [Arcjet](https://arcjet.com/)
