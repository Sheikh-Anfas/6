# MERN Storefront

MERN + JWT + Stripe Checkout test mode.

## Reviewer
Customer: reviewer@example.com / Reviewer123!
Admin: admin@example.com / Admin123!

## Stripe test card
4242 4242 4242 4242
Expiry: any future date
CVC: any 3 digits

## Local
1. `cd server && npm install && cp .env.example .env && npm run seed && npm run dev`
2. `cd client && npm install && cp .env.example .env && npm run dev`

Server env:
MONGODB_URI=...
JWT_SECRET=...
CLIENT_URL=http://localhost:5173
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

Client env:
VITE_API_URL=http://localhost:5000/api

## Deployment
Deploy `client` to Vercel and `server` to Render; use MongoDB Atlas for MONGODB_URI. Add the Stripe webhook:
`POST https://YOUR-RENDER-APP.onrender.com/api/payments/webhook`

Replace these placeholders after deployment:
GitHub: https://github.com/YOUR_USER/YOUR_REPO
Frontend: https://YOUR_VERCEL_APP.vercel.app
API: https://YOUR-RENDER-APP.onrender.com
