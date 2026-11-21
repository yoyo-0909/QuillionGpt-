Quillion GPT — One Platform. Endless Intelligence.

A lightweight multi-provider AI workspace with AI chat, model comparison, productivity tools, and server-side provider configuration.

## Deploy to Vercel
1. Import this GitHub repository into Vercel.
2. In Project Settings → Environment Variables, add provider API keys and model names from `.env.example`.
3. Redeploy. Never commit a real `.env` file or expose provider keys in browser code.

## Local development
Use Node.js 20 or newer and the Vercel CLI. Copy `.env.example` to `.env`, fill in the providers you want to use, then run `vercel dev`.

## Important before sharing
This version does not include user sign-in. Anyone who can access a public deployment may use configured provider keys and consume your API credits. Set provider spending limits and add authentication and production-grade rate limiting before sharing widely.
