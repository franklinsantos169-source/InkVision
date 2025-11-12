# InkVision - Tattoo Preview (MVP)

This is a minimal Vite + React project to demo InkVision: AI-generated tattoo previews.

## Features
- Describe a tattoo and generate an AI image (server-side call to Replicate)
- Upload a photo to preview the tattoo on skin (client-side)
- Move, rotate and scale tattoo overlay (mobile touch support)
- Premium upgrade simulated on frontend

## How to deploy (Vercel) — recommended for mobile users
1. Create a Vercel account (https://vercel.com) and install Vercel CLI if you want, or use their dashboard.
2. Create a new project and connect your Git repository or use 'Import from GitHub' and push this repo.
3. In Vercel project settings -> Environment Variables, add:
   - `REPLICATE_API_TOKEN` = your replicate API token
4. Deploy the project. Vercel will build and serve it.
5. The serverless function `api/generate.js` will handle requests to Replicate securely.

## Local development (optional)
```
npm install
npm run dev
```

## Payments / Monetization
- This repo includes a simulated Premium button. For real subscriptions:
  - Use Stripe Checkout / Billing.
  - Protect `/api/generate` with authentication (only allow requests from logged-in premium users).
  - Store user data and subscriptions in a DB (Supabase or Firebase recommended).

## Notes
- Keep your Replicate token secret. Use serverless functions (Vercel) to avoid exposing keys in the browser.
- The chosen model in `api/generate.js` is set to an example realistic model. You can change it in the server code.

Good luck — launch and promote on social (Product Hunt, TikTok) and reach tattoo studios for partnerships.
