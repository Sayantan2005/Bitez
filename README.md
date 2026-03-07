# Bitez - Food Delivery Application

A modern full-stack food delivery application with real-time tracking and order management.

## Features

- **User Authentication**: Sign up, login, and password reset with OTP verification
- **Shop Management**: Create and manage your food shop
- **Food Ordering**: Browse restaurants and order food items
- **Real-time Tracking**: Track your deliveries in real-time
- **Payment Integration**: Razorpay payment gateway
- **Admin Dashboard**: Manage orders and shop operations
- **Delivery Boy Tracking**: Real-time GPS tracking for delivery personnel
- **Image Management**: Cloudinary integration for food images

## Tech Stack

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **Socket.io** for real-time communication
- **SendGrid** for email notifications
- **Razorpay** for payments
- **Cloudinary** for image storage
- **JWT** for authentication

### Frontend
- **React** with Vite
- **Redux** for state management
- **Firebase** for real-time database
- **Tailwind CSS** for styling

## Installation

### Prerequisites
- Node.js (v20.12.1 or higher)
- MongoDB 
- npm or yarn

### Backend Setup

1. Clone the repository
```bash
git clone https://github.com/yourusername/bitez.git
cd bitez/backend
```

2. Install dependencies
```bash
npm install
```

3. Create `.env` file in the backend directory
```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Email (SendGrid)
SENDGRID_API_KEY=your_sendgrid_api_key
EMAIL=your_verified_sender_email@example.com

# JWT
JWT_SECRET=your_jwt_secret_key

# Cloudinary
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# Razorpay
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Frontend URL
CLIENT_URL=http://localhost:5173
```

4. Start the backend server
```bash
npm run dev
```

The backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to frontend directory
```bash
cd ../frontend
```

2. Install dependencies
```bash
npm install
```

3. Create `.env.local` file in the frontend directory
```env
VITE_API_URL=http://localhost:5000
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
```

4. Start the frontend development server
```bash
npm run dev
```

The frontend will run on `http://localhost:5173`

## Email Configuration (SendGrid)

To enable OTP sending for password reset and delivery verification:

1. Sign up for SendGrid at https://sendgrid.com
2. Generate an API key with Full Access permissions
3. Verify your sender email in SendGrid
4. Add `SENDGRID_API_KEY` and `EMAIL` to your `.env` file

## Deployment

### Deploy Backend on Render

1. Push code to GitHub
2. Connect your GitHub repository to Render
3. Set environment variables on Render dashboard
4. Render will auto-deploy on every push

### Deploy Frontend on Vercel

1. Push code to GitHub
2. Connect repository to Vercel
3. Set environment variables
4. Deploy with one click

## Project Structure

```
bitez/
├── backend/
│   ├── controllers/      # Route controllers
│   ├── models/          # MongoDB models
│   ├── routes/          # API routes
│   ├── middleware/      # Custom middleware
│   ├── config/          # Configuration files
│   ├── utils/           # Utility functions
│   └── index.js         # Entry point
└── frontend/
    ├── src/
    │   ├── components/   # React components
    │   ├── pages/       # Page components
    │   ├── hooks/       # Custom hooks
    │   ├── redux/       # Redux store
    │   └── App.jsx      # Main app component
    └── package.json
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - Register new user
- `POST /api/auth/signin` - Login user
- `POST /api/auth/forgot-password` - Send reset OTP
- `POST /api/auth/verify-otp` - Verify OTP

### Shop
- `GET /api/shop/` - Get all shops
- `POST /api/shop/create` - Create new shop
- `PUT /api/shop/:id` - Update shop

### Items
- `GET /api/item/` - Get all items
- `POST /api/item/` - Create new item
- `PUT /api/item/:id` - Update item

### Orders
- `GET /api/order/` - Get user orders
- `POST /api/order/` - Create new order
- `PUT /api/order/:id` - Update order status

## Troubleshooting

### OTP not sending on Render
- Ensure `SENDGRID_API_KEY` and `EMAIL` environment variables are set
- Verify the sender email is verified in SendGrid dashboard
- Check SendGrid Activity feed for error details

### MongoDB connection issues
- Verify connection string is correct
- Ensure MongoDB instance is running
- Check firewall/IP whitelist settings

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

MIT License - see LICENSE file for details

## Support

For issues and questions, please open an issue on GitHub or contact the development team.

---

**Latest Update**: Updated email system to use SendGrid for production-ready email delivery.
