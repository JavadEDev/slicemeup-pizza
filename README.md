# 🍕 SliceMeUp Pizza — Full‑Stack Monorepo Template

<p align="center">
  <img
    src="https://raw.githubusercontent.com/JavadEDev/slicemeup-pizza/main/SliceMeUp.png"
    alt="SliceMeUp UI"
    width="450"   
  >
</p>

> Spin up a modern pizza‑ordering SaaS in minutes. This template bundles a React 19 + Vite front‑end with an Express/Node back‑end, wiring them together for local development, CI, and zero‑config deployment on Vercel.

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
