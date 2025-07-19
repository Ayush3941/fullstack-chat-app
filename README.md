# ✨ Full Stack Realtime Chat App ✨

![Demo App](/frontend/public/screenshot-for-readme.png)

[Video Tutorial on Youtube](https://youtu.be/ntKkVrQqBYY)

## Highlights:

- 🌟 Tech stack: MERN (MongoDB, Express.js, React, Node.js) + Socket.io + TailwindCSS + Daisy UI
- 🎃 Authentication & Authorization using JWT tokens
- 👾 Real-time messaging powered by Socket.io
- 🚀 Online user status indicator
- 👌 Global state management with Zustand
- 🐞 Robust error handling on both server and client sides
- ⭐ Final deployment guide for FREE hosting
- ⏳ And much more!

## Setting up `.env` file (Environment Variables)

Create a `.env` file in the **root directory** of your project and add the following keys with appropriate values:

```env
MONGODB_URI=your_mongodb_connection_uri
PORT=5001
JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

NODE_ENV=development
```

### How to obtain these keys:

### 1. **MONGODB_URI (MongoDB Database Connection URI)**
   - Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
   - Sign up for a free account and create a new **free cluster**.
   - Under your cluster, click **Database Access** > create a new database user with proper privileges.
   - Under **Network Access**, whitelist your IP address or allow access from anywhere (0.0.0.0/0).
   - Under **Connect** > **Connect your application**, copy the connection string.
     - Replace `<password>` with the database user's password.
     - Replace `test` with your database name if required.

Example:
```env
MONGODB_URI=mongodb+srv://username:<password>@cluster0.mongodb.net/chatapp?retryWrites=true&w=majority
```

### 2. **JWT_SECRET (JSON Web Token Secret Key)**
   - This is a secret string used to sign and verify JWT tokens.
   - You can generate one securely using:
```shell
openssl rand -base64 32
```
   - Or manually set a long random string:
```env
JWT_SECRET=your_long_random_secret_key
```

### 3. **CLOUDINARY_CLOUD_NAME, CLOUDINARY_API_KEY, CLOUDINARY_API_SECRET (for Image Uploading)**
   - Go to [Cloudinary](https://cloudinary.com/)
   - Sign up for a free account.
   - After signing in, navigate to your **Dashboard**.
   - Copy the following from your account:
     - `Cloud name`
     - `API key`
     - `API secret`

Your `.env` entries should look like this:
```env
CLOUDINARY_CLOUD_NAME=your_cloud_name_here
CLOUDINARY_API_KEY=your_api_key_here
CLOUDINARY_API_SECRET=your_api_secret_here
```

### 4. **PORT**
   - By default, use `5001`. You can change this as needed.

### 5. **NODE_ENV**
   - For development purposes, set this as:
```env
NODE_ENV=development
```

## Commands to Run the App

### Install Dependencies
```shell
npm install
```

### Build the App
```shell
npm run build
```

### Start the App
```shell
npm start
```

## Running in Development Mode
For easier debugging during development, you can use:
```shell
npm run dev
```

---

## Troubleshooting
- Ensure all `.env` variables are set correctly.
- Verify MongoDB Atlas access and connection string.
- Confirm Cloudinary credentials are correct.
- If ports conflict, change the PORT in `.env`.

## Deployment
Once you have tested locally, refer to the provided [Video Tutorial](https://youtu.be/ntKkVrQqBYY) for step-by-step instructions on deploying the app for free using platforms like **Render**, **Vercel**, or **Netlify** (for frontend) and **Render** (for backend).

---

If you face any issues, raise an issue in this repository or refer to the [Video Tutorial](https://youtu.be/ntKkVrQqBYY).
