# 🚀 Deploy Quillion GPT to Vercel

This project uses Vercel serverless functions in the `api/` directory. Import the GitHub repository into Vercel and keep the project root as the repository root.

## 1. Import the repository

1. Open [Vercel](https://vercel.com/new).
2. Choose **Import Git Repository** and select `yoyo-0909/QuillionGpt-`.
3. Keep the default framework preset / build settings unless Vercel prompts otherwise.
4. Deploy once to create the project.

## 2. Add provider environment variables

In **Vercel → Project → Settings → Environment Variables**, add the key and model variables for each provider you want to enable.

| Provider | API key variable | Model variable |
|:--|:--|:--|
| OpenAI | `OPENAI_API_KEY` | `OPENAI_MODEL` |
| Anthropic | `ANTHROPIC_API_KEY` | `ANTHROPIC_MODEL` |
| Google | `GOOGLE_API_KEY` | `GOOGLE_MODEL` |
| Mistral | `MISTRAL_API_KEY` | `MISTRAL_MODEL` |
| DeepSeek | `DEEPSEEK_API_KEY` | `DEEPSEEK_MODEL` |

Use model IDs that are available to your account. You can configure one provider or several. Both variables for a provider must be set.

## 3. Redeploy

After adding or changing environment variables, trigger a new deployment. Open the generated Vercel URL and check the AI Models view to see configured providers.

## 4. Local development

1. Install Node.js 20 or newer.
2. Install the Vercel CLI: `npm install --global vercel`.
3. Copy `.env.example` to `.env` and add your own credentials.
4. Run `vercel dev`.

## ⚠️ Before sharing a public demo

This prototype does not have user authentication. Anyone who can access a public deployment may be able to send requests through your configured provider accounts and consume your API credits.

- Set strict spending limits and usage alerts in every provider dashboard.
- Do not commit `.env` or paste API keys into frontend code.
- The current in-memory rate limiter is best-effort and may not be reliable across serverless instances.
- Add authentication and shared, production-grade rate limiting before opening the app to the public.

A deployment URL is not proof that the app is production-ready. Test each configured provider and monitor usage after deployment.
