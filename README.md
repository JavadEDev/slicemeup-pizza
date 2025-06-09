# 🍕 SliceMeUp Pizza — Full‑Stack Monorepo Template

<p align="center">
  <img
    src="https://raw.githubusercontent.com/JavadEDev/slicemeup-pizza/main/SliceMeUp.png"
    alt="SliceMeUp UI"
    width="450"   
  >
</p>

# 🍕 SliceMeUp Pizza - Full Stack Application

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

src/
├── api/          # API integration and services
├── assets/       # Static assets
├── components/   # Reusable React components
├── routes/       # Application routes
├── __tests__/    # Test files
├── App.jsx       # Main application component
├── main.jsx      # Application entry point
└── index.css     # Global styles


### Server Structure

src/
├── controllers/  # Request handlers
├── models/       # Data models
├── routes/       # API routes
├── services/     # Business logic
├── utils/        # Helper functions
└── config/       # Configuration files


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
- **Framework:** Express.js
- **Database:** Turso
- **Testing:** Jest
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

4. --------------------------------
> Spin up a modern pizza‑ordering SaaS in minutes. This template bundles a React 19 + Vite front‑end with a Node.js with Fastify framework back‑end, wiring them together for local development, CI, and zero‑config deployment on Vercel.

## Why use this template?

* **Batteries‑included**: Real‑time order updates, payment flow stubs, and secure authentication out of the box.
* **Two codebases, one repo**: Keep client and server in sync, share types, and deploy them together.
* **Production‑ready**: ESLint, Prettier, tests, GitHub Actions, and environment‑driven configuration.
* **One‑click deploy**: Vercel configuration files are already in place — just connect and ship.

## 🗂️ Repository structure

```text
.
├── slicemeup-client-app/   # React 19 + Vite front‑end
└── slicemeup-server-app/   # Express back‑end API
```

Each module remains an independent, publishable project so you can still work on or fork them separately.

## 🚀 Quick Start

### 1. Clone the template with submodules

```bash
git clone --recursive https://github.com/JavadEDev/slicemeup-pizza.git
cd slicemeup-pizza
```

> Forgot `--recursive`? Run `git submodule update --init --recursive`.

### 2. Install dependencies

```bash
# Front‑end
(cd slicemeup-client-app && npm install)

# Back‑end
(cd slicemeup-server-app && npm install)
```

### 3. Configure your environment

Copy the example env files and fill in the blanks (database URL, JWT secret, etc.):

```bash
cp slicemeup-client-app/.env.example slicemeup-client-app/.env
cp slicemeup-server-app/.env.example slicemeup-server-app/.env
```

### 4. Run both apps concurrently

From the repository root:

```bash
npm run dev          # Starts client on :5173 and server on :3000
```

or individually:

```bash
npm run dev:client
npm run dev:server
```

Open **[http://localhost:5173](http://localhost:5173)** and order a slice!

## 🌍 Live Demo

* **Front‑end** ⇢ [https://pizza-front-sooty.vercel.app](https://pizza-front-sooty.vercel.app)
* **Back‑end** ⇢ [https://slicemeup-server-app.vercel.app](https://slicemeup-server-app.vercel.app)

## 🛠️ Tech Stack

| Layer          | Tech                                                       | Highlights                                     |
| -------------- | ---------------------------------------------------------- | ---------------------------------------------- |
| **Front‑end**  | React 19, Vite, Tailwind CSS, TanStack Router, React Query | Suspense‑based data fetching, type‑safe routes |
| **Back‑end**   | Node.js, Express, Turso (SQLite‑compatible edge DB)        | Auth, validation, rate‑limiting                |
| **Testing**    | Vitest (client), Jest & Supertest (server)                 | Coverage and CI gating                         |
| **Deployment** | Vercel (client & server), GitHub Actions workflow          | Auto deploy on main                            |

## 📚 API Overview

`/api` is served by `slicemeup-server-app`.

* **Auth**

  * `POST /auth/register` – sign up
  * `POST /auth/login` – sign in
* **Orders**

  * `GET /orders` – list current orders
  * `POST /orders` – place order
  * `GET /orders/:id` – status by id
  * History endpoints are documented in Swagger
* **Support**

  * `POST /contact` – send a message

Interactive OpenAPI docs are available at `/docs` when the server is running.

## 🧑‍🍳 Using this as your own project

1. Click **“Use this template”** on GitHub and create your repo.
2. Update the project name in `package.json` files.
3. Replace the example logo under `SliceMeUp.png` with your brand.
4. Push — CI will run, Vercel will deploy.

## 🧪 Testing

```bash
# Front‑end
(cd slicemeup-client-app && npm test)

# Back‑end
(cd slicemeup-server-app && npm test)
```

Run `npm run coverage` in each module for detailed reports.

## 🔒 Security notes

* CORS locked to allowed origins (configured via env var).
* Rate‑limiting middleware active in production.
* Helmet & HTTPS redirect enabled on Vercel.
* DB credentials never committed.

## 🖥️ CI / CD

GitHub Actions workflow (simplified):

```yaml
name: CI
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci --workspaces
      - run: npm test --workspaces
```

Deployments are handled automatically by Vercel on push to `main`.

## 📦 Building for production

```bash
npm run build:client   # outputs static build to client/dist
npm run build:server   # transpiles server to dist/
```

The Vercel adapters inside each app perform these steps in the cloud.

## 🤝 Contributing

Pull requests are welcome! Please open an issue to discuss major changes.

## 📝 License

MIT © 2025 Javad Esmati

---

Bon appétit and happy coding! 🍕
