# imagify
This web application allows users to generate AI-powered images from text prompts using the ClipDrop API, with image optimization handled by Imagify.
# 🖼️ Imagify Prompt-to-Image Generator

A full-stack web application that allows users to generate AI-powered images from text prompts using the ClipDrop API, optimize them using Imagify, and manage user credits with integrated payment options.

---

## 🚀 Features

- 🔐 JWT-based Authentication system
- 🎁 **5 Free Credits** on signup
- 💬 Generate AI images via **ClipDrop API**
- 📉 Images optimized via **Imagify API**
- 📦 Store image metadata in **MongoDB Atlas**
- 🛑 Credit deduction per image generation
- 💳 Credit Recharge via **Razorpay** and **Stripe**

---

## 🧪 How It Works

1. Users register or log in (JWT Auth).
2. Each new user is assigned **5 credits**.
3. When a user enters a text prompt:
   - The app sends it to the **ClipDrop API** to generate an image.
   - 1 credit is deducted per request.
   - The resulting image is passed through the **Imagify API** for compression.
4. Optimized image is stored in MongoDB (or served directly).
5. Once credits are exhausted, user must **purchase more credits**:
   - Indian Users: via **Razorpay**
   - International Users: via **Stripe**

---

## 🧱 Tech Stack

| Layer         | Technology          |
|---------------|---------------------|
| Frontend      | HTML, CSS, JS / React (optional) |
| Backend       | Node.js + Express.js |
| Auth          | JWT                 |
| Database      | MongoDB Atlas       |
| Image Gen     | [ClipDrop API](https://clipdrop.co/apis) |
| Optimization  | [Imagify API](https://imagify.io) |
| Payments      | Razorpay & Stripe   |

---

## 🔐 API Keys & Config (`.env`)

```env
JWT_SECRET="your_jwt_secret"

# MongoDB
MONGODB_URI="your_mongodb_uri"

# ClipDrop API (Prompt to Image)
CLIPDROP_API="your_clipdrop_api_key"

# Imagify API
IMAGIFY_API="your_imagify_api_key"

# Razorpay
RAZORPAY_KEY_ID="your_razorpay_key_id"
RAZORPAY_KEY_SECRET="your_razorpay_key_secret"

# Stripe
STRIPE_SECRET_KEY="your_stripe_secret"
