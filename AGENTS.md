# Mandi Connect

Agricultural marketplace connecting farmers directly with buyers with live APMC rates from Agmarknet.

## Deployment on Vercel

1. Push this repository to GitHub / GitLab / Bitbucket.
2. Import the project into **Vercel** ([vercel.com](https://vercel.com)).
3. Vercel will automatically read `vercel.json` and build using `npm run build`.
4. Add the required Environment Variables in the Vercel Project Settings:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_PUBLISHABLE_KEY`
   - `SUPABASE_URL`
   - `SUPABASE_PUBLISHABLE_KEY`
   - `TWILIO_ACCOUNT_SID`
   - `TWILIO_AUTH_TOKEN`
   - `TWILIO_API_KEY_SID`
   - `TWILIO_API_KEY_SECRET`
   - `TWILIO_VERIFY_SERVICE_SID`
   - `DATA_GOV_API_KEY`
