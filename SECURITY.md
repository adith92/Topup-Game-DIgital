# Security Policy

Fitbite is currently a demo-first healthy food-tech application. This file defines the baseline security rules before the project is expanded into production.

## Supported Scope

The current security scope covers:

- Next.js App Router routes
- Server-side API routes under `app/api/*`
- OpenRouter integration
- Supabase future integration
- Vercel deployment environment

## Secrets and Environment Variables

Never commit real secrets to this repository.

Sensitive variables must only be configured in Vercel Environment Variables or a local `.env` file that is ignored by Git.

Important variables:

```txt
AI_PROVIDER=openrouter
OPENROUTER_API_KEY=
OPENROUTER_MODEL=
OPENROUTER_SITE_URL=
OPENROUTER_APP_NAME=
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
TELEGRAM_BOT_TOKEN=
WHATSAPP_ACCESS_TOKEN=
```

Rules:

- `OPENROUTER_API_KEY` must stay server-side only.
- `SUPABASE_SERVICE_ROLE_KEY` must never be used in a client component.
- `NEXT_PUBLIC_*` variables are public by design and must not contain private secrets.
- Do not log request bodies if they may contain private user information.

## API Hardening Checklist

Before production traffic, every API route should have:

- Request body validation with Zod or equivalent schema validation.
- Rate limiting per IP, user, or session.
- Safe error logging without secrets.
- Strict method handling.
- Clear JSON error responses.

Current priority endpoint:

```txt
POST /api/ai/pantry-wizard
```

## Admin Protection

All `/admin` features must be treated as private by default.

Production requirement:

- Add Supabase Auth or equivalent authentication.
- Protect `/admin` through Next.js middleware.
- Never expose operational data without authentication.

The current admin page is allowed only as a non-sensitive demo preview.

## Dependency Safety

Dependencies should be pinned in `package.json` and locked with `package-lock.json`.

Required checks before deploy:

```bash
npm ci
npm run typecheck
npm run lint
npm run build
```

## Reporting Issues

If you find a security issue, do not open a public issue with secret details. Contact the repository owner directly first.

## Medical and Nutrition Safety

Fitbite nutrition output is an estimate for general wellness use only. It is not medical advice and should not replace consultation with a doctor or certified nutrition professional.
