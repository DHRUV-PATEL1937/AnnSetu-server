# AnnSetu server

Express + MongoDB + Sarvam API for AnnSetu. This repository contains no React/Vite frontend.

## Local development

```powershell
npm install
Copy-Item .env.example .env
npm run seed
npm run dev
```

Required production settings:

- `MONGODB_URI`
- `JWT_SECRET`
- `SARVAM_API_KEY` (server-only)
- `APP_ORIGIN` as a comma-separated list of hosted frontend origins
- `COOKIE_SAMESITE=none` when frontend and API use different HTTPS origins

The frontend sends credentialed requests to the API URL configured with `VITE_API_URL`.
