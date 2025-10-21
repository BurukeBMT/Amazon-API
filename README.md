# 💳 Amazon API

A simple Express.js API for handling payments using Stripe, designed to work with the Amazon Clone frontend. 🚀

**Repository:** [GitHub](https://github.com/BurukeBMT/Amazon-API.git) 📂

## ✨ Features

- **💳 Payment Processing**: Create payment intents using Stripe for secure transactions.
- **🌐 CORS Support**: Configured to allow cross-origin requests from the frontend.
- **⚠️ Error Handling**: Proper error responses for invalid requests.
- **🔐 Environment Configuration**: Uses environment variables for sensitive data like Stripe keys.

## 🛠️ Tech Stack

- **🟢 Node.js**: JavaScript runtime for server-side development.
- **🚀 Express.js**: Web framework for building the API.
- **💳 Stripe**: Payment processing library.
- **🌐 CORS**: Middleware for handling cross-origin requests.
- **📄 Dotenv**: For loading environment variables.

## 📦 Installation

1. **📥 Clone the repository**:
   ```bash
   git clone <repository-url>
   cd amazon-api
   ```

2. **📦 Install dependencies**:
   ```bash
   npm install
   ```

3. **🔧 Set up environment variables**:
   Create a `.env` file in the root directory and add your Stripe secret key:
   ```
   STRIPE_KEY=your_stripe_secret_key_here
   ```

4. **▶️ Start the server**:
   - For development: `npm run dev`
   - For production: `npm start`

   The server will run on `http://localhost:5000`. 🌐

## 🔗 API Endpoints

### GET /
- **📋 Description**: Health check endpoint.
- **📤 Response**: `{ "message": "Success!" }`

### POST /payment/create
- **💳 Description**: Creates a Stripe payment intent.
- **🔍 Query Parameters**:
  - `total` (integer): The total amount in cents (e.g., 1000 for $10.00).
- **📤 Response** (Success):
  ```json
  {
    "clientSecret": "pi_xxx_secret_xxx"
  }
  ```
- **❌ Response** (Error):
  ```json
  {
    "message": "Total must be greater than 0"
  }
  ```

## 🚀 Usage

This API is intended to be used with the Amazon Clone frontend application. It handles payment processing for orders. 🛒

The API is deployed and available at: **https://amazon-api-0az0.onrender.com** 🌐

### 📝 Example Request
```bash
curl -X POST "https://amazon-api-0az0.onrender.com/payment/create?total=1000"
```

For local development, use `http://localhost:5000`.

## 🔐 Environment Variables

- `STRIPE_KEY`: Your Stripe secret key. Obtain this from your Stripe dashboard. 🔑

## 🤝 Contributing

1. 🍴 Fork the repository.
2. 🌿 Create a feature branch.
3. 🔄 Make your changes.
4. ✅ Test thoroughly.
5. 📤 Submit a pull request.

## 📄 License

This project is licensed under the ISC License. 📜

## 🎓 Educational Purpose

This project is created for educational purposes to demonstrate payment processing with Stripe in test mode. 💳

### 🧪 Test Payment Details
- **Card Number:** 4242 4242 4242 4242 (Visa)
- **CVC:** Any 3 digits
- **Expiration Date:** Any date after today (MM/YY)
- **Postal Code:** Any valid postal code
