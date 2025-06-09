# 🍕 SliceMeUp Pizza - Full Stack Application

<p align="center">
  <img
    src="https://raw.githubusercontent.com/JavadEDev/slicemeup-pizza/main/SliceMeUp.png"
    alt="SliceMeUp UI"
    width="450"   
  >
</p>


A modern, full-stack pizza ordering application built with React (client) and Node.js (server). This project provides a complete solution for pizza ordering with real-time updates, order tracking, and a beautiful user interface.

## 🌟 Project Overview

SliceMeUp Pizza is a full-stack application consisting of two main parts:

- **Client Application**: A modern React-based frontend
- **Server Application**: A robust Node.js backend

### Live Demo

- Frontend: [pizza-front-sooty.vercel.app](https://pizza-front-sooty.vercel.app)
- Backend: [slicemeup-server-app.vercel.app](https://slicemeup-server-app.vercel.app)

## ✨ Features

### Client Features

- 🚀 Built with React 19 and Vite for lightning-fast performance
- 🎨 Modern UI with Tailwind CSS
- 🔄 Real-time updates with React Query
- 🛣️ Type-safe routing with TanStack Router
- 📱 Fully responsive design
- 🎯 Error boundary implementation
- 🔍 ESLint and Prettier for code quality

### Server Features

- 🔒 Secure API endpoints with CORS protection
- 📦 Database integration with Turso
- 🔄 Real-time order processing
- 📝 Comprehensive API documentation
- 🛡️ Input validation and error handling
- 📊 Order tracking and history
- 📧 Contact form support

## 🏗️ Project Structure


### Client Structure
```
src/
├── api/          # API integration and services
├── assets/       # Static assets
├── components/   # Reusable React components
├── routes/       # Application routes
├── __tests__/    # Test files
├── App.jsx       # Main application component
├── main.jsx      # Application entry point
└── index.css     # Global styles
```

### Server Structure
```
src/
├── controllers/  # Request handlers
├── models/       # Data models
├── routes/       # API routes
├── services/     # Business logic
├── utils/        # Helper functions
└── config/       # Configuration files
```

## 🚀 Getting Started

### Prerequisites

- Node.js (Latest LTS version recommended)
- npm or yarn
- Git

### Installation

1. Clone both repositories:

bash
# Clone client repository
git clone https://github.com/JavadEDev/slicemeup-client-app.git
cd slicemeup-client-app

# Clone server repository
git clone https://github.com/JavadEDev/slicemeup-server-app.git
cd slicemeup-server-app


2. Install dependencies for both projects:

bash
# Client
cd slicemeup-client-app
npm install

# Server
cd ../slicemeup-server-app
npm install


3. Start both applications:

bash
# Client (in client directory)
npm run dev

# Server (in server directory)
npm run dev


The applications will be available at:

- Client: http://localhost:5173
- Server: http://localhost:3000

## 🛠️ Tech Stack

### Frontend

- **Framework:** React 19
- **Build Tool:** Vite
- **Styling:** Tailwind CSS
- **State Management:** React Query
- **Routing:** TanStack Router
- **Testing:** Vitest
- **Code Quality:** ESLint, Prettier

### Backend

- **Runtime:** Node.js
- **Framework:** Fastify
- **Database:** Turso
- **Testing:** Jest & Supertest
- **API Documentation:** Swagger/OpenAPI
- **Security:** CORS, Rate Limiting

## 📚 API Endpoints

### Authentication

- POST /api/auth/login - User login
- POST /api/auth/register - User registration

### Orders

- GET /api/orders - Get all orders
- GET /api/orders/:id - Get specific order
- POST /api/orders - Create new order
- GET /api/past-orders - Get order history
- GET /api/past-order/:order_id - Get specific past order

### Customer Support

- POST /api/contact - Submit contact form

## 🧪 Testing

### Client Testing

bash
# Run unit tests
npm run test

# Run UI tests
npm run test:ui

# Generate coverage
npm run coverage


### Server Testing

bash
# Run unit tests
npm test

# Run integration tests
npm run test:integration

# Run end-to-end tests
npm run test:e2e


## 🔒 Security Features

- CORS protection with specific allowed origins
- Environment variable management
- Secure database connections
- Input validation
- Error handling and logging
- Transaction management
- Rate limiting (production)

## 📦 Deployment

The application is configured for deployment on Vercel:

- Frontend: https://pizza-front-sooty.vercel.app
- Backend: https://pizza-server-iota.vercel.app

### Allowed Origins

- https://pizza-front-sooty.vercel.app
- https://pizza-server-iota.vercel.app/
- http://localhost:5173 (development)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Author

- Javad Esmati

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape this project
- Special thanks to the open-source community
- Turso for providing the database infrastructure
- Vercel for hosting services

## 📞 Support

For support, please:

1. Open an issue in the GitHub repository
2. Use the contact form in the application
3. Check the documentation for common issues
