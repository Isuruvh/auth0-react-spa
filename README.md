# Auth0 React SPA

A React + TypeScript + Vite single-page app that uses [Auth0](https://auth0.com) for authentication via the `@auth0/auth0-react` SDK.

## Prerequisites

- Node.js 20+
- An Auth0 tenant with a **Single Page Application**

## Auth0 setup

In the Auth0 Dashboard, open your application and set the following to `http://localhost:5173`:

- Allowed Callback URLs
- Allowed Logout URLs
- Allowed Web Origins

## Configuration

Create a `.env` file in the project root (git-ignored, so credentials are never committed):

```
VITE_AUTH0_DOMAIN=your-tenant.region.auth0.com
VITE_AUTH0_CLIENT_ID=your_client_id
```

## Getting started

```bash
npm install
npm run dev
```

Then open http://localhost:5173.

## Scripts

| Command           | Description                   |
| ----------------- | ----------------------------- |
| `npm run dev`     | Start the dev server          |
| `npm run build`   | Type-check and build for prod |
| `npm run preview` | Preview the production build  |
| `npm run lint`    | Lint with Oxlint              |

## Project structure

- `src/main.tsx` - app entry point
- `src/App.tsx` - root component
- `src/LoginButton.tsx` / `src/LogoutButton.tsx` - login and logout actions
- `src/Profile.tsx` - displays the authenticated user's profile

## Security

Never commit `.env` or client secrets.
