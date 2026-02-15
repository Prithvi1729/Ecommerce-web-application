# MERN E-commerce Web Application

This repository contains a full-stack e-commerce app:

- **Frontend:** React (Create React App)
- **Backend:** Node.js + Express
- **Database:** MongoDB (Mongoose)

## 1) Run locally

### Prerequisites

- Node.js 18+
- npm 9+
- MongoDB database (local or Atlas)

### Environment variables

Create `backend/.env` from `backend/.env.example` and set at minimum:

```bash
JWT_SECRET=your-secret
MONGODB_URI=your-mongodb-connection-string
PAYPAL_CLIENT_ID=sb
```

You can keep the rest empty unless you need uploads/maps/mail features.

### Install dependencies

```bash
npm install
npm --prefix backend install
npm --prefix frontend install
```

### Start development servers

Use two terminals:

**Terminal 1 (backend API):**

```bash
npm run start:backend
```

**Terminal 2 (frontend app):**

```bash
npm run start:frontend
```

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:5000`

### Production-style local run

```bash
npm run build
npm start
```

This builds the frontend and serves it through Express.

---

## 2) Deploy on Vercel

This repo is configured for Vercel using:

- `api/index.js` as the serverless API entry point
- `frontend` as a static React build
- `vercel.json` for API + SPA routing

### Steps

1. Push this repo to GitHub/GitLab/Bitbucket.
2. In Vercel, **Add New Project** and import the repo.
3. Keep root as project directory.
4. In **Environment Variables**, set:
   - `MONGODB_URI`
   - `JWT_SECRET`
   - `PAYPAL_CLIENT_ID`
   - Any optional variables you use (`GOOGLE_API_KEY`, `CLOUDINARY_*`, `MAILGUN_*`).
5. Deploy.

### Notes

- All `/api/*` routes are handled by the Express serverless function.
- All other routes are served as frontend SPA routes.
- If you use external services (Cloudinary, Mailgun, Google Maps), set those env vars in Vercel too.
